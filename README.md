<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saicharan K. | Portfolio</title>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-primary: #090d16;
            --bg-secondary: #0b101d;
            --bg-card: #111827;
            --bg-card-hover: #1f2937;
            --border-color: #1f2937;
            --text-main: #f3f4f6;
            --text-muted: #9ca3af;
            --accent-blue: #3b82f6;
            --accent-cyan: #06b6d4;
            --gradient-accent: linear-gradient(135deg, #3b82f6 0%, #06b6d4 100%);
            --shadow-glow: 0 10px 30px -10px rgba(59, 130, 246, 0.3);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--bg-primary);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--border-color);
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #374151;
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background-color: rgba(9, 13, 22, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(31, 41, 55, 0.6);
            transition: var(--transition);
        }

        header.scrolled {
            background-color: rgba(9, 13, 22, 0.95);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 1.25rem;
            font-weight: 800;
            text-decoration: none;
            background: var(--gradient-accent);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
        }

        .nav-link {
            text-decoration: none;
            color: var(--text-muted);
            font-weight: 500;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .nav-link:hover {
            color: var(--accent-blue);
        }

        .nav-btn {
            padding: 0.6rem 1.25rem;
            border-radius: 50px;
            background: var(--gradient-accent);
            color: white;
            font-weight: 600;
            font-size: 0.9rem;
            text-decoration: none;
            box-shadow: var(--shadow-glow);
            transition: var(--transition);
        }

        .nav-btn:hover {
            transform: translateY(-2px);
            filter: brightness(1.1);
        }

        .hamburger {
            display: none;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            color: var(--text-main);
            padding: 0.5rem;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.2rem;
        }

        /* Mobile Menu */
        .mobile-menu {
            display: none;
            background-color: var(--bg-secondary);
            border-bottom: 1px solid var(--border-color);
            padding: 1.5rem 2rem;
            flex-direction: column;
            gap: 1rem;
        }

        .mobile-menu.active {
            display: flex;
        }

        .mobile-menu .nav-link {
            padding: 0.5rem 0;
            font-size: 1.1rem;
        }

        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 8rem 2rem 4rem 2rem;
            text-align: center;
            overflow: hidden;
        }

        .hero-glow-1 {
            position: absolute;
            top: 25%;
            left: 50%;
            transform: translateX(-50%) translateY(-50%);
            width: 450px;
            height: 450px;
            background: rgba(59, 130, 246, 0.15);
            border-radius: 50%;
            filter: blur(120px);
            pointer-events: none;
        }

        .hero-glow-2 {
            position: absolute;
            bottom: 10%;
            right: 10%;
            width: 300px;
            height: 300px;
            background: rgba(6, 182, 212, 0.1);
            border-radius: 50%;
            filter: blur(100px);
            pointer-events: none;
        }

        .hero-content {
            max-width: 850px;
            position: relative;
            z-index: 2;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.5rem 1rem;
            background: rgba(30, 58, 138, 0.4);
            border: 1px solid rgba(30, 64, 175, 0.5);
            border-radius: 50px;
            color: #60a5fa;
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 2rem;
            backdrop-filter: blur(5px);
        }

        .badge-dot {
            width: 8px;
            height: 8px;
            background-color: var(--accent-blue);
            border-radius: 50%;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.3); opacity: 0.5; }
            100% { transform: scale(1); opacity: 1; }
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4.5rem);
            font-weight: 800;
            letter-spacing: -0.025em;
            margin-bottom: 1.5rem;
            line-height: 1.1;
        }

        .hero h1 span {
            background: var(--gradient-accent);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: clamp(1rem, 2vw, 1.2rem);
            color: var(--text-muted);
            max-width: 680px;
            margin: 0 auto 2.5rem auto;
            line-height: 1.7;
        }

        .hero-actions {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn-primary {
            padding: 0.9rem 2rem;
            border-radius: 12px;
            background: var(--accent-blue);
            color: white;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            box-shadow: var(--shadow-glow);
            transition: var(--transition);
        }

        .btn-primary:hover {
            background: #2563eb;
            transform: translateY(-2px);
        }

        .btn-secondary {
            padding: 0.9rem 2rem;
            border-radius: 12px;
            background: rgba(17, 24, 39, 0.8);
            border: 1px solid var(--border-color);
            color: var(--text-main);
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: var(--transition);
        }

        .btn-secondary:hover {
            background: var(--bg-card-hover);
            border-color: #374151;
            transform: translateY(-2px);
        }

        .social-bar {
            display: flex;
            justify-content: center;
            gap: 1.25rem;
            margin-top: 3.5rem;
        }

        .social-icon {
            width: 45px;
            height: 45px;
            background: rgba(17, 24, 39, 0.9);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-muted);
            font-size: 1.1rem;
            text-decoration: none;
            transition: var(--transition);
        }

        .social-icon:hover {
            color: white;
            border-color: rgba(59, 130, 246, 0.5);
            background: var(--bg-card-hover);
            transform: translateY(-3px);
        }

        section {
            padding: 6rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-subtitle {
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.15em;
            color: var(--accent-blue);
            margin-bottom: 0.75rem;
        }

        .section-title {
            font-size: clamp(2rem, 3.5vw, 2.75rem);
            font-weight: 800;
            letter-spacing: -0.02em;
        }

        .about-wrapper {
            display: grid;
            grid-template-columns: 1fr 1.5fr;
            gap: 3rem;
            align-items: center;
        }

        .about-card-profile {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 3rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .about-card-profile::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 150px;
            height: 150px;
            background: rgba(59, 130, 246, 0.1);
            border-radius: 50%;
            filter: blur(40px);
        }

        .avatar-box {
            width: 90px;
            height: 90px;
            margin: 0 auto 1.5rem auto;
            border-radius: 18px;
            background: var(--gradient-accent);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: 800;
            color: white;
            box-shadow: var(--shadow-glow);
        }

        .about-card-profile h3 {
            font-size: 1.25rem;
            margin-bottom: 0.25rem;
        }

        .about-card-profile .role {
            font-size: 0.9rem;
            color: var(--accent-blue);
            font-weight: 600;
            margin-bottom: 0.75rem;
        }

        .about-card-profile .location {
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        .about-text-box {
            background: rgba(17, 24, 39, 0.6);
            border: 1px solid rgba(31, 41, 55, 0.8);
            border-radius: 20px;
            padding: 2.5rem;
        }

        .about-text-box p {
            color: var(--text-muted);
            font-size: 1.05rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            padding-top: 1.5rem;
            border-top: 1px solid var(--border-color);
        }

        .stat-item .stat-num {
            font-size: 1.75rem;
            font-weight: 800;
            color: white;
            display: block;
        }

        .stat-item .stat-label {
            font-size: 0.75rem;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 2rem;
            transition: var(--transition);
        }

        .skill-card:hover {
            border-color: rgba(59, 130, 246, 0.4);
            transform: translateY(-4px);
        }

        .skill-icon-box {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent-blue);
            font-size: 1.25rem;
            margin-bottom: 1.25rem;
        }

        .skill-card h4 {
            font-size: 1.15rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .skill-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .pill {
            padding: 0.35rem 0.85rem;
            background: rgba(31, 41, 55, 0.8);
            border: 1px solid rgba(55, 65, 81, 0.6);
            border-radius: 8px;
            font-size: 0.8rem;
            font-weight: 500;
            color: #d1d5db;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: var(--transition);
        }

        .project-card:hover {
            border-color: rgba(59, 130, 246, 0.5);
            transform: translateY(-5px);
            box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.5);
        }

        .project-body {
            padding: 2.5rem;
        }

        .project-top {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 1.5rem;
        }

        .project-tag {
            padding: 0.35rem 0.9rem;
            background: rgba(30, 58, 138, 0.4);
            border: 1px solid rgba(30, 64, 175, 0.5);
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
            color: #60a5fa;
        }

        .project-card i {
            font-size: 1.5rem;
            color: var(--accent-blue);
        }

        .project-card h4 {
            font-size: 1.35rem;
            font-weight: 700;
            margin-bottom: 0.75rem;
        }

        .project-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        .project-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem;
        }

        .project-footer {
            padding: 1.25rem 2.5rem;
            background: rgba(3, 7, 18, 0.6);
            border-top: 1px solid rgba(31, 41, 55, 0.8);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .project-footer span {
            font-size: 0.8rem;
            color: var(--text-muted);
            font-weight: 500;
        }

        .project-link {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--accent-blue);
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.3rem;
            transition: var(--transition);
        }

        .project-link:hover {
            color: #60a5fa;
            gap: 0.5rem;
        }

        .certs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
        }

        .cert-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 2rem;
            display: flex;
            align-items: flex-start;
            gap: 1.25rem;
            transition: var(--transition);
        }

        .cert-card:hover {
            border-color: rgba(59, 130, 246, 0.4);
        }

        .cert-icon {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.2);
            flex-shrink: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent-blue);
            font-size: 1.1rem;
        }

        .cert-org {
            display: inline-block;
            padding: 0.2rem 0.6rem;
            background: rgba(30, 58, 138, 0.4);
            border: 1px solid rgba(30, 64, 175, 0.5);
            border-radius: 4px;
            font-size: 0.7rem;
            font-weight: 600;
            color: #60a5fa;
            margin-bottom: 0.5rem;
        }

        .cert-card h4 {
            font-size: 1.05rem;
            font-weight: 700;
            margin-bottom: 0.3rem;
        }

        .cert-card p {
            font-size: 0.85rem;
            color: var(--text-muted);
            line-height: 1.5;
        }

        .contact-container {
            max-width: 750px;
            margin: 0 auto;
        }

        .contact-form {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 3rem;
            box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.5);
        }

        .form-group-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-label {
            display: block;
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            color: var(--text-muted);
            margin-bottom: 0.5rem;
        }

        .form-input, .form-textarea {
            width: 100%;
            background: #030712;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 0.9rem 1.25rem;
            color: white;
            font-family: inherit;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .form-input:focus, .form-textarea:focus {
            outline: none;
            border-color: var(--accent-blue);
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.2);
        }

        .form-textarea {
            resize: none;
            height: 140px;
        }

        .form-alert {
            display: none;
            padding: 1rem;
            border-radius: 12px;
            font-size: 0.9rem;
            font-weight: 500;
            margin-bottom: 1.5rem;
            border: 1px solid transparent;
        }

        .form-alert.success {
            display: block;
            background: rgba(6, 78, 59, 0.4);
            border-color: rgba(5, 150, 105, 0.5);
            color: #34d399;
        }

        .form-alert.error {
            display: block;
            background: rgba(127, 29, 29, 0.4);
            border-color: rgba(220, 38, 38, 0.5);
            color: #f87171;
        }

        .submit-btn {
            width: 100%;
            padding: 1rem;
            border-radius: 12px;
            background: var(--gradient-accent);
            border: none;
            color: white;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            box-shadow: var(--shadow-glow);
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .submit-btn:hover {
            filter: brightness(1.1);
            transform: translateY(-2px);
        }

        footer {
            border-top: 1px solid var(--border-color);
            background-color: var(--bg-primary);
            padding: 3rem 2rem;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .footer-socials {
            display: flex;
            gap: 1.5rem;
        }

        .footer-socials a {
            color: var(--text-muted);
            font-size: 1rem;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-socials a:hover {
            color: white;
        }

        @media (max-width: 900px) {
            .about-wrapper {
                grid-template-columns: 1fr;
            }
            .nav-menu, .nav-btn {
                display: none;
            }
            .hamburger {
                display: block;
            }
        }

        @media (max-width: 768px) {
            .form-group-grid {
                grid-template-columns: 1fr;
                gap: 0;
            }
            .footer-container {
                flex-direction: column;
                gap: 1.5rem;
            }
            .projects-grid, .skills-grid, .certs-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <header id="header">
        <div class="nav-container">
            <a href="#hero" class="logo">
                <i class="fa-solid fa-code"></i> Saicharan K.
            </a>
            
            <ul class="nav-menu">
                <li><a href="#about" class="nav-link">About</a></li>
                <li><a href="#skills" class="nav-link">Skills</a></li>
                <li><a href="#projects" class="nav-link">Projects</a></li>
                <li><a href="#certifications" class="nav-link">Certifications</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>

            <a href="#contact" class="nav-btn">Let's Talk</a>

            <button id="hamburger" class="hamburger" aria-label="Toggle Navigation">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="mobile-menu">
            <a href="#about" class="nav-link mobile-nav-link">About</a>
            <a href="#skills" class="nav-link mobile-nav-link">Skills</a>
            <a href="#projects" class="nav-link mobile-nav-link">Projects</a>
            <a href="#certifications" class="nav-link mobile-nav-link">Certifications</a>
            <a href="#contact" class="nav-link mobile-nav-link">Contact</a>
        </div>
    </header>

    <section id="hero" class="hero">
        <div class="hero-glow-1"></div>
        <div class="hero-glow-2"></div>

        <div class="hero-content">
            <div class="hero-badge">
                <span class="badge-dot"></span>
                J.N.N Institute of Engineering • CSE Undergraduate
            </div>

            <h1>Hi, I'm <span>Saicharan K.</span></h1>
            
            <p>
                Undergraduate Computer Science & Engineering Student | Full-Stack Developer & AI Integrator bridging modern frontend interfaces with robust backend systems.
            </p>

            <div class="hero-actions">
                <a href="#projects" class="btn-primary">
                    <span>View Projects</span>
                    <i class="fa-solid fa-arrow-down" style="font-size: 0.85rem;"></i>
                </a>
                <a href="#contact" class="btn-secondary">
                    <span>Contact Me</span>
                    <i class="fa-regular fa-envelope" style="font-size: 0.85rem;"></i>
                </a>
            </div>

            <div class="social-bar">
                <a href="https://github.com" target="_blank" rel="noopener noreferrer" aria-label="GitHub Profile" class="social-icon">
                    <i class="fa-brands fa-github"></i>
                </a>
                <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn Profile" class="social-icon">
                    <i class="fa-brands fa-linkedin-in"></i>
                </a>
                <a href="mailto:contact@saicharan.dev" aria-label="Email Me" class="social-icon">
                    <i class="fa-solid fa-envelope"></i>
                </a>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="section-header">
            <div class="section-subtitle">About Me</div>
            <h2 class="section-title">Engineering Intelligent Digital Solutions</h2>
        </div>

        <div class="about-wrapper">
            <div class="about-card-profile">
                <div class="avatar-box">SK</div>
                <h3>Saicharan K.</h3>
                <div class="role">CSE Undergraduate</div>
                <div class="location">J.N.N Institute of Engineering, Tamil Nadu</div>
            </div>

            <div class="about-text-box">
                <p>
                    Motivated and detail-oriented Computer Science undergraduate with hands-on experience building full-stack web applications, integrating multimodal artificial intelligence pipelines, and developing automated workflow solutions.
                </p>
                <p>
                    Adept at bridging modern frontend interfaces with robust backend architectures, focusing on practical, user-centric deployments across health-tech, travel, and communication domains.
                </p>

                <div class="about-stats">
                    <div class="stat-item">
                        <span class="stat-num">3+</span>
                        <span class="stat-label">Core Projects</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-num">SIH</span>
                        <span class="stat-label">National Finalist</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-num">AI/Full</span>
                        <span class="stat-label">Stack Focus</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="section-header">
            <div class="section-subtitle">Expertise</div>
            <h2 class="section-title">Skills & Technical Stack</h2>
        </div>

        <div class="skills-grid">
            <!-- Languages -->
            <div class="skill-card">
                <div class="skill-icon-box"><i class="fa-solid fa-code"></i></div>
                <h4>Languages</h4>
                <div class="skill-pills">
                    <span class="pill">Python</span>
                    <span class="pill">JavaScript</span>
                    <span class="pill">TypeScript</span>
                    <span class="pill">Java</span>
                    <span class="pill">C</span>
                    <span class="pill">8086 Assembly</span>
                </div>
            </div>

            <!-- Frontend & Styling -->
            <div class="skill-card">
                <div class="skill-icon-box"><i class="fa-solid fa-laptop-code"></i></div>
                <h4>Frontend & Styling</h4>
                <div class="skill-pills">
                    <span class="pill">React</span>
                    <span class="pill">Next.js</span>
                    <span class="pill">Tailwind CSS</span>
                    <span class="pill">Bootstrap</span>
                </div>
            </div>

            <!-- Backend & APIs -->
            <div class="skill-card">
                <div class="skill-icon-box"><i class="fa-solid fa-server"></i></div>
                <h4>Backend & APIs</h4>
                <div class="skill-pills">
                    <span class="pill">Node.js</span>
                    <span class="pill">Express</span>
                    <span class="pill">FastAPI</span>
                    <span class="pill">WhatsApp Cloud API</span>
                    <span class="pill">Twilio</span>
                    <span class="pill">n8n Webhooks</span>
                </div>
            </div>

            <!-- Databases -->
            <div class="skill-card">
                <div class="skill-icon-box"><i class="fa-solid fa-database"></i></div>
                <h4>Databases</h4>
                <div class="skill-pills">
                    <span class="pill">MongoDB</span>
                    <span class="pill">PostgreSQL</span>
                    <span class="pill">SQLite</span>
                </div>
            </div>

            <!-- AI & Tooling -->
            <div class="skill-card" style="grid-column: span 1;">
                <div class="skill-icon-box"><i class="fa-solid fa-brain"></i></div>
                <h4>AI & Tooling</h4>
                <div class="skill-pills">
                    <span class="pill">Google Gemini API</span>
                    <span class="pill">Bhashini ULCA APIs</span>
                    <span class="pill">Ollama (Qwen2.5-Coder)</span>
                    <span class="pill">Git & GitHub</span>
                    <span class="pill">GitHub Copilot</span>
                    <span class="pill">Continue / VS Code</span>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="section-header">
            <div class="section-subtitle">Portfolio</div>
            <h2 class="section-title">Featured Key Projects</h2>
        </div>

        <div class="projects-grid">
            <!-- Project 1 -->
            <div class="project-card">
                <div class="project-body">
                    <div class="project-top">
                        <span class="project-tag">SIH 2026</span>
                        <i class="fa-solid fa-hospital-user"></i>
                    </div>
                    <h4>CareIntake Platform</h4>
                    <p>
                        An AI-powered pre-consultation medical history platform featuring voice and touch interfaces, OCR document parsing, AYUSH diagnostic mode, and an offline decision tree inference engine.
                    </p>
                    <div class="project-pills">
                        <span class="pill">React</span>
                        <span class="pill">FastAPI</span>
                        <span class="pill">Gemini API</span>
                        <span class="pill">OCR</span>
                    </div>
                </div>
                <div class="project-footer">
                    <span>Health-Tech Innovation</span>
                    <a href="#contact" class="project-link">Inquire <i class="fa-solid fa-arrow-right" style="font-size: 0.75rem;"></i></a>
                </div>
            </div>

            <!-- Project 2 -->
            <div class="project-card">
                <div class="project-body">
                    <div class="project-top">
                        <span class="project-tag" style="background: rgba(8, 145, 178, 0.2); border-color: rgba(6, 182, 212, 0.4); color: #22d3ee;">Internship Project</span>
                        <i class="fa-solid fa-plane-departure" style="color: var(--accent-cyan);"></i>
                    </div>
                    <h4>Travel Booking Platform</h4>
                    <p>
                        Designed and engineered a full-stack travel booking platform leveraging React for dynamic user interactions and Node.js for backend server handling and booking data management.
                    </p>
                    <div class="project-pills">
                        <span class="pill">React</span>
                        <span class="pill">Node.js</span>
                        <span class="pill">Express</span>
                        <span class="pill">MongoDB</span>
                    </div>
                </div>
                <div class="project-footer">
                    <span>J.N.N Internship</span>
                    <a href="#contact" class="project-link" style="color: var(--accent-cyan);">Inquire <i class="fa-solid fa-arrow-right" style="font-size: 0.75rem;"></i></a>
                </div>
            </div>

            <!-- Project 3 -->
            <div class="project-card">
                <div class="project-body">
                    <div class="project-top">
                        <span class="project-tag" style="background: rgba(99, 102, 241, 0.2); border-color: rgba(99, 102, 241, 0.4); color: #818cf8;">Automation</span>
                        <i class="fa-brands fa-whatsapp" style="color: #818cf8;"></i>
                    </div>
                    <h4>Prescription Dispatcher</h4>
                    <p>
                        Built an automated backend workflow using Express and the WhatsApp Cloud API to securely dispatch digital prescriptions and PDF medical attachments directly to patients.
                    </p>
                    <div class="project-pills">
                        <span class="pill">Express</span>
                        <span class="pill">WhatsApp Cloud API</span>
                        <span class="pill">n8n</span>
                    </div>
                </div>
                <div class="project-footer">
                    <span>Automated Workflow</span>
                    <a href="#contact" class="project-link" style="color: #818cf8;">Inquire <i class="fa-solid fa-arrow-right" style="font-size: 0.75rem;"></i></a>
                </div>
            </div>
        </div>
    </section>

    <section id="certifications">
        <div class="section-header">
            <div class="section-subtitle">Credentials</div>
            <h2 class="section-title">Certifications & Training</h2>
        </div>

        <div class="certs-grid">
            <!-- Cert 1 -->
            <div class="cert-card">
                <div class="cert-icon"><i class="fa-solid fa-award"></i></div>
                <div>
                    <span class="cert-org">Infosys Springboard</span>
                    <h4>Artificial Intelligence & Python</h4>
                    <p>Comprehensive coursework covering core Python programming and foundational AI concepts.</p>
                </div>
            </div>

            <!-- Cert 2 -->
            <div class="cert-card">
                <div class="cert-icon" style="color: var(--accent-cyan);"><i class="fa-solid fa-robot"></i></div>
                <div>
                    <span class="cert-org" style="background: rgba(8, 145, 178, 0.2); border-color: rgba(6, 182, 212, 0.4); color: #22d3ee;">GitHub</span>
                    <h4>GitHub Copilot Developer</h4>
                    <p>Developer Productivity & AI-Assisted Coding Certification for accelerated software engineering.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="section-header">
            <div class="section-subtitle">Get In Touch</div>
            <h2 class="section-title">Let's Build Something Great</h2>
        </div>

        <div class="contact-container">
            <form id="contact-form" class="contact-form">
                <div id="form-alert" class="form-alert"></div>

                <div class="form-group-grid">
                    <div class="form-group">
                        <label for="name" class="form-label">Your Name</label>
                        <input type="text" id="name" required class="form-input" placeholder="John Doe">
                    </div>
                    <div class="form-group">
                        <label for="email" class="form-label">Your Email</label>
                        <input type="email" id="email" required class="form-input" placeholder="john@example.com">
                    </div>
                </div>

                <div class="form-group">
                    <label for="subject" class="form-label">Subject</label>
                    <input type="text" id="subject" required class="form-input" placeholder="Project Inquiry / Collaboration">
                </div>

                <div class="form-group">
                    <label for="message" class="form-label">Message</label>
                    <textarea id="message" required class="form-textarea" placeholder="Write your message here..."></textarea>
                </div>

                <button type="submit" class="submit-btn">
                    <span>Send Message</span>
                    <i class="fa-solid fa-paper-plane" style="font-size: 0.85rem;"></i>
                </button>
            </form>
        </div>
    </section>

    <footer>
        <div class="footer-container">
            <p>&copy; 2026 Saicharan K. All rights reserved.</p>
            <div class="footer-socials">
                <a href="https://github.com" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i> GitHub</a>
                <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin-in"></i> LinkedIn</a>
                <a href="mailto:contact@saicharan.dev"><i class="fa-solid fa-envelope"></i> Email</a>
            </div>
        </div>
    </footer>

    <script>
        // Hamburger Menu Toggle
        const hamburger = document.getElementById('hamburger');
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-nav-link');

        hamburger.addEventListener('click', () => {
            mobileMenu.classList.toggle('active');
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
            });
        });

        // Sticky Header Shadow on Scroll
        const header = document.getElementById('header');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 25) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Contact Form Submission & Custom Success Box (No alert())
        const contactForm = document.getElementById('contact-form');
        const formAlert = document.getElementById('form-alert');

        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();

            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const subject = document.getElementById('subject').value.trim();
            const message = document.getElementById('message').value.trim();

            if (!name || !email || !subject || !message) {
                showFormAlert('Please fill in all required fields.', 'error');
                return;
            }

            showFormAlert(`Thank you, ${name}! Your message has been successfully sent. I will get back to you soon.`, 'success');
            contactForm.reset();
        });

        function showFormAlert(text, type) {
            formAlert.textContent = text;
            formAlert.className = `form-alert ${type}`;
            formAlert.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
    </script>
</body>
</html>
