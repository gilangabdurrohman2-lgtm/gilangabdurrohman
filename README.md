<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>PiKIR | Praktisi Kewirausahaan Inovasi Riset</title>
    <meta
      name="description"
      content="PiKIR adalah organisasi yang bergerak di bidang kewirausahaan, inovasi, dan riset untuk menciptakan solusi nyata bagi masyarakat."
    />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <style>
      :root {
        --primary: #0f172a;
        --secondary: #f7b731;
        --dark: #121826;
        --text: #1f2937;
        --muted: #5d6475;
        --light: #f5f7fb;
        --white: #ffffff;
        --soft: #f3f6fb;
        --card-shadow: 0 18px 40px rgba(15, 23, 42, 0.12);
        --border: rgba(15, 23, 42, 0.08);

        --brand-blue: #0e2245;
        --brand-blue-2: #16375a;
        --brand-gold: #f3c54c;
        --brand-gold-2: #dca81f;
        --brand-cream: #fffaf1;
        --brand-cream-2: #fff3d4;
      }

      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      html {
        scroll-behavior: smooth;
      }

      body {
        font-family: "Plus Jakarta Sans", sans-serif;
        background: var(--light);
        color: var(--text);
        line-height: 1.6;
      }

      a {
        text-decoration: none;
      }

      img {
        max-width: 100%;
        display: block;
      }

      button {
        font: inherit;
        cursor: pointer;
      }

      .container {
        width: min(1200px, calc(100% - 32px));
        margin: 0 auto;
      }

      .header {
        position: sticky;
        top: 0;
        z-index: 10;
        background: rgba(255, 255, 255, 0.92);
        backdrop-filter: blur(12px);
        border-bottom: 1px solid var(--border);
      }

      .navbar {
        display: flex;
        align-items: center;
        justify-content: space-between;
        min-height: 80px;
        gap: 20px;
      }

      .logo {
        display: flex;
        align-items: center;
        gap: 10px;
        font-size: 1.1rem;
        font-weight: 800;
        color: var(--dark);
      }

      .logo-mark {
        background: linear-gradient(135deg, var(--brand-gold), var(--brand-gold-2));
        color: var(--brand-blue);
        width: 42px;
        height: 42px;
        border-radius: 50%;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        font-weight: 800;
        box-shadow: 0 10px 18px rgba(247, 183, 49, 0.3);
        border: 3px solid rgba(14, 34, 69, 0.9);
        overflow: hidden;
      }

      .logo-mark svg {
        width: 24px;
        height: 24px;
        display: block;
      }

      .logo-text {
        display: flex;
        align-items: center;
        gap: 0;
        font-weight: 900;
        letter-spacing: -0.04em;
      }

      .logo-text .pi {
        color: var(--brand-blue);
      }

      .logo-text .kir {
        color: var(--brand-blue);
      }

      .nav-menu {
        display: flex;
        align-items: center;
        gap: 20px;
      }

      .nav-menu a {
        color: var(--text);
        font-weight: 600;
        transition: 0.2s ease;
      }

      .nav-menu a:hover {
        color: var(--secondary);
      }

      .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        border-radius: 12px;
        font-weight: 700;
        padding: 12px 22px;
        transition: 0.2s ease;
      }

      .btn-primary {
        background: linear-gradient(135deg, var(--brand-gold), var(--brand-gold-2));
        color: var(--brand-blue);
        box-shadow: 0 14px 24px rgba(247, 183, 49, 0.25);
      }

      .btn-primary:hover {
        transform: translateY(-2px);
      }

      .btn-secondary {
        background: transparent;
        border: 1px solid rgba(15, 23, 42, 0.12);
        color: var(--text);
      }

      .btn-light {
        background: white;
        color: var(--dark);
        border: 1px solid rgba(255, 255, 255, 0.28);
      }

      .hero {
        position: relative;
        background: linear-gradient(135deg, #fef7db 0%, #fffaf0 35%, #f8fafc 100%);
        padding: 90px 0 70px;
        overflow: hidden;
      }

      .hero::before {
        content: "";
        position: absolute;
        inset: 0;
        background:
          radial-gradient(circle at top left, rgba(247, 183, 49, 0.18), transparent 30%),
          radial-gradient(circle at bottom right, rgba(15, 23, 42, 0.08), transparent 35%);
        pointer-events: none;
      }

      .hero-content {
        position: relative;
        z-index: 1;
        display: grid;
        grid-template-columns: 1.2fr 0.8fr;
        gap: 42px;
        align-items: center;
      }

      .eyebrow {
        font-size: 0.78rem;
        font-weight: 800;
        text-transform: uppercase;
        letter-spacing: 0.12em;
        color: var(--brand-blue);
        margin-bottom: 18px;
      }

      .hero-copy h1 {
        font-size: clamp(2.5rem, 4vw, 4.2rem);
        line-height: 1.08;
        color: var(--dark);
        margin-bottom: 18px;
      }

      .subtitle {
        font-size: 1.04rem;
        color: var(--muted);
        max-width: 620px;
      }

      .hero-actions {
        display: flex;
        gap: 14px;
        flex-wrap: wrap;
        margin-top: 28px;
      }

      .stats {
        display: grid;
        grid-template-columns: repeat(3, minmax(120px, 1fr));
        gap: 16px;
        margin-top: 34px;
      }

      .stats > div {
        padding: 18px 16px;
        background: rgba(255, 255, 255, 0.55);
        border: 1px solid rgba(15, 23, 42, 0.06);
        border-radius: 16px;
        box-shadow: 0 10px 18px rgba(15, 23, 42, 0.03);
      }

      .stats strong {
        display: block;
        color: var(--dark);
        font-size: clamp(1.3rem, 2.7vw, 2rem);
      }

      .stats span {
        color: var(--muted);
        font-size: 0.88rem;
      }

      .hero-visual {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 420px;
      }

      .main-card {
        position: relative;
        background: linear-gradient(135deg, #111827, #1f2937);
        color: white;
        border-radius: 28px;
        padding: 30px 28px;
        width: min(100%, 420px);
        box-shadow: var(--card-shadow);
        border: 1px solid rgba(255,255,255,0.08);
      }

      .badge {
        display: inline-block;
        background: rgba(247, 183, 49, 0.2);
        color: #f7d470;
        padding: 8px 12px;
        border-radius: 999px;
        font-size: 0.76rem;
        font-weight: 800;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      .main-card h3 {
        margin-top: 18px;
        font-size: 1.65rem;
        line-height: 1.35;
        margin-bottom: 18px;
      }

      .main-card ul {
        list-style: none;
        display: grid;
        gap: 12px;
        padding-left: 0;
      }

      .main-card li {
        position: relative;
        padding-left: 20px;
        color: rgba(255, 255, 255, 0.85);
      }

      .main-card li::before {
        content: "•";
        position: absolute;
        left: 0;
        color: var(--secondary);
      }

      .floating-card {
        position: absolute;
        right: -10px;
        bottom: 10px;
        background: white;
        border-radius: 18px;
        padding: 18px 18px;
        box-shadow: var(--card-shadow);
        border: 1px solid rgba(15, 23, 42, 0.06);
        min-width: 180px;
      }

      .floating-card .icon {
        width: 52px;
        height: 52px;
        border-radius: 12px;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        background: linear-gradient(135deg, #fef3c7, #facc15);
        font-size: 1.5rem;
        margin-bottom: 10px;
      }

      .floating-card strong {
        display: block;
        font-size: 1.8rem;
        color: var(--dark);
        margin-bottom: 8px;
      }

      .floating-card p {
        color: var(--muted);
        font-size: 0.9rem;
      }

      .section {
        padding: 86px 0;
      }

      .alt {
        background: #eef4ff;
      }

      .section-heading {
        text-align: center;
        margin-bottom: 38px;
      }

      .section-heading h2 {
        font-size: clamp(1.9rem, 3vw, 3rem);
        color: var(--dark);
        margin-top: 10px;
        line-height: 1.2;
      }

      .about-grid,
      .program-grid,
      .portfolio-grid,
      .team-grid {
        display: grid;
        gap: 24px;
      }

      .about-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }

      .about-card,
      .program-card,
      .portfolio-card,
      .team-card {
        background: white;
        border: 1px solid rgba(15, 23, 42, 0.06);
        border-radius: 22px;
        box-shadow: 0 12px 28px rgba(15, 23, 42, 0.05);
        padding: 28px 22px;
      }

      .about-card h3,
      .program-card h3,
      .portfolio-card h3,
      .team-card h3 {
        font-size: 1.3rem;
        color: var(--dark);
        margin-bottom: 12px;
      }

      .about-card p,
      .program-card p,
      .portfolio-card p,
      .team-card p {
        color: var(--muted);
      }

      .program-grid {
        grid-template-columns: repeat(4, minmax(0, 1fr));
      }

      .program-card {
        position: relative;
        padding-top: 22px;
      }

      .icon-box {
        width: 62px;
        height: 62px;
        border-radius: 16px;
        background: linear-gradient(135deg, #fef3c7, #f7b731);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.7rem;
        margin-bottom: 18px;
      }

      .activity-grid {
        display: grid;
        gap: 22px;
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }

      .activity-item {
        overflow: hidden;
        border-radius: 20px;
        background: white;
        border: 1px solid rgba(15, 23, 42, 0.06);
        box-shadow: 0 12px 28px rgba(15, 23, 42, 0.06);
      }

      .activity-image {
        height: 220px;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
      }

      .image-one {
        background: linear-gradient(135deg, rgba(247,183,49,0.35), rgba(15,23,42,0.45)),
          url("https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=900&q=80");
      }

      .image-two {
        background: linear-gradient(135deg, rgba(247,183,49,0.35), rgba(15,23,42,0.45)),
          url("https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=900&q=80");
      }

      .image-three {
        background: linear-gradient(135deg, rgba(247,183,49,0.35), rgba(15,23,42,0.45)),
          url("https://images.unsplash.com/photo-1531482615713-2afd69097998?auto=format&fit=crop&w=900&q=80");
      }

      .image-four {
        background: linear-gradient(135deg, rgba(247,183,49,0.35), rgba(15,23,42,0.45)),
          url("https://images.unsplash.com/photo-1523240795612-9a054b0db644?auto=format&fit=crop&w=900&q=80");
      }

      .image-five {
        background: linear-gradient(135deg, rgba(247,183,49,0.35), rgba(15,23,42,0.45)),
          url("https://images.unsplash.com/photo-1552664730-06b4d7076f8d?auto=format&fit=crop&w=900&q=80");
      }

      .image-six {
        background: linear-gradient(135deg, rgba(247,183,49,0.35), rgba(15,23,42,0.45)),
          url("https://images.unsplash.com/photo-1516321497487-3d1d1c8f6e5d?auto=format&fit=crop&w=900&q=80");
      }

      .activity-content {
        padding: 22px 18px 26px;
      }

      .tag {
        display: inline-block;
        background: #fff6d8;
        color: var(--secondary);
        font-size: 0.72rem;
        font-weight: 800;
        text-transform: uppercase;
        letter-spacing: 0.08em;
        padding: 7px 10px;
        border-radius: 999px;
        margin-bottom: 14px;
      }

      .activity-content h3 {
        font-size: 1.3rem;
        color: var(--dark);
        margin-bottom: 10px;
      }

      .activity-content p {
        color: var(--muted);
      }

      .portfolio-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }

      .portfolio-card {
        background: linear-gradient(135deg, #fffdf7, #ffffff);
        border: 1px solid rgba(15, 23, 42, 0.08);
      }

      .portfolio-badge {
        display: inline-block;
        margin-bottom: 14px;
        background: #fff3c8;
        color: #8a4b00;
        border-radius: 999px;
        padding: 8px 12px;
        font-size: 0.72rem;
        font-weight: 800;
        text-transform: uppercase;
        letter-spacing: 0.06em;
      }

      .team-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }

      .team-card {
        text-align: center;
        padding: 28px 20px;
      }

      .avatar {
        width: 110px;
        height: 110px;
        border-radius: 50%;
        margin: 0 auto 16px;
        background: linear-gradient(135deg, #f9db73, #f5b623);
        box-shadow: 0 18px 28px rgba(247, 183, 49, 0.25);
      }

      .avatar-one {
        background: linear-gradient(135deg, #fef3c7, #facc15);
      }

      .avatar-two {
        background: linear-gradient(135deg, #fde68a, #fbbf24);
      }

      .avatar-three {
        background: linear-gradient(135deg, #fef3c7, #f59e0b);
      }

      .team-card h3 {
        margin-bottom: 8px;
      }

      .team-card p {
        color: var(--muted);
      }

      .cta {
        padding: 0 0 80px;
      }

      .cta-box {
        background: linear-gradient(135deg, #121826, #1e293b);
        border-radius: 26px;
        padding: 36px 28px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 24px;
        box-shadow: var(--card-shadow);
      }

      .cta-box .eyebrow {
        color: #f8d877;
        margin-bottom: 8px;
      }

      .cta-box h2 {
        color: white;
        font-size: clamp(1.7rem, 3vw, 2.5rem);
      }

      .footer {
        background: #101827;
        color: white;
        padding-top: 30px;
      }

      .footer-grid {
        display: grid;
        grid-template-columns: 1.2fr 1fr 1fr;
        gap: 26px;
        padding-bottom: 28px;
      }

      .footer-logo {
        margin-bottom: 16px;
      }

      .footer h4 {
        color: white;
        margin-bottom: 12px;
        font-size: 1rem;
      }

      .footer ul {
        list-style: none;
        display: grid;
        gap: 10px;
      }

      .footer a,
      .footer li {
        color: rgba(255, 255, 255, 0.8);
      }

      .copyright {
        border-top: 1px solid rgba(255, 255, 255, 0.18);
        padding: 18px 0;
        text-align: center;
        color: rgba(255, 255, 255, 0.75);
      }

      .menu-toggle {
        display: none;
        width: 46px;
        height: 46px;
        background: transparent;
        border: none;
        padding: 0;
        border-radius: 12px;
        cursor: pointer;
      }

      .menu-toggle span {
        display: block;
        width: 100%;
        height: 3px;
        background: var(--dark);
        border-radius: 10px;
        margin: 8px 0;
      }

      @media (max-width: 768px) {
        .nav-menu {
          position: absolute;
          top: 80px;
          left: 0;
          right: 0;
          padding: 18px 24px;
          background: rgba(255, 255, 255, 0.96);
          border-bottom: 1px solid rgba(15, 23, 42, 0.08);
          display: none;
          flex-direction: column;
          align-items: flex-start;
        }

        .nav-menu.active {
          display: flex;
        }

        .menu-toggle {
          display: block;
        }

        .hero-content,
        .about-grid,
        .program-grid,
        .portfolio-grid,
        .team-grid,
        .activity-grid,
        .footer-grid {
          grid-template-columns: 1fr;
        }

        .cta-box {
          flex-direction: column;
          align-items: flex-start;
        }

        .btn {
          width: 100%;
        }

        .hero-actions {
          flex-direction: column;
        }
      }
    </style>
  </head>
  <body>
    <header class="header">
      <nav class="navbar container">
        <div class="logo">
          <div class="logo-mark" aria-label="PiKIR logo">
            <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg">
              <circle cx="32" cy="32" r="29" fill="#0e2245" />
              <circle cx="32" cy="32" r="20" fill="#f3c54c" />
              <path
                d="M20 18 V46 H25 V32 H36 C42 32 46 29 46 23 C46 17 42 14 36 14 H20 Z M25 19 H35 C39 19 41 21 41 24 C41 27 39 29 35 29 H25 V19 Z"
                fill="#0e2245"
              />
              <circle cx="32" cy="32" r="3.2" fill="#fffef5" />
            </svg>
          </div>

          <div class="logo-text">
            <span class="pi">Pi</span><span class="kir">KIR</span>
          </div>
        </div>

        <button class="menu-toggle" aria-label="Menu">
          <span></span>
          <span></span>
          <span></span>
        </button>

        <div class="nav-menu">
          <a href="#beranda">Beranda</a>
          <a href="#tentang">Tentang</a>
          <a href="#program">Program</a>
          <a href="#kegiatan">Kegiatan</a>
          <a href="#portfolio">Portofolio</a>
          <a href="#tim">Pembina</a>
          <a href="#kontak">Kontak</a>
          <a href="#kontak" class="btn btn-primary nav-cta">Kolaborasi</a>
        </div>
      </nav>
    </header>

    <main>
      <section id="beranda" class="hero">
        <div class="container hero-content">
          <div class="hero-copy">
            <p class="eyebrow">Praktisi Kewirausahaan Inovasi Riset</p>
            <h1>Menghubungkan riset, inovasi, dan kewirausahaan untuk perubahan nyata.</h1>
            <p class="subtitle">
              PiKIR hadir sebagai wadah bagi para praktisi, akademisi, dan pelaku
              inovasi untuk mengembangkan ide, membangun solusi berbasis riset,
              serta mendorong ekosistem kewirausahaan yang berdampak.
            </p>

            <div class="hero-actions">
              <a href="#kontak" class="btn btn-primary">Bergabung</a>
              <a href="#program" class="btn btn-secondary">Lihat Program</a>
            </div>

            <div class="stats">
              <div>
                <strong>14th</strong>
                <span>tahun pengalaman</span>
              </div>
              <div>
                <strong>40+</strong>
                <span>program inovasi</span>
              </div>
              <div>
                <strong>2000+</strong>
                <span>pelaku terlibat</span>
              </div>
            </div>
          </div>

          <div class="hero-visual">
            <div class="main-card">
              <div class="badge">Research to Venture</div>
              <h3>Inovasi yang lahir dari riset dan siap diimplementasikan.</h3>
              <ul>
                <li>Riset kebutuhan masyarakat</li>
                <li>Pengembangan solusi inovatif</li>
                <li>Inkubasi kewirausahaan</li>
              </ul>
            </div>

            <div class="floating-card">
              <div class="icon">📈</div>
              <div>
                <strong>85%</strong>
                <p>inovasi siap dikembangkan</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="tentang" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Tentang PiKIR</p>
            <h2>Memberdayakan ide menjadi solusi yang berdampak.</h2>
          </div>

          <div class="about-grid">
            <div class="about-card">
              <h3>Visi</h3>
              <p>
                Menjadi pelopor ekosistem inovasi riset dan kewirausahaan yang
                mendorong kualitas hidup masyarakat melalui solusi nyata.
              </p>
            </div>
            <div class="about-card">
              <h3>Misi</h3>
              <p>
                Mengembangkan kemampuan riset, membangun inovasi yang aplikatif,
                dan mendorong kemandirian usaha berbasis pengetahuan.
              </p>
            </div>
            <div class="about-card">
              <h3>Nilai</h3>
              <p>
                Kreativitas, kolaborasi, integritas, dan kebermanfaatan menjadi
                fondasi utama dalam setiap langkah PiKIR.
              </p>
            </div>
          </div>
        </div>
      </section>

      <section id="program" class="section alt">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Program</p>
            <h2>Lintasan pengembangan inovasi dan kewirausahaan.</h2>
          </div>

          <div class="program-grid">
            <article class="program-card">
              <div class="icon-box">🔬</div>
              <h3>Riset & Analisis</h3>
              <p>
                Mengidentifikasi kebutuhan nyata dan membangun dasar data untuk
                solusi inovatif yang relevan.
              </p>
            </article>

            <article class="program-card">
              <div class="icon-box">💡</div>
              <h3>Inovasi</h3>
              <p>
                Mengembangkan konsep, prototipe, dan model solusi baru yang
                teruji dan aplikatif.
              </p>
            </article>

            <article class="program-card">
              <div class="icon-box">🚀</div>
              <h3>Inkubasi Kewirausahaan</h3>
              <p>
                Menyediakan pendampingan, strategi bisnis, dan jaringan
                pengembangan usaha berbasis inovasi.
              </p>
            </article>

            <article class="program-card">
              <div class="icon-box">🤝</div>
              <h3>Kolaborasi</h3>
              <p>
                Menjalin kemitraan dengan berbagai pihak untuk memperluas
                dampak dan akses terhadap inovasi.
              </p>
            </article>
          </div>
        </div>
      </section>

      <section id="kegiatan" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Kegiatan</p>
            <h2>Aktivitas yang mendorong ide berkembang menjadi solusi.</h2>
          </div>

          <div class="activity-grid">
            <div class="activity-item">
              <div class="activity-image image-one"></div>
              <div class="activity-content">
                <span class="tag">Informasi</span>
                <h3>Info PiKIR Day</h3>
                <p>
                  Serangkaian sosialisasi, pengenalan program, dan informasi
                  penting seputar inovasi, riset, serta peluang kewirausahaan
                  bagi siswa dan komunitas.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-two"></div>
              <div class="activity-content">
                <span class="tag">Festival</span>
                <h3>FIKSA (Festival Kewirausahaan SMASA)</h3>
                <p>
                  Festival kewirausahaan yang menampilkan ide kreatif, bisnis
                  inovatif, serta semangat berwirausaha siswa SMA/SMK dalam
                  wadah yang inspiratif dan kompetitif.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-three"></div>
              <div class="activity-content">
                <span class="tag">Eksperimen</span>
                <h3>Roket Air</h3>
                <p>
                  Kegiatan eksperimen dan kreativitas siswa yang menggabungkan
                  konsep sains, teknik, dan inovasi melalui pembuatan roket air
                  yang menarik dan edukatif.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-four"></div>
              <div class="activity-content">
                <span class="tag">Pengajaran</span>
                <h3>PiJAR (PiKIR Mengajar)</h3>
                <p>
                  Program berbagi ilmu dan pendampingan belajar melalui kegiatan
                  mengajar, pembinaan, serta transfer pengetahuan untuk membangun
                  karakter dan kemampuan siswa.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-five"></div>
              <div class="activity-content">
                <span class="tag">Kunjungan</span>
                <h3>Studi Visit</h3>
                <p>
                  Kegiatan kunjungan belajar ke berbagai instansi, lembaga, atau
                  komunitas untuk menambah wawasan, inspirasi, dan jaringan
                  kolaborasi.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-six"></div>
              <div class="activity-content">
                <span class="tag">Riset</span>
                <h3>Penamaan Ilmiah</h3>
                <p>
                  Kegiatan yang menumbuhkan kreativitas siswa dalam mengembangkan
                  ide-ide ilmiah, inovatif, dan aplikatif melalui proses penamaan
                  produk, karya, atau inovasi dengan pendekatan yang terarah dan
                  edukatif.
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="portfolio" class="section alt">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Portofolio</p>
            <h2>Proyek yang menunjukkan dampak nyata PiKIR.</h2>
          </div>

          <div class="portfolio-grid">
            <div class="portfolio-card">
              <div class="portfolio-badge">Inovasi Sosial</div>
              <h3>Program solusi berbasis kebutuhan masyarakat</h3>
              <p>
                Menciptakan model inovasi yang menjawab permasalahan nyata di
                komunitas dengan pendekatan riset yang terukur.
              </p>
            </div>

            <div class="portfolio-card">
              <div class="portfolio-badge">Startup</div>
              <h3>Pendampingan ide bisnis berbasis riset</h3>
              <p>
                Membantu pelaku usaha menghadapi tantangan pasar dengan strategi
                serta data yang lebih kuat dan terarah.
              </p>
            </div>

            <div class="portfolio-card">
              <div class="portfolio-badge">Teknologi</div>
              <h3>Pengembangan produk inovatif berbasis data</h3>
              <p>
                Menghasilkan prototype dan pengembangan karya yang siap diuji,
                dipelajari, dan diterapkan.
              </p>
            </div>
          </div>
        </div>
      </section>

      <section id="tim" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Pembina Organisasi</p>
            <h2>Para pembina yang membimbing dan mengarahkan organisasi.</h2>
          </div>

          <div class="team-grid">
            <div class="team-card">
              <div class="avatar avatar-one"></div>
              <h3>A. Chizam Baihaqy M.Pd</h3>
              <p>Pembina</p>
            </div>

            <div class="team-card">
              <div class="avatar avatar-two"></div>
              <h3>Ainun Tazkia S.Pd</h3>
              <p>Pembina</p>
            </div>

            <div class="team-card">
              <div class="avatar avatar-three"></div>
              <h3>Rizki Yudha Sentika M.Pd</h3>
              <p>Pembina</p>
            </div>
          </div>
        </div>
      </section>

      <section class="cta">
        <div class="container cta-box">
          <div>
            <p class="eyebrow">Bersama kita membangun ekosistem inovasi yang memberi manfaat.</p>
            <h2>Jadikan ide Anda bermakna dan siap berdaya.</h2>
          </div>
          <a href="#kontak" class="btn btn-light">Hubungi Kami</a>
        </div>
      </section>
    </main>

    <footer id="kontak" class="footer">
      <div class="container footer-grid">
        <div>
          <div class="logo footer-logo">
            <div class="logo-mark" aria-label="PiKIR logo">
              <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg">
                <circle cx="32" cy="32" r="29" fill="#0e2245" />
                <circle cx="32" cy="32" r="20" fill="#f3c54c" />
                <path
                  d="M20 18 V46 H25 V32 H36 C42 32 46 29 46 23 C46 17 42 14 36 14 H20 Z M25 19 H35 C39 19 41 21 41 24 C41 27 39 29 35 29 H25 V19 Z"
                  fill="#0e2245"
                />
                <circle cx="32" cy="32" r="3.2" fill="#fffef5" />
              </svg>
            </div>
          </div>
          <p>
            PiKIR adalah wadah inovasi yang menghubungkan riset, teknologi,
            dan kewirausahaan untuk menghasilkan solusi yang berdampak.
          </p>
        </div>

        <div>
          <h4>Kontak</h4>
          <ul>
            <li>Jl. Inovasi No. 25, Bandung</li>
            <li>hello@pikir.or.id</li>
            <li>+62 812-3456-7890</li>
          </ul>
        </div>

        <div>
          <h4>Menu</h4>
          <ul>
            <li><a href="#beranda">Beranda</a></li>
            <li><a href="#tentang">Tentang</a></li>
            <li><a href="#program">Program</a></li>
            <li><a href="#kontak">Kontak</a></li>
          </ul>
        </div>
      </div>

      <div class="copyright">
        <div class="container">
          <p>© <span id="year"></span> PiKIR. Semua hak dilindungi.</p>
        </div>
      </div>
    </footer>

    <script>
      document.addEventListener("DOMContentLoaded", function () {
        const toggleButton = document.querySelector(".menu-toggle");
        const navMenu = document.querySelector(".nav-menu");
        const yearEl = document.getElementById("year");

        if (toggleButton && navMenu) {
          toggleButton.addEventListener("click", function () {
            navMenu.classList.toggle("active");
          });
        }

        if (yearEl) {
          yearEl.textContent = new Date().getFullYear();
        }
      });
    </script>
  </body>
</html>
