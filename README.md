<script>
const API_KEY = 'ouX4lmi5e83b0dca8a8a9bebuRE46ojF';

// Proxy list untuk bypass CORS (dicoba berurutan)
const PROXIES = [
  'https://corsproxy.io/?',
  'https://api.allorigins.win/raw?url=',
  'https://cors-anywhere.herokuapp.com/',
];

async function fetchWithProxy(url) {
  // Coba tanpa proxy dulu
  try {
    const r = await fetch(url, { signal: AbortSignal.timeout(8000) });
    if (r.ok) return r;
  } catch(e) {}

  // Coba tiap proxy
  for (const proxy of PROXIES) {
    try {
      const proxyUrl = proxy + encodeURIComponent(url);
      const r = await fetch(proxyUrl, { signal: AbortSignal.timeout(10000) });
      if (r.ok) return r;
    } catch(e) {}
  }
  throw new Error('Semua proxy gagal');
}

const courierIcons = {
  sicepat: '🔴', jne: '🔴', jnt: '🟠', anteraja: '🔵', pos: '🔴',
  ninja: '🟠', tiki: '🟡', rpx: '🟢', sap: '🟣', wahana: '🔵',
  idexpress: '🟠', lion: '🩷', paxel: '🟤', ncs: '⚪', sentral: '🟤',
  lazada: '🔵', shopee: '🟠', grab: '🟢', gosend: '🟢'
};

const courierNames = {
  sicepat: 'SiCepat', jne: 'JNE', jnt: 'J&T Express', anteraja: 'Anteraja',
  pos: 'Pos Indonesia', ninja: 'Ninja Xpress', tiki: 'TIKI', rpx: 'RPX',
  sap: 'SAP Express', wahana: 'Wahana', idexpress: 'ID Express', lion: 'Lion Parcel',
  paxel: 'Paxel', ncs: 'NCS', sentral: 'Sentral Cargo', lazada: 'Lazada Express',
  shopee: 'Shopee Express', grab: 'Grab Express', gosend: 'GoSend'
};

function getStatusClass(status) {
  const s = (status || '').toLowerCase();
  if (s.includes('delivered') || s.includes('terima') || s.includes('serah') || s.includes('diterima')) return 'status-delivered';
  if (s.includes('transit') || s.includes('proses') || s.includes('antar') || s.includes('pickup') || s.includes('manifest') || s.includes('sorting')) return 'status-transit';
  if (s.includes('pending') || s.includes('menunggu') || s.includes('booking')) return 'status-pending';
  return 'status-transit';
}

function getStatusLabel(status) {
  const s = (status || '').toLowerCase();
  if (s.includes('delivered') || s.includes('terima') || s.includes('serah') || s.includes('diterima')) return '✅ Terkirim';
  if (s.includes('transit') || s.includes('sorting')) return '🚚 Dalam Transit';
  if (s.includes('antar') || s.includes('courier')) return '🛵 Dalam Pengiriman';
  if (s.includes('pickup') || s.includes('manifest')) return '📦 Diambil Kurir';
  if (s.includes('pending') || s.includes('booking')) return '⏳ Menunggu';
  return '🚚 ' + (status || 'Dalam Proses');
}

function setProgress(pct) {
  const bar = document.getElementById('progressBar');
  const fill = document.getElementById('progressFill');
  bar.style.display = 'block';
  fill.style.width = pct + '%';
  if (pct >= 100) {
    setTimeout(() => {
      bar.style.display = 'none';
      fill.style.width = '0%';
    }, 600);
  }
}

async function trackPackage() {
  const courier = document.getElementById('courierSelect').value;
  const resi = document.getElementById('resiInput').value.trim();

  if (!courier)
    return showError('Silakan pilih ekspedisi terlebih dahulu.');
  if (!resi)
    return showError('Masukkan nomor resi yang ingin dilacak.');

  // Reset
  document.getElementById('errorBox').classList.remove('show');
  document.getElementById('result').classList.remove('show');
  document.getElementById('hintBox').style.display = 'none';
  document.getElementById('trackBtn').disabled = true;
  document.getElementById('loading').classList.add('show');

  setProgress(20);
  document.getElementById('loadingText').textContent =
    'Menghubungi server ' + courierNames[courier] + '...';

  setTimeout(() => setProgress(60), 400);

  try {
    const url =
      `https://api.binderbyte.com/v1/track?api_key=${API_KEY}&courier=${courier}&awb=${encodeURIComponent(resi)}`;

    let res, data;

    try {
      res = await fetchWithProxy(url);
    } catch(netErr) {
      setProgress(100);
      document.getElementById('loading').classList.remove('show');
      document.getElementById('trackBtn').disabled = false;

      showError(
        'Gagal terhubung ke server. Periksa koneksi internet Anda.'
      );

      document.getElementById('hintBox').style.display = 'block';
      return;
    }

    try {
      data = await res.json();
    } catch(e) {
      setProgress(100);
      document.getElementById('loading').classList.remove('show');
      document.getElementById('trackBtn').disabled = false;

      showError(
        'Server mengembalikan respons yang tidak valid.'
      );
      return;
    }

    setProgress(100);
    document.getElementById('loading').classList.remove('show');
    document.getElementById('trackBtn').disabled = false;

    if (data.status !== 200 || !data.data) {
      let msg = data.message || 'Nomor resi tidak ditemukan.';

      if (msg.toLowerCase().includes('api key')) {
        msg =
          'API Key tidak valid atau kuota habis.';
      }

      showError(msg);
      document.getElementById('hintBox').style.display = 'block';
      return;
    }

    renderResult(data.data, courier, resi);

  } catch (e) {
    setProgress(100);
    document.getElementById('loading').classList.remove('show');
    document.getElementById('trackBtn').disabled = false;

    showError('Terjadi kesalahan: ' + e.message);
    document.getElementById('hintBox').style.display = 'block';
  }
}

function showError(msg) {
  const box = document.getElementById('errorBox');
  box.textContent = '⚠️ ' + msg;
  box.classList.add('show');
}

function renderResult(data, courier, resi) {
  const summary = data.summary || {};
  const history = data.history || [];

  const latestStatus =
    summary.status ||
    (history[0] && history[0].status) ||
    'Dalam Proses';

  const statusClass = getStatusClass(latestStatus);
  const statusLabel = getStatusLabel(latestStatus);

  const courierName =
    courierNames[courier] || courier.toUpperCase();

  document.getElementById('infoCard').innerHTML = `
    <div class="info-header">
      <div>
        <div class="info-courier">${courierName}</div>
        <div class="info-resi">${resi.toUpperCase()}</div>
      </div>
      <div class="status-badge ${statusClass}">
        ${statusLabel}
      </div>
    </div>
  `;

  const tl = document.getElementById('timeline');

  if (history.length === 0) {
    tl.innerHTML =
      '<div>Belum ada riwayat pengiriman.</div>';
  } else {
    tl.innerHTML = history.map((h, i) => `
      <div class="tl-item">
        <div class="tl-dot ${i === 0 ? 'current' : 'old'}">
          ${i === 0 ? '●' : '○'}
        </div>
        <div class="tl-content">
          <div class="tl-desc">
            ${h.desc || h.status || '-'}
          </div>
          ${h.location
            ? `<div class="tl-loc">📍 ${h.location}</div>`
            : ''}
          <div class="tl-time">
            ${h.date || ''} ${h.time || ''}
          </div>
        </div>
      </div>
    `).join('');
  }

  document.getElementById('result')
    .classList.add('show');
}

// Enter key support
document
  .getElementById('resiInput')
  .addEventListener('keydown', e => {
    if (e.key === 'Enter')
      trackPackage();
  });
</script>
