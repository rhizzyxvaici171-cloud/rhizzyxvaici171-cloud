<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio | Lead Systems Architect</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --bg: #0a0a0c;
            --card-bg: rgba(255, 255, 255, 0.03);
            --accent: #64ffda;
            --text-main: #e6f1ff;
            --text-dim: #8892b0;
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', -apple-system, sans-serif; }

        body {
            background-color: var(--bg);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Smooth Scroll */
        html { scroll-behavior: smooth; }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2rem 10%;
            position: fixed;
            width: 100%;
            backdrop-filter: blur(10px);
            z-index: 1000;
        }

        .logo { font-weight: 800; color: var(--accent); font-size: 1.5rem; }

        .nav-links a {
            color: var(--text-main);
            text-decoration: none;
            margin-left: 2rem;
            font-size: 0.9rem;
            transition: 0.3s;
        }

        .nav-links a:hover { color: var(--accent); }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 0 15%;
            background: radial-gradient(circle at 10% 20%, rgba(100, 255, 218, 0.05) 0%, transparent 50%);
        }

        .hero span { color: var(--accent); font-family: monospace; font-size: 1.1rem; }

        .hero h1 {
            font-size: clamp(40px, 8vw, 80px);
            font-weight: 700;
            margin: 1rem 0;
            color: var(--text-main);
        }

        .hero h2 {
            font-size: clamp(30px, 5vw, 50px);
            color: var(--text-dim);
            margin-bottom: 2rem;
        }

        .hero p { max-width: 600px; color: var(--text-dim); margin-bottom: 3rem; }

        /* Section Styling */
        section { padding: 100px 15%; }
        h3.section-title {
            display: flex;
            align-items: center;
            font-size: 2rem;
            margin-bottom: 40px;
            color: var(--text-main);
        }

        h3.section-title::after {
            content: "";
            height: 1px;
            width: 300px;
            background: var(--glass-border);
            margin-left: 20px;
        }

        /* Project Grid */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: var(--card-bg);
            border: 1px solid var(--glass-border);
            padding: 30px;
            border-radius: 12px;
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent);
        }

        .project-card i { color: var(--accent); font-size: 1.5rem; margin-bottom: 1.5rem; }

        /* Experience Section */
        .exp-container {
            border-left: 2px solid var(--glass-border);
            padding-left: 30px;
            margin-left: 10px;
        }

        .exp-item { position: relative; margin-bottom: 50px; }

        .exp-item::before {
            content: "";
            position: absolute;
            left: -41px;
            top: 5px;
            width: 20px;
            height: 20px;
            background: var(--bg);
            border: 2px solid var(--accent);
            border-radius: 50%;
        }

        .btn {
            border: 1px solid var(--accent);
            color: var(--accent);
            padding: 1.25rem 1.75rem;
            text-decoration: none;
            border-radius: 4px;
            display: inline-block;
            transition: 0.3s;
        }

        .btn:hover { background: rgba(100, 255, 218, 0.1); }

        footer {
            text-align: center;
            padding: 50px;
            color: var(--text-dim);
            font-size: 0.8rem;
        }

    </style>
</head>
<body>

    <nav>
        <div class="logo">/dev/name</div>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="#projects">Projects</a>
            <a href="#experience">Experience</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <header class="hero">
        <span>Hi, my name is</span>
        <h1>Your Name.</h1>
        <h2>I build things for the web.</h2>
        <p>I’m a software engineer specializing in building (and occasionally designing) exceptional digital experiences. Currently, I’m focused on building accessible, human-centered products at <strong>[Your Company]</strong>.</p>
        <a href="#projects" class="btn">View My Work</a>
    </header>

    <section id="about">
        <h3 class="section-title">About Me</h3>
        <p style="max-width: 800px; color: var(--text-dim);">
            Hello! My interest in web development started back in 2012 when I decided to try editing custom Tumblr themes — turns out hacking together a custom reblog button taught me a lot about HTML & CSS! <br><br>
            Fast-forward to today, and I’ve had the privilege of working at an advertising agency, a start-up, a huge corporation, and a student-led design studio. My main focus these days is building accessible, inclusive products and digital experiences for a variety of clients.
        </p>
    </section>

    <section id="projects">
        <h3 class="section-title">Featured Projects</h3>
        <div class="project-grid">
            <div class="project-card">
                <i class="fa-regular fa-folder-open"></i>
                <h4>Cloud Dashboard</h4>
                <p>A high-performance monitoring tool for Kubernetes clusters, featuring real-time metrics and alerts.</p>
                <div style="margin-top: 1rem; font-size: 0.8rem; color: var(--accent);">React · Go · AWS</div>
            </div>
            <div class="project-card">
                <i class="fa-regular fa-folder-open"></i>
                <h4>AI Engine</h4>
                <p>Custom LLM implementation for analyzing codebase patterns and suggesting architectural improvements.</p>
                <div style="margin-top: 1rem; font-size: 0.8rem; color: var(--accent);">Python · PyTorch · Docker</div>
            </div>
            <div class="project-card">
                <i class="fa-regular fa-folder-open"></i>
                <h4>Protocol X</h4>
                <p>Decentralized storage protocol optimized for high-speed retrieval of encrypted medical records.</p>
                <div style="margin-top: 1rem; font-size: 0.8rem; color: var(--accent);">Rust · WebAssembly</div>
            </div>
        </div>
    </section>

    <section id="experience">
        <h3 class="section-title">Career Path</h3>
        <div class="exp-container">
            <div class="exp-item">
                <h4>Senior Software Engineer @ TechGiant</h4>
                <p style="font-size: 0.9rem; color: var(--accent);">2024 — Present</p>
                <p style="color: var(--text-dim);">Leading the core infrastructure team. Scaled system throughput by 40% and mentored 5 junior engineers.</p>
            </div>
            <div class="exp-item">
                <h4>Full Stack Developer @ StartupInc</h4>
                <p style="font-size: 0.9rem; color: var(--accent);">2022 — 2024</p>
                <p style="color: var(--text-dim);">Architected the initial MVP using Next.js and Supabase. Secured Series A funding through technical excellence.</p>
            </div>
        </div>
    </section>

    <section id="contact" style="text-align: center;">
        <h3 class="section-title" style="justify-content: center;">Get In Touch</h3>
        <p style="margin-bottom: 2rem; color: var(--text-dim);">My inbox is always open. Whether you have a question or just want to say hi, I’ll try my best to get back to you!</p>
        <a href="mailto:your.email@example.com" class="btn">Say Hello</a>
    </section>

    <footer>
        <p>Designed & Built by Your Name &copy; 2026</p>
    </footer>

</body>
</html>
