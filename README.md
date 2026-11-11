<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rise of Kingdoms Hub - Panduan, Kalkulator & Aliansi</title>
    <style>
        :root {
            --bg-dark: #0f141e;
            --bg-card: #1a2234;
            --bg-accent: #232d45;
            --gold: #f1c40f;
            --gold-hover: #d4ac0d;
            --red-accent: #e74c3c;
            --text-main: #f4f6f9;
            --text-muted: #a0aab8;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: var(--bg-dark); color: var(--text-main); line-height: 1.6; }
        
        /* Header & Hero */
        header {
            background: linear-gradient(135deg, #16213e 0%, #0f141e 100%);
            text-align: center;
            padding: 50px 20px;
            border-bottom: 3px solid var(--gold);
        }
        header h1 { color: var(--gold); font-size: 2.4rem; letter-spacing: 1px; margin-bottom: 10px; text-transform: uppercase; }
        header p { color: var(--text-muted); max-width: 600px; margin: 0 auto 20px auto; }
        .badge { background-color: var(--red-accent); color: #fff; padding: 5px 12px; border-radius: 20px; font-size: 0.85rem; font-weight: bold; }

        /* Navigation */
        nav { background-color: var(--bg-card); position: sticky; top: 0; z-index: 100; border-bottom: 1px solid #2c3852; display: flex; justify-content: center; flex-wrap: wrap; }
        nav a { color: var(--text-main); text-decoration: none; padding: 15px 20px; font-weight: 600; transition: 0.3s; }
        nav a:hover { color: var(--gold); background-color: var(--bg-accent); }

        /* Main Container */
        .container { max-width: 1000px; margin: 30px auto; padding: 0 20px; }
        section { margin-bottom: 50px; }
        h2 { color: var(--gold); border-left: 5px solid var(--gold); padding-left: 12px; margin-bottom: 20px; font-size: 1.6rem; }

        /* Filter Buttons */
        .filter-group { margin-bottom: 20px; display: flex; gap: 10px; flex-wrap: wrap; }
        .btn-filter { background: var(--bg-card); color: var(--text-main); border: 1px solid #344363; padding: 8px 16px; border-radius: 6px; cursor: pointer; font-weight: bold; }
        .btn-filter.active, .btn-filter:hover { background: var(--gold); color: #000; border-color: var(--gold); }

        /* Grid & Cards */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .card { background-color: var(--bg-card); padding: 20px; border-radius: 10px; border: 1px solid #2a364f; transition: transform 0.2s; }
        .card:hover { transform: translateY(-4px); border-color: var(--gold); }
        .card h3 { color: #fff; margin-bottom: 8px; display: flex; justify-content: space-between; align-items: center; }
        .tag { font-size: 0.75rem; padding: 3px 8px; border-radius: 4px; background: var(--bg-accent); color: var(--gold); }
        .card p { color: var(--text-muted); font-size: 0.95rem; margin-bottom: 12px; }
        .pairing { font-size: 0.85rem; color: #5dade2; font-weight: bold; }

        /* Speedup Calculator */
        .calc-box { background-color: var(--bg-card); padding: 25px; border-radius: 10px; border: 1px solid #2a364f; }
        .calc-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; margin-bottom: 20px; }
        .input-group label { display: block; margin-bottom: 5px; font-size: 0.9rem; color: var(--text-muted); }
        .input-group input { width: 100%; padding: 10px; border-radius: 6px; border: 1px solid #3c4b6e; background: var(--bg-dark); color: #fff; font-size: 1rem; }
        .btn-primary { background-color: var(--gold); color: #000; border: none; padding: 12px 24px; border-radius: 6px; font-weight: bold; cursor: pointer; font-size: 1rem; width: 100%; }
        .btn-primary:hover { background-color: var(--gold-hover); }
        .result-box { margin-top: 20px; padding: 15px; background: var(--bg-accent); border-radius: 8px; text-align: center; font-size: 1.2rem; font-weight: bold; color: var(--gold); display: none; }

        /* Redeem Codes */
        .code-item { display: flex; justify-content: space-between; align-items: center; background: var(--bg-card); padding: 15px 20px; border-radius: 8px; margin-bottom: 10px; border: 1px solid #2a364f; }
        .code-text { font-family: monospace; font-size: 1.2rem; color: var(--gold); font-weight: bold; }
        .btn-copy { background: var(--bg-accent); color: #fff; border: 1px solid var(--gold); padding: 6px 14px; border-radius: 5px; cursor: pointer; }
        .btn-copy:hover { background: var(--gold); color: #000; }

        /* Alliance Box */
        .alliance-box { background: linear-gradient(135deg, #1f2b44 0%, #16213e 100%); padding: 30px; border-radius: 10px; text-align: center; border: 1px solid var(--gold); }
        .alliance-box h3 { font-size: 1.5rem; margin-bottom: 10px; color: #fff; }

        footer { text-align: center; padding: 25px; background-color: var(--bg-card); color: var(--text-muted); font-size: 0.9rem; border-top: 1px solid #2a364f; }
    </style>
</head>
<body>

<header>
    <span class="badge">PORTAL KOMUNITAS & PANDUAN</span>
    <h1>Rise of Kingdoms Hub</h1>
    <p>Pusat informasi build komandan terbaik, kalkulator speedup KvK, dan informasi aliansi resmi.</p>
</header>

<nav>
    <a href="#komandan">Komandan</a>
    <a href="#kalkulator">Kalkulator Speedup</a>
    <a href="#redeem">Kode Redeem</a>
    <a href="#aliansi">Info Aliansi</a>
</nav>

<div class="container">

    <!-- Bagian Komandan -->
    <section id="komandan">
        <h2>Panduan Komandan Meta</h2>
        <div class="filter-group">
            <button class="btn-filter active" onclick="filterCmd('all', this)">Semua</button>
            <button class="btn-filter" onclick="filterCmd('infanteri', this)">Infanteri</button>
            <button class="btn-filter" onclick="filterCmd('kavaleri', this)">Kavaleri</button>
            <button class="btn-filter" onclick="filterCmd('pemanah', this)">Pemanah</button>
        </div>

        <div class="grid" id="cmd-list">
            <div class="card cmd-card" data-type="infanteri">
                <h3>Sun Tzu <span class="tag">Epik • Infanteri</span></h3>
                <p>Komandan terbaik untuk pemain F2P. Memberikan damage area (AoE) tinggi dan regenerasi rage cepat untuk pertahanan maupun open field.</p>
                <div class="pairing">Pasangan Terbaik: Bjorn Ironside / Martel</div>
            </div>

            <div class="card cmd-card" data-type="infanteri">
                <h3>Scipio Africanus Prime <span class="tag">Legendaris • Infanteri</span></h3>
                <p>Raja pertempuran terbuka dengan damage AoE besar, pengurangan health musuh, serta shield pertahanan yang sangat tebal.</p>
                <div class="pairing">Pasangan Terbaik: Liu Che / Guan Yu</div>
            </div>

            <div class="card cmd-card" data-type="kavaleri">
                <h3>Nevsky <span class="tag">Legendaris • Kavaleri</span></h3>
                <p>Komandan kavaleri serba bisa dengan damage single-target mematikan, bonus serangan tinggi, dan peningkatan kecepatan baris.</p>
                <div class="pairing">Pasangan Terbaik: Joan of Arc Prime / Huo Qubing</div>
            </div>

            <div class="card cmd-card" data-type="pemanah">
                <h3>Zhuge Liang <span class="tag">Legendaris • Pemanah</span></h3>
                <p>Memiliki serangan area melingkar 360 derajat yang sangat efektif untuk perang massal di KvK maupun barbarian chaining.</p>
                <div class="pairing">Pasangan Terbaik: Hermann Prime / YSG</div>
            </div>
        </div>
    </section>

    <!-- Bagian Kalkulator Speedup -->
    <section id="kalkulator">
        <h2>Kalkulator Speedup KvK / MGE</h2>
        <div class="calc-box">
            <p style="margin-bottom: 15px; color: var(--text-muted);">Masukkan jumlah item speedup yang Anda miliki di tas untuk menghitung total hari dan jam.</p>
            <div class="calc-grid">
                <div class="input-group">
                    <label>Speedup 5 Menit</label>
                    <input type="number" id="m5" min="0" placeholder="0">
                </div>
                <div class="input-group">
                    <label>Speedup 15 Menit</label>
                    <input type="number" id="m15" min="0" placeholder="0">
                </div>
                <div class="input-group">
                    <label>Speedup 60 Menit (1 Jam)</label>
                    <input type="number" id="m60" min="0" placeholder="0">
                </div>
                <div class="input-group">
                    <label>Speedup 3 Jam</label>
                    <input type="number" id="h3" min="0" placeholder="0">
                </div>
                <div class="input-group">
                    <label>Speedup 8 Jam</label>
                    <input type="number" id="h8" min="0" placeholder="0">
                </div>
                <div class="input-group">
                    <label>Speedup 24 Jam (1 Hari)</label>
                    <input type="number" id="h24" min="0" placeholder="0">
                </div>
            </div>
            <button class="btn-primary" onclick="hitungSpeedup()">Hitung Total Speedup</button>
            <div class="result-box" id="hasil-speedup"></div>
        </div>
    </section>

    <!-- Bagian Kode Redeem -->
    <section id="redeem">
        <h2>Kode Redeem & Cara Klaim</h2>
        <p style="margin-bottom: 15px; color: var(--text-muted);">Cara klaim: Buka Profil di pojok kiri atas &gt; Pengaturan (Settings) &gt; Tukar (Redeem). Kode di bawah ini dapat Anda ubah sesuai pembaruan terbaru:</p>
        
        <div class="code-item">
            <div>
