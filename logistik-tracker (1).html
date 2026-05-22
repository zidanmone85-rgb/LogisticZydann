<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TrackID — Pelacak Logistik Indonesia</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0e1a;
    --bg2: #111827;
    --bg3: #1a2236;
    --border: rgba(255,255,255,0.08);
    --border2: rgba(255,255,255,0.15);
    --text: #f0f4ff;
    --muted: #8892a4;
    --accent: #3b82f6;
    --accent2: #06b6d4;
    --success: #10b981;
    --warn: #f59e0b;
    --danger: #ef4444;
    --delivered: #10b981;
    --transit: #3b82f6;
    --pending: #f59e0b;
    --radius: 12px;
    --radius-sm: 8px;
  }

  body {
    font-family: 'Space Grotesk', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Background grid */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(59,130,246,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(59,130,246,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container { max-width: 900px; margin: 0 auto; padding: 0 20px; position: relative; z-index: 1; }

  /* Header */
  header {
    padding: 28px 0 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 22px;
    font-weight: 700;
    letter-spacing: -0.5px;
  }

  .logo-icon {
    width: 38px; height: 38px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px;
  }

  .logo span { color: var(--accent2); }

  .badge-live {
    display: flex; align-items: center; gap: 6px;
    font-size: 12px; color: var(--success);
    background: rgba(16,185,129,0.1);
    border: 1px solid rgba(16,185,129,0.2);
    padding: 4px 10px; border-radius: 20px;
    font-weight: 500;
  }

  .badge-live::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--success);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(1.3); }
  }

  /* Hero */
  .hero {
    text-align: center;
    padding: 60px 0 40px;
  }

  .hero h1 {
    font-size: clamp(28px, 5vw, 46px);
    font-weight: 700;
    letter-spacing: -1px;
    line-height: 1.15;
    margin-bottom: 14px;
    background: linear-gradient(135deg, #fff 0%, #a5b4fc 60%, var(--accent2) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero p {
    color: var(--muted);
    font-size: 16px;
    max-width: 480px;
    margin: 0 auto 32px;
    line-height: 1.6;
  }

  /* Kurir chips */
  .couriers-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin-bottom: 36px;
  }

  .courier-chip {
    padding: 5px 14px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.3px;
    border: 1px solid;
    transition: all 0.2s;
    cursor: default;
  }

  .cc-sicepat  { color: #ff4d00; background: rgba(255,77,0,0.08); border-color: rgba(255,77,0,0.25); }
  .cc-jne      { color: #e31e24; background: rgba(227,30,36,0.08); border-color: rgba(227,30,36,0.25); }
  .cc-jnt      { color: #f7941d; background: rgba(247,148,29,0.08); border-color: rgba(247,148,29,0.25); }
  .cc-anteraja { color: #00aeef; background: rgba(0,174,239,0.08); border-color: rgba(0,174,239,0.25); }
  .cc-pos      { color: #e4002b; background: rgba(228,0,43,0.08); border-color: rgba(228,0,43,0.25); }
  .cc-ninja    { color: #ee4d2d; background: rgba(238,77,45,0.08); border-color: rgba(238,77,45,0.25); }
  .cc-tiki     { color: #ffd700; background: rgba(255,215,0,0.08); border-color: rgba(255,215,0,0.25); }
  .cc-rpx      { color: #4ade80; background: rgba(74,222,128,0.08); border-color: rgba(74,222,128,0.25); }
  .cc-sap      { color: #c084fc; background: rgba(192,132,252,0.08); border-color: rgba(192,132,252,0.25); }
  .cc-wahana   { color: #60a5fa; background: rgba(96,165,250,0.08); border-color: rgba(96,165,250,0.25); }
  .cc-idexpress{ color: #fb923c; background: rgba(251,146,60,0.08); border-color: rgba(251,146,60,0.25); }
  .cc-lion     { color: #f472b6; background: rgba(244,114,182,0.08); border-color: rgba(244,114,182,0.25); }

  /* Search box */
  .search-card {
    background: var(--bg2);
    border: 1px solid var(--border2);
    border-radius: 16px;
    padding: 24px;
    margin-bottom: 40px;
    position: relative;
    overflow: hidden;
  }

  .search-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent), var(--accent2), transparent);
  }

  .search-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }

  .input-wrap {
    position: relative;
    flex: 1 1 200px;
  }

  .input-icon {
    position: absolute;
    left: 14px; top: 50%;
    transform: translateY(-50%);
    color: var(--muted);
    font-size: 16px;
    pointer-events: none;
  }

  input[type="text"], select {
    width: 100%;
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    color: var(--text);
    font-family: inherit;
    font-size: 14px;
    padding: 12px 14px 12px 38px;
    outline: none;
    transition: border-color 0.2s, box-shadow 0.2s;
  }

  select { padding-left: 14px; cursor: pointer; appearance: none; }

  .select-wrap { position: relative; flex: 1 1 160px; }
  .select-wrap::after {
    content: '▾';
    position: absolute;
    right: 12px; top: 50%;
    transform: translateY(-50%);
    color: var(--muted);
    pointer-events: none;
    font-size: 12px;
  }

  input:focus, select:focus {
    border-color: var(--accent);
    box-shadow: 0 0 0 3px rgba(59,130,246,0.12);
  }

  input::placeholder { color: var(--muted); }
  select option { background: var(--bg3); color: var(--text); }

  .btn-track {
    padding: 12px 28px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    border: none;
    border-radius: var(--radius-sm);
    color: #fff;
    font-family: inherit;
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s;
    white-space: nowrap;
    letter-spacing: 0.3px;
  }

  .btn-track:hover { filter: brightness(1.12); transform: translateY(-1px); }
  .btn-track:active { transform: translateY(0); }
  .btn-track:disabled { opacity: 0.5; cursor: not-allowed; transform: none; }

  /* Loading */
  .loading {
    display: none;
    text-align: center;
    padding: 48px;
  }

  .loading.show { display: block; }

  .spinner {
    width: 40px; height: 40px;
    border: 3px solid var(--border);
    border-top-color: var(--accent);
    border-radius: 50%;
    margin: 0 auto 16px;
    animation: spin 0.8s linear infinite;
  }

  @keyframes spin { to { transform: rotate(360deg); } }

  .loading p { color: var(--muted); font-size: 14px; }

  /* Error */
  .error-box {
    display: none;
    background: rgba(239,68,68,0.08);
    border: 1px solid rgba(239,68,68,0.2);
    border-radius: var(--radius);
    padding: 16px 20px;
    color: #fca5a5;
    margin-bottom: 24px;
    font-size: 14px;
    line-height: 1.5;
  }

  .error-box.show { display: block; }

  /* Result */
  .result { display: none; }
  .result.show { display: block; animation: fadeUp 0.4s ease; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Info card */
  .info-card {
    background: var(--bg2);
    border: 1px solid var(--border2);
    border-radius: 16px;
    padding: 22px 24px;
    margin-bottom: 20px;
    position: relative;
    overflow: hidden;
  }

  .info-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 16px;
    flex-wrap: wrap;
  }

  .info-courier {
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 4px;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: 600;
  }

  .info-resi {
    font-family: 'JetBrains Mono', monospace;
    font-size: 18px;
    font-weight: 500;
    color: var(--text);
    letter-spacing: 1px;
  }

  .status-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 600;
    white-space: nowrap;
  }

  .status-delivered { background: rgba(16,185,129,0.15); color: #34d399; border: 1px solid rgba(16,185,129,0.25); }
  .status-transit   { background: rgba(59,130,246,0.15); color: #60a5fa; border: 1px solid rgba(59,130,246,0.25); }
  .status-pending   { background: rgba(245,158,11,0.15); color: #fbbf24; border: 1px solid rgba(245,158,11,0.25); }
  .status-unknown   { background: rgba(139,148,158,0.15); color: #94a3b8; border: 1px solid rgba(139,148,158,0.25); }

  .info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 16px;
    margin-top: 20px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
  }

  .info-item label {
    display: block;
    font-size: 11px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 4px;
    font-weight: 600;
  }

  .info-item p {
    font-size: 14px;
    color: var(--text);
    font-weight: 500;
    line-height: 1.4;
  }

  /* Timeline */
  .timeline-card {
    background: var(--bg2);
    border: 1px solid var(--border2);
    border-radius: 16px;
    padding: 22px 24px;
    margin-bottom: 28px;
  }

  .timeline-title {
    font-size: 14px;
    font-weight: 600;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 20px;
  }

  .timeline {
    position: relative;
  }

  .timeline::before {
    content: '';
    position: absolute;
    left: 15px; top: 0; bottom: 0;
    width: 1px;
    background: linear-gradient(to bottom, var(--accent), transparent);
    opacity: 0.3;
  }

  .tl-item {
    display: flex;
    gap: 16px;
    margin-bottom: 0;
    position: relative;
    padding-bottom: 24px;
  }

  .tl-item:last-child { padding-bottom: 0; }

  .tl-dot {
    width: 32px; height: 32px;
    border-radius: 50%;
    flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
    font-size: 14px;
    border: 2px solid;
    background: var(--bg);
    position: relative;
    z-index: 1;
  }

  .tl-dot.active {
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    border-color: transparent;
    box-shadow: 0 0 16px rgba(59,130,246,0.4);
  }

  .tl-dot.done { border-color: var(--success); color: var(--success); }
  .tl-dot.current { border-color: var(--accent); color: var(--accent); }
  .tl-dot.old { border-color: var(--border2); color: var(--muted); }

  .tl-content { flex: 1; padding-top: 4px; }

  .tl-desc {
    font-size: 14px;
    font-weight: 500;
    color: var(--text);
    line-height: 1.5;
    margin-bottom: 4px;
  }

  .tl-desc.dim { color: var(--muted); font-weight: 400; }

  .tl-loc {
    font-size: 12px;
    color: var(--muted);
    display: flex; align-items: center; gap: 4px;
  }

  .tl-time {
    font-size: 12px;
    color: var(--muted);
    white-space: nowrap;
    font-family: 'JetBrains Mono', monospace;
    margin-top: 2px;
  }

  /* Hint */
  .hint {
    text-align: center;
    padding: 32px 0 48px;
    color: var(--muted);
    font-size: 13px;
    line-height: 1.8;
  }

  .hint strong { color: var(--text); font-weight: 500; }

  /* Empty state */
  .empty-state {
    text-align: center;
    padding: 60px 20px;
    color: var(--muted);
  }

  .empty-icon { font-size: 48px; margin-bottom: 16px; opacity: 0.4; }
  .empty-state h3 { font-size: 18px; color: var(--text); margin-bottom: 8px; font-weight: 500; }
  .empty-state p { font-size: 14px; line-height: 1.6; }

  footer {
    text-align: center;
    padding: 24px 0;
    color: var(--muted);
    font-size: 12px;
    border-top: 1px solid var(--border);
    margin-top: 40px;
  }

  .progress-bar {
    height: 4px;
    background: var(--border);
    border-radius: 4px;
    margin-top: 16px;
    overflow: hidden;
  }

  .progress-fill {
    height: 100%;
    border-radius: 4px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    transition: width 0.6s ease;
  }

  @media (max-width: 600px) {
    .hero h1 { font-size: 26px; }
    .info-resi { font-size: 15px; }
    .tl-time { display: none; }
  }
</style>
</head>
<body>

<div class="container">

  <header>
    <div class="logo">
      <div class="logo-icon">📦</div>
      Track<span>ID</span>
    </div>
    <div class="badge-live">Real-time</div>
  </header>

  <section class="hero">
    <h1>Lacak Paket Anda<br>di Seluruh Indonesia</h1>
    <p>Pantau status pengiriman dari semua ekspedisi besar Indonesia dalam satu platform.</p>

    <div class="couriers-row">
      <span class="courier-chip cc-sicepat">SiCepat</span>
      <span class="courier-chip cc-jne">JNE</span>
      <span class="courier-chip cc-jnt">J&T Express</span>
      <span class="courier-chip cc-anteraja">Anteraja</span>
      <span class="courier-chip cc-pos">Pos Indonesia</span>
      <span class="courier-chip cc-ninja">Ninja Xpress</span>
      <span class="courier-chip cc-tiki">TIKI</span>
      <span class="courier-chip cc-rpx">RPX</span>
      <span class="courier-chip cc-sap">SAP</span>
      <span class="courier-chip cc-wahana">Wahana</span>
      <span class="courier-chip cc-idexpress">ID Express</span>
      <span class="courier-chip cc-lion">Lion Parcel</span>
    </div>

    <div class="search-card">
      <div class="search-row">
        <div class="select-wrap">
          <select id="courierSelect">
            <option value="">— Pilih Ekspedisi —</option>
            <option value="sicepat">SiCepat</option>
            <option value="jne">JNE</option>
            <option value="jnt">J&T Express</option>
            <option value="anteraja">Anteraja</option>
            <option value="pos">Pos Indonesia</option>
            <option value="ninja">Ninja Xpress</option>
            <option value="tiki">TIKI</option>
            <option value="rpx">RPX</option>
            <option value="sap">SAP</option>
            <option value="wahana">Wahana</option>
            <option value="idexpress">ID Express</option>
            <option value="lion">Lion Parcel</option>
            <option value="paxel">Paxel</option>
            <option value="ncs">NCS</option>
            <option value="sentral">Sentral Cargo</option>
            <option value="lazada">Lazada Express</option>
            <option value="shopee">Shopee Express</option>
            <option value="grab">Grab Express</option>
            <option value="gosend">GoSend</option>
          </select>
        </div>

        <div class="input-wrap" style="flex: 2 1 240px;">
          <span class="input-icon">🔍</span>
          <input type="text" id="resiInput" placeholder="Masukkan nomor resi..." autocomplete="off" />
        </div>

        <button class="btn-track" id="trackBtn" onclick="trackPackage()">
          Lacak Paket
        </button>
      </div>

      <div id="progressBar" class="progress-bar" style="display:none;">
        <div class="progress-fill" id="progressFill" style="width:0%"></div>
      </div>
    </div>
  </section>

  <!-- Loading -->
  <div class="loading" id="loading">
    <div class="spinner"></div>
    <p id="loadingText">Menghubungi server ekspedisi...</p>
  </div>

  <!-- Error -->
  <div class="error-box" id="errorBox"></div>

  <!-- Result -->
  <div class="result" id="result">

    <div class="info-card" id="infoCard">
      <!-- dinamis -->
    </div>

    <div class="timeline-card" id="timelineCard">
      <div class="timeline-title">📍 Riwayat Pengiriman</div>
      <div class="timeline" id="timeline"></div>
    </div>

  </div>

  <!-- Hint -->
  <div class="hint" id="hintBox">
    <strong>Tips:</strong> Pilih ekspedisi terlebih lalu masukkan nomor resi Anda.<br>
    Contoh resi SiCepat: <code style="font-family:monospace; font-size:12px; background:rgba(255,255,255,0.05); padding:2px 6px; border-radius:4px;">000912345678901</code>
  </div>

</div>

<footer>
  <div class="container">
    TrackID &mdash; Layanan pelacakan logistik seluruh Indonesia &bull; Didukung oleh BinderByte API
  </div>
</footer>

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
  if (pct >= 100) setTimeout(() => { bar.style.display = 'none'; fill.style.width = '0%'; }, 600);
}

async function trackPackage() {
  const courier = document.getElementById('courierSelect').value;
  const resi = document.getElementById('resiInput').value.trim();

  if (!courier) return showError('Silakan pilih ekspedisi terlebih dahulu.');
  if (!resi) return showError('Masukkan nomor resi yang ingin dilacak.');

  // Reset
  document.getElementById('errorBox').classList.remove('show');
  document.getElementById('result').classList.remove('show');
  document.getElementById('hintBox').style.display = 'none';
  document.getElementById('trackBtn').disabled = true;
  document.getElementById('loading').classList.add('show');

  setProgress(20);
  document.getElementById('loadingText').textContent = 'Menghubungi server ' + courierNames[courier] + '...';

  setTimeout(() => setProgress(60), 400);

  try {
    const url = `https://api.binderbyte.com/v1/track?api_key=${API_KEY}&courier=${courier}&awb=${encodeURIComponent(resi)}`;

    let res, data;
    try {
      res = await fetchWithProxy(url);
    } catch(netErr) {
      setProgress(100);
      document.getElementById('loading').classList.remove('show');
      document.getElementById('trackBtn').disabled = false;
      showError('Gagal terhubung ke server. Periksa koneksi internet Anda, atau coba buka website ini melalui server (bukan file lokal).');
      document.getElementById('hintBox').style.display = 'block';
      return;
    }

    try {
      data = await res.json();
    } catch(e) {
      setProgress(100);
      document.getElementById('loading').classList.remove('show');
      document.getElementById('trackBtn').disabled = false;
      showError('Server mengembalikan respons yang tidak valid. Coba lagi beberapa saat.');
      return;
    }

    setProgress(100);
    document.getElementById('loading').classList.remove('show');
    document.getElementById('trackBtn').disabled = false;

    // Tampilkan pesan error asli dari API supaya lebih informatif
    if (data.status !== 200 || !data.data) {
      let msg = data.message || 'Nomor resi tidak ditemukan.';
      if (msg.toLowerCase().includes('api key')) {
        msg = 'API Key tidak valid atau kuota habis. Silakan cek dashboard BinderByte Anda di binderbyte.com';
      } else if (msg.toLowerCase().includes('not found') || msg.toLowerCase().includes('tidak ditemukan')) {
        msg = 'Nomor resi tidak ditemukan di ekspedisi ' + (courierNames[courier] || courier) + '. Pastikan resi dan ekspedisi sudah benar.';
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
  const latestStatus = summary.status || (history[0] && history[0].status) || 'Dalam Proses';
  const statusClass = getStatusClass(latestStatus);
  const statusLabel = getStatusLabel(latestStatus);
  const courierName = courierNames[courier] || courier.toUpperCase();

  // Info card
  document.getElementById('infoCard').innerHTML = `
    <div class="info-header">
      <div>
        <div class="info-courier">${courierName}</div>
        <div class="info-resi">${resi.toUpperCase()}</div>
      </div>
      <div class="status-badge ${statusClass}">${statusLabel}</div>
    </div>
    <div class="info-grid">
      ${summary.shipper ? `<div class="info-item"><label>Pengirim</label><p>${summary.shipper}</p></div>` : ''}
      ${summary.receiver ? `<div class="info-item"><label>Penerima</label><p>${summary.receiver}</p></div>` : ''}
      ${summary.origin ? `<div class="info-item"><label>Asal</label><p>${summary.origin}</p></div>` : ''}
      ${summary.destination ? `<div class="info-item"><label>Tujuan</label><p>${summary.destination}</p></div>` : ''}
      ${summary.description ? `<div class="info-item"><label>Deskripsi</label><p>${summary.description}</p></div>` : ''}
      ${summary.date ? `<div class="info-item"><label>Tanggal Kirim</label><p>${summary.date}</p></div>` : ''}
      ${summary.weight ? `<div class="info-item"><label>Berat</label><p>${summary.weight}</p></div>` : ''}
      ${summary.service ? `<div class="info-item"><label>Layanan</label><p>${summary.service}</p></div>` : ''}
    </div>
  `;

  // Timeline
  const tl = document.getElementById('timeline');
  if (history.length === 0) {
    tl.innerHTML = `<div style="color:var(--muted); font-size:14px;">Belum ada riwayat pengiriman.</div>`;
  } else {
    tl.innerHTML = history.map((h, i) => {
      const isFirst = i === 0;
      const dotClass = isFirst ? 'current' : 'old';
      const descClass = isFirst ? '' : 'dim';
      return `
        <div class="tl-item">
          <div class="tl-dot ${dotClass}">${isFirst ? '●' : '○'}</div>
          <div class="tl-content">
            <div class="tl-desc ${descClass}">${h.desc || h.status || '-'}</div>
            ${h.location ? `<div class="tl-loc">📍 ${h.location}</div>` : ''}
            <div class="tl-time">${h.date || ''} ${h.time || ''}</div>
          </div>
        </div>
      `;
    }).join('');
  }

  document.getElementById('result').classList.add('show');
}

// Enter key support
document.getElementById('resiInput').addEventListener('keydown', e => {
  if (e.key === 'Enter') trackPackage();
});
</script>

</body>
</html>
