<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Portofolio - M. Dwi Adi Pangestu</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* --- CORE STYLES --- */
        :root {
            --bg-primary: #ffffff;
            --bg-secondary: #f8fafc;
            --text-dark: #0f172a;
            --text-light: #64748b;
            --accent-blue: #0284c7;
            --accent-light: #e0f2fe;
            --border-gray: #e2e8f0;
            --shadow-sm: 0 2px 4px rgba(0,0,0,0.02);
            --shadow-md: 0 10px 15px -3px rgba(0,0,0,0.05);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        html { scroll-behavior: smooth; }
        body { font-family: 'Poppins', sans-serif; background-color: var(--bg-primary); color: var(--text-dark); line-height: 1.6; overflow-x: hidden; }

        .container { width: 100%; max-width: 500px; margin: 0 auto; padding: 0 20px; }

        /* --- HEADER --- */
        header { position: fixed; top: 0; width: 100%; background: rgba(255, 255, 255, 0.95); backdrop-filter: blur(10px); z-index: 1000; border-bottom: 1px solid var(--border-gray); }
        nav { height: 65px; display: flex; align-items: center; justify-content: center; }
        .logo { font-weight: 700; font-size: 18px; letter-spacing: 1px; color: var(--text-dark); }
        .logo span { color: var(--accent-blue); }

        /* --- HERO SECTION --- */
        .hero { padding: 110px 0 50px 0; text-align: center; background: radial-gradient(circle at top right, #f0f9ff, transparent); border-bottom: 1px solid var(--border-gray); }
        .profile-img { width: 140px; height: 140px; border-radius: 50%; border: 5px solid white; box-shadow: var(--shadow-md); object-fit: cover; margin-bottom: 20px; }
        .badge-class { background: var(--accent-light); color: var(--accent-blue); font-size: 12px; font-weight: 600; padding: 6px 16px; border-radius: 20px; display: inline-block; margin-bottom: 12px; }
        h1 { font-size: 28px; font-weight: 700; line-height: 1.2; margin-bottom: 10px; }
        .hero p { font-size: 14px; color: var(--text-light); }

        /* --- QUOTE SECTION --- */
        .quote-box { background: var(--text-dark); color: white; padding: 25px; border-radius: 16px; text-align: center; margin: -20px auto 30px auto; position: relative; z-index: 10; box-shadow: var(--shadow-md); }
        .quote-box i { color: var(--accent-blue); font-size: 24px; margin-bottom: 10px; }
        .quote-box p { font-style: italic; font-size: 14px; margin-bottom: 10px; line-height: 1.8; }
        .quote-box span { font-size: 12px; color: var(--text-light); font-weight: 600; letter-spacing: 1px; text-transform: uppercase; }

        /* --- CONTENT WRAPPER --- */
        .content-wrapper { padding: 10px 0 40px 0; }

        /* --- SECTION HEADERS --- */
        .section-title { font-size: 18px; font-weight: 700; margin-bottom: 20px; display: flex; align-items: center; gap: 10px; color: var(--text-dark); }
        .section-title i { color: var(--accent-blue); font-size: 20px; background: var(--accent-light); padding: 8px; border-radius: 8px; }

        /* --- CARDS --- */
        .card { background: white; border-radius: 16px; padding: 25px; margin-bottom: 30px; border: 1px solid var(--border-gray); box-shadow: var(--shadow-sm); }
        .text-content { font-size: 14px; color: var(--text-light); text-align: justify; margin-bottom: 15px; }

        /* --- LIST INFO --- */
        .info-list { font-size: 14px; }
        .info-item { display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px dashed var(--border-gray); }
        .info-item:last-child { border-bottom: none; }
        .info-item span:first-child { color: var(--text-light); }
        .info-item span:last-child { font-weight: 600; color: var(--text-dark); text-align: right; }

        /* --- TIMELINE --- */
        .timeline { position: relative; padding-left: 30px; margin-top: 20px; }
        .timeline::before { content: ''; position: absolute; left: 7px; top: 0; bottom: 0; width: 2px; background: var(--accent-light); }
        .timeline-item { position: relative; margin-bottom: 25px; }
        .timeline-item::before { content: ''; position: absolute; left: -30px; top: 5px; width: 16px; height: 16px; border-radius: 50%; background: var(--accent-blue); border: 4px solid white; box-shadow: 0 0 0 2px var(--accent-light); }
        .timeline-date { font-size: 12px; color: var(--accent-blue); font-weight: 600; margin-bottom: 5px; }
        .timeline-title { font-weight: 700; font-size: 15px; margin-bottom: 5px; }
        .timeline-desc { font-size: 13px; color: var(--text-light); }

        /* --- SKILL BARS --- */
        .skill-group { margin-bottom: 15px; }
        .skill-header { display: flex; justify-content: space-between; font-size: 13px; font-weight: 600; margin-bottom: 5px; }
        .skill-bar { height: 8px; background: var(--border-gray); border-radius: 10px; overflow: hidden; }
        .skill-progress { height: 100%; background: var(--accent-blue); border-radius: 10px; }

        /* --- OSIS LIST --- */
        .osis-list { list-style: none; margin-top: 15px; }
        .osis-list li { font-size: 13px; color: var(--text-light); margin-bottom: 10px; display: flex; gap: 10px; align-items: flex-start; }
        .osis-list li i { color: var(--accent-blue); margin-top: 3px; }

        /* --- YOUTUBE & GALLERY --- */
        .video-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 12px; margin-bottom: 15px; border: 1px solid var(--border-gray); }
        .video-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; }
        
        .gallery-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 15px; }
        .gallery-img { width: 100%; height: 120px; border-radius: 10px; object-fit: cover; background: var(--border-gray); border: 1px solid var(--border-gray); }

        /* --- GAMES SECTION --- */
        .game-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-bottom: 20px; }
        .game-card { background: var(--bg-secondary); padding: 15px 5px; border-radius: 12px; text-align: center; font-size: 11px; font-weight: 600; border: 1px solid var(--border-gray); }
        .game-card i { display: block; font-size: 24px; color: var(--accent-blue); margin-bottom: 8px; }
        .guild-box { background: var(--text-dark); color: white; padding: 15px; border-radius: 12px; text-align: center; font-size: 13px; }
        .guild-box span { color: #facc15; font-weight: 700; letter-spacing: 1px; font-size: 15px; display: block; margin-top: 5px;}

        /* --- MUSIC PLAYER MOCKUP --- */
        .music-card { background: var(--bg-secondary); border-radius: 12px; padding: 15px; display: flex; align-items: center; gap: 15px; border: 1px solid var(--border-gray); }
        .music-icon { width: 50px; height: 50px; background: #1DB954; border-radius: 10px; display: flex; align-items: center; justify-content: center; color: white; font-size: 24px; }
        .music-info h4 { font-size: 14px; margin-bottom: 2px; }
        .music-info p { font-size: 12px; color: var(--text-light); }
        .music-wave { margin-left: auto; color: #1DB954; font-size: 18px; }

        /* --- FAQ SECTION --- */
        details { background: var(--bg-secondary); border: 1px solid var(--border-gray); border-radius: 10px; margin-bottom: 10px; overflow: hidden; }
        summary { font-size: 13px; font-weight: 600; padding: 15px; cursor: pointer; list-style: none; display: flex; justify-content: space-between; align-items: center; }
        summary::-webkit-details-marker { display: none; }
        summary::after { content: '\f078'; font-family: 'Font Awesome 5 Free'; font-weight: 900; color: var(--text-light); transition: 0.3s; }
        details[open] summary::after { transform: rotate(180deg); color: var(--accent-blue); }
        .faq-content { padding: 0 15px 15px 15px; font-size: 13px; color: var(--text-light); border-top: 1px dashed var(--border-gray); margin-top: 5px; padding-top: 10px; }

        /* --- BUTTONS --- */
        .contact-group { display: flex; flex-direction: column; gap: 15px; margin-top: 20px; }
        .btn-contact { width: 100%; height: 50px; display: flex; align-items: center; justify-content: center; gap: 10px; border-radius: 12px; font-weight: 600; font-size: 14px; transition: 0.2s; color: white; text-decoration: none; }
        .btn-wa { background: #25d366; }
        .btn-ig { background: #ffffff; color: #e1306c; border: 1px solid #e1306c; }
        .btn-yt { background: #ff0000; }
        
        /* --- FOOTER --- */
        footer { text-align: center; padding: 30px 0 50px 0; font-size: 12px; color: var(--text-light); background: var(--bg-secondary); border-top: 1px solid var(--border-gray); }
    </style>
</head>
<body>

    <header>
        <nav>
            <div class="logo">M. <span>DWI</span> ADI P.</div>
        </nav>
    </header>

    <section class="hero">
        <div class="container">
            <img src="image_0.png" alt="M. Dwi Adi Pangestu" class="profile-img">
            <br>
            <div class="badge-class"><i class="fas fa-graduation-cap"></i> 9 THOIF • SMP IT Mutiara Global</div>
            <h1>Muhammad Dwi <br>Adi Pangestu</h1>
            <p>Pelajar Eksakta | Content Creator | Kepala OSIS</p>
        </div>
    </section>

    <div class="content-wrapper">
        <div class="container">

            <div class="quote-box">
                <i class="fas fa-quote-left"></i>
                <p>"Keseimbangan antara pemikiran logis sains dan imajinasi kreatif digital adalah kunci untuk terus berkembang di masa depan."</p>
                <span>- Dwi Adi Pangestu</span>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-user"></i> Biografi Singkat</h2>
                <p class="text-content">
                    Halo! Saya adalah pelajar yang lahir dan tumbuh di Pekanbaru. Saya sangat menikmati tantangan memecahkan soal-soal eksakta dasar. Di luar jam sekolah, saya gemar menuangkan imajinasi melalui editing video, merancang *prompt* AI, dan aktif dalam keorganisasian siswa.
                </p>
                <div class="info-list">
                    <div class="info-item"><span>Tempat Lahir</span><span>Pekanbaru</span></div>
                    <div class="info-item"><span>Tanggal Lahir</span><span>26 Maret 2011</span></div>
                    <div class="info-item"><span>Fokus Minat</span><span>Sains & Teknologi</span></div>
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-route"></i> Jalur Pendidikan</h2>
                <p class="text-content">Pendidikan adalah fondasi utama saya untuk meraih masa depan di bidang ilmu pengetahuan alam.</p>
                
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-date">Saat Ini (Kelas 9)</div>
                        <div class="timeline-title">SMP IT Mutiara Global</div>
                        <div class="timeline-desc">Fokus pada penyelesaian studi menengah pertama dengan nilai terbaik, mengasah logika dasar, dan aktif menjalankan kewajiban di OSIS.</div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-date">Target Masa Depan</div>
                        <div class="timeline-title">MAN 3</div>
                        <div class="timeline-desc">Melanjutkan pendidikan menengah atas. Bertujuan untuk memperdalam ilmu eksakta sebagai persiapan menuju pendidikan tinggi dan cita-cita utama.</div>
                    </div>
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-users"></i> Kepemimpinan OSIS</h2>
                <p class="text-content">
                    Dipercaya sebagai <strong>Kepala OSIS Divisi Sosial</strong> untuk masa bakti 2025/2026. Peran ini melatih saya untuk menjadi pribadi yang terorganisir dan mampu memimpin rekan satu tim.
                </p>
                <div style="margin-top: 15px; padding-top: 15px; border-top: 1px solid var(--border-gray);">
                    <strong style="font-size: 13px; color: var(--text-dark);">Fokus & Program Kerja:</strong>
                    <ul class="osis-list">
                        <li><i class="fas fa-check-circle"></i> Membangun solidaritas dan kepedulian sosial di lingkungan sekolah.</li>
                        <li><i class="fas fa-check-circle"></i> Merencanakan kegiatan bakti sosial dan penggalangan dana.</li>
                        <li><i class="fas fa-check-circle"></i> Mengelola komunikasi antar siswa untuk menciptakan suasana sekolah yang harmonis.</li>
                    </ul>
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-bolt"></i> Distribusi Keahlian</h2>
                <p class="text-content">Beberapa area yang terus saya pelajari dan kembangkan setiap harinya:</p>
                
                <div class="skill-group">
                    <div class="skill-header"><span>Sains & Eksakta Dasar</span><span>85%</span></div>
                    <div class="skill-bar"><div class="skill-progress" style="width: 85%;"></div></div>
                </div>
                <div class="skill-group">
                    <div class="skill-header"><span>Video Editing (CapCut)</span><span>90%</span></div>
                    <div class="skill-bar"><div class="skill-progress" style="width: 90%;"></div></div>
                </div>
                <div class="skill-group">
                    <div class="skill-header"><span>Manajemen Organisasi</span><span>80%</span></div>
                    <div class="skill-bar"><div class="skill-progress" style="width: 80%;"></div></div>
                </div>
                <div class="skill-group">
                    <div class="skill-header"><span>Digital Image & AI Prompting</span><span>75%</span></div>
                    <div class="skill-bar"><div class="skill-progress" style="width: 75%;"></div></div>
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-video"></i> Kreator Visual</h2>
                <p class="text-content">
                    Saya sangat tertarik dengan seni visual digital. Mulai dari mengedit video secara dinamis menggunakan <strong>CapCut</strong>, melakukan manipulasi foto (photo editing), hingga merancang *prompt* AI bernuansa sinematik.
                </p>

                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/npt-5a-Q5nE" allowfullscreen></iframe>
                </div>

                <a href="https://youtube.com/@dwzz_zz?si=VUzuuWi2W8dYN0_y" target="_blank" class="btn-contact btn-yt" style="margin-bottom: 25px;">
                    <i class="fab fa-youtube"></i> Subscribe Channel Dwzz
                </a>

                <strong style="font-size: 14px; color: var(--text-dark);">Galeri Eksplorasi Digital:</strong>
                <p style="font-size: 12px; color: var(--text-light); margin-bottom: 10px;">Tempat saya memajang hasil photo editing & AI Image.</p>
                <div class="gallery-grid">
                    <img src="https://via.placeholder.com/150/1e293b/ffffff?text=Karya+1" class="gallery-img">
                    <img src="https://via.placeholder.com/150/1e293b/ffffff?text=Karya+2" class="gallery-img">
                    <img src="https://via.placeholder.com/150/1e293b/ffffff?text=Karya+3" class="gallery-img">
                    <img src="https://via.placeholder.com/150/1e293b/ffffff?text=Karya+4" class="gallery-img">
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-gamepad"></i> Zona Gaming</h2>
                <p class="text-content">Game adalah tempat saya melatih strategi, refleks, dan kekompakan tim bersama teman-teman.</p>
                
                <div class="game-grid">
                    <div class="game-card"><i class="fas fa-mobile-alt"></i> MLBB</div>
                    <div class="game-card"><i class="fas fa-crosshairs"></i> PUBG</div>
                    <div class="game-card"><i class="fas fa-fire"></i> FF</div>
                    <div class="game-card"><i class="fas fa-shield-alt"></i> COC</div>
                    <div class="game-card"><i class="fas fa-cube"></i> Minecraft</div>
                    <div class="game-card"><i class="fas fa-cubes"></i> Roblox</div>
                    <div class="game-card"><i class="fas fa-bus"></i> BUSSID</div>
                    <div class="game-card"><i class="fas fa-plane"></i> RFS</div>
                    <div class="game-card"><i class="fas fa-cloud"></i> Aerofly</div>
                </div>

                <div class="guild-box">
                    <i class="fas fa-crown" style="color: #facc15; font-size: 20px; margin-bottom: 5px;"></i>
                    <p>Bagian dari Free Fire Guild:</p>
                    <span>D⁴` NGEL々</span>
                </div>

                <div style="display: flex; gap: 10px; margin-top: 15px;">
                    <div style="flex: 1; background: var(--bg-secondary); padding: 10px; border-radius: 8px; text-align: center; border: 1px solid var(--border-gray);">
                        <p style="font-size: 11px; color: var(--text-light);">Free Fire ID</p>
                        <strong style="font-size: 13px;">2192978297</strong>
                    </div>
                    <div style="flex: 1; background: var(--bg-secondary); padding: 10px; border-radius: 8px; text-align: center; border: 1px solid var(--border-gray);">
                        <p style="font-size: 11px; color: var(--text-light);">Roblox User</p>
                        <strong style="font-size: 13px;">Dwi0823</strong>
                    </div>
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-headphones-alt"></i> Vibe Saat Ini</h2>
                <p class="text-content">Musik yang sering menemani saat saya sedang belajar, *coding*, atau mengedit video.</p>
                
                <div class="music-card">
                    <div class="music-icon"><i class="fab fa-spotify"></i></div>
                    <div class="music-info">
                        <h4>Lofi Study Vibes</h4>
                        <p>Playlist Favorit</p>
                    </div>
                    <div class="music-wave">
                        <i class="fas fa-chart-bar"></i>
                    </div>
                </div>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-comments"></i> Q&A Singkat</h2>
                
                <details>
                    <summary>Kenapa memilih target MAN 3?</summary>
                    <div class="faq-content">
                        Karena MAN 3 merupakan salah satu sekolah unggulan yang sejalan dengan ketertarikan saya pada ilmu pengetahuan dan lingkungan akademik yang mendukung eksplorasi sains.
                    </div>
                </details>
                
                <details>
                    <summary>Aplikasi apa saja yang dipakai untuk editing?</summary>
                    <div class="faq-content">
                        Untuk editing video yang cepat dan dinamis saya mengandalkan CapCut. Sedangkan untuk eksplorasi gambar saya mempelajari berbagai tools berbasis AI.
                    </div>
                </details>

                <details>
                    <summary>Bisa diajak mabar Free Fire?</summary>
                    <div class="faq-content">
                        Sangat bisa! Silakan *add* ID Free Fire saya (2192978297) atau hubungi langsung via DM Instagram atau WhatsApp untuk janjian mabar bareng anak-anak *guild*.
                    </div>
                </details>
            </div>

            <div class="card">
                <h2 class="section-title"><i class="fas fa-paper-plane"></i> Mari Terhubung</h2>
                <p class="text-content" style="text-align: center;">Punya pertanyaan terkait OSIS, minat pada sains, atau mengajak mabar dan ingin sekadar menyapa? Jangan ragu hubungi saya.</p>
                
                <div class="contact-group">
                    <a href="https://wa.me/628566655594" target="_blank" class="btn-contact btn-wa">
                        <i class="fab fa-whatsapp"></i> Chat via WhatsApp
                    </a>
                    <a href="https://www.instagram.com/hmmm__dwzz?igsh=ZnVvcWRkOXY5N3pz" target="_blank" class="btn-contact btn-ig">
                        <i class="fab fa-instagram"></i> Follow Instagram
                    </a>
                </div>
            </div>

        </div>
    </div>

    <footer>
        <div class="container">
            <p>&copy; 2026 M. Dwi Adi Pangestu</p>
            <p style="margin-top: 5px;">SMP IT Mutiara Global (9 THOIF) • Pekanbaru</p>
        </div>
    </footer>

</body>
</html>
