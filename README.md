# Muhammaddwiadipangestu
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Biodata - M. Dwi Adi Pangestu</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* --- CORE STYLES --- */
        :root {
            --bg-primary: #ffffff;
            --bg-secondary: #f9fafb;
            --text-dark: #111827;
            --text-light: #6b7280;
            --accent-blue: #0ea5e9;
            --border-gray: #f3f4f6;
            --shadow-sm: 0 1px 2px rgba(0,0,0,0.05);
            --shadow-md: 0 4px 6px -1px rgba(0,0,0,0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-dark);
            line-height: 1.5;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 480px; /* Lebar maksimal seukuran HP portrait */
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- HEADER --- */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(8px);
            z-index: 1000;
            border-bottom: 1px solid var(--border-gray);
        }

        nav {
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .logo {
            font-weight: 700;
            font-size: 18px;
            letter-spacing: 1px;
        }

        .logo span { color: var(--accent-blue); }

        /* --- HERO SECTION --- */
        .hero {
            padding: 100px 0 40px 0;
            text-align: center;
        }

        .profile-wrapper {
            margin-bottom: 20px;
        }

        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid var(--bg-secondary);
            box-shadow: var(--shadow-md);
            object-fit: cover;
        }

        .badge-class {
            background: #e0f2fe;
            color: var(--accent-blue);
            font-size: 12px;
            font-weight: 600;
            padding: 4px 12px;
            border-radius: 20px;
            display: inline-block;
            margin-bottom: 10px;
        }

        h1 {
            font-size: 24px;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 8px;
            padding: 0 10px;
        }

        .hero p {
            font-size: 14px;
            color: var(--text-light);
            font-weight: 400;
        }

        /* --- INFO BOX --- */
        .section-card {
            background: var(--bg-secondary);
            border-radius: 16px;
            padding: 20px;
            margin-bottom: 25px;
            border: 1px solid var(--border-gray);
        }

        .section-title {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-list {
            font-size: 13px;
        }

        .info-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 8px;
            border-bottom: 1px dotted #e5e7eb;
        }

        .info-item span:first-child { color: var(--text-light); }
        .info-item span:last-child { font-weight: 500; text-align: right; }

        /* --- GAMES SECTION --- */
        .game-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
        }

        .game-card {
            background: white;
            padding: 10px;
            border-radius: 12px;
            text-align: center;
            font-size: 10px;
            font-weight: 600;
            border: 1px solid var(--border-gray);
            box-shadow: var(--shadow-sm);
        }

        .game-card i {
            display: block;
            font-size: 20px;
            color: var(--accent-blue);
            margin-bottom: 5px;
        }

        .game-id-box {
            margin-top: 15px;
            background: #f1f5f9;
            padding: 10px;
            border-radius: 10px;
            font-size: 12px;
        }

        /* --- BUTTONS --- */
        .contact-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-top: 20px;
        }

        .btn-contact {
            width: 100%;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 14px;
            transition: 0.2s;
        }

        .btn-wa { background: #25d366; color: white; }
        .btn-ig { background: #ffffff; color: #e1306c; border: 1px solid #e1306c; }

        /* --- FOOTER --- */
        footer {
            text-align: center;
            padding: 40px 0;
            font-size: 11px;
            color: var(--text-light);
        }

    </style>
</head>
<body>

    <header>
        <nav>
            <div class="logo">M. <span>DWI</span> ADI P.</div>
        </nav>
    </header>

    <div class="container">
        
        <section class="hero">
            <div class="profile-wrapper">
                <img src="https://via.placeholder.com/150" alt="M. Dwi Adi Pangestu" class="profile-img">
            </div>
            <div class="badge-class">9 THOIF • SMP IT Mutiara Global</div>
            <h1>Muhammad Dwi <br>Adi Pangestu</h1>
            <p>Kepala OSIS Divisi Sosial (2025/2026)</p>
        </section>

        <div class="section-card">
            <h2 class="section-title"><i class="fas fa-user"></i> Data Pribadi</h2>
            <div class="info-list">
                <div class="info-item">
                    <span>Lahir di</span>
                    <span>Pekanbaru</span>
                </div>
                <div class="info-item">
                    <span>Tanggal Lahir</span>
                    <span>26 Maret 2011</span>
                </div>
                <div class="info-item">
                    <span>Minat Utama</span>
                    <span>Sains & Teknologi</span>
                </div>
                <div class="info-item">
                    <span>Hobi</span>
                    <span>Coding & Gaming</span>
                </div>
            </div>
        </div>

        <div class="section-card">
            <h2 class="section-title"><i class="fas fa-gamepad"></i> Koleksi Game</h2>
            <div class="game-grid">
                <div class="game-card"><i class="fas fa-mobile-alt"></i> MLBB</div>
                <div class="game-card"><i class="fas fa-gun"></i> PUBG</div>
                <div class="game-card"><i class="fas fa-fire"></i> FF</div>
                <div class="game-card"><i class="fas fa-shield-alt"></i> COC</div>
                <div class="game-card"><i class="fas fa-cube"></i> Minecraft</div>
                <div class="game-card"><i class="fas fa-robot"></i> Roblox</div>
                <div class="game-card"><i class="fas fa-bus"></i> BUSSID</div>
                <div class="game-card"><i class="fas fa-plane"></i> RFS</div>
                <div class="game-card"><i class="fas fa-cloud"></i> Aerofly</div>
            </div>
            <div class="game-id-box">
                <p><strong>FF ID:</strong> 2092978297</p>
                <p><strong>Roblox User:</strong> Dwi0823</p>
            </div>
        </div>

        <div class="section-card">
            <h2 class="section-title"><i class="fas fa-paper-plane"></i> Mari Terhubung</h2>
            <div class="contact-group">
                <a href="https://wa.me/628566655594" class="btn-contact btn-wa">
                    <i class="fab fa-whatsapp"></i> Chat WhatsApp
                </a>
                <a href="https://www.instagram.com/hmmm__dwzz?igsh=ZnVvcWRkOXY5N3pz" class="btn-contact btn-ig">
                    <i class="fab fa-instagram"></i> Follow Instagram
                </a>
            </div>
        </div>

        <footer>
            <p>&copy; 2026 M. Dwi Adi Pangestu<br>Dibuat dengan semangat untuk SMP IT Mutiara Global</p>
        </footer>

    </div>

</body>
</html>

