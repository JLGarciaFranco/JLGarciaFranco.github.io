---
layout: default
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dr. Jorge Luis García Franco - Atmospheric Sciences</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            overflow-x: hidden;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.9) 0%, rgba(118, 75, 162, 0.9) 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><path d="M0,300 Q300,200 600,300 T1200,300 L1200,600 L0,600 Z" fill="rgba(255,255,255,0.05)"/></svg>') no-repeat bottom;
            background-size: cover;
            animation: wave 20s ease-in-out infinite;
        }

        @keyframes wave {
            0%, 100% { transform: translateX(0) translateY(0); }
            50% { transform: translateX(-50px) translateY(-20px); }
        }

        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 40px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-text {
            color: white;
            animation: fadeInLeft 1s ease-out;
        }

        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .hero-text h1 {
            font-size: 3.5em;
            margin-bottom: 20px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .hero-text h2 {
            font-size: 1.8em;
            margin-bottom: 30px;
            font-weight: 400;
            opacity: 0.95;
        }

        .hero-text p {
            font-size: 1.2em;
            line-height: 1.8;
            margin-bottom: 15px;
            opacity: 0.9;
        }

        .hero-image {
            position: relative;
            animation: fadeInRight 1s ease-out;
        }

        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .hero-image img {
            width: 100%;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            transition: transform 0.5s ease;
        }

        .hero-image:hover img {
            transform: scale(1.05) rotate(2deg);
        }

        .content-section {
            background: white;
            padding: 80px 40px;
            position: relative;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: #667eea;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60%;
            height: 4px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .research-intro {
            font-size: 1.2em;
            line-height: 1.8;
            color: #555;
            margin: 40px 0;
        }

        .papers-grid {
            display: grid;
            gap: 30px;
            margin-top: 50px;
        }

        .paper-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .paper-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(180deg, #667eea, #764ba2);
        }

        .paper-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }

        .paper-number {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 3em;
            font-weight: 700;
            color: rgba(102, 126, 234, 0.2);
        }

        .paper-card h3 {
            font-size: 1.5em;
            color: #333;
            margin-bottom: 15px;
            padding-right: 60px;
        }

        .paper-card p {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .paper-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 12px 25px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        .paper-link:hover {
            transform: translateX(5px);
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.6);
        }

        .group-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 80px 40px;
            color: white;
        }

        .group-photo-container {
            max-width: 900px;
            margin: 40px auto;
            position: relative;
        }

        .group-photo-container img {
            width: 100%;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.4);
        }

        .cta-section {
            background: #f8f9fa;
            padding: 60px 40px;
            text-align: center;
        }

        .cta-box {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .cta-box h3 {
            font-size: 2em;
            color: #667eea;
            margin-bottom: 20px;
        }

        .cta-box p {
            font-size: 1.2em;
            color: #666;
            margin-bottom: 30px;
        }

        .btn-primary {
            display: inline-block;
            padding: 15px 40px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-size: 1.1em;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.6);
        }

        .links-section {
            background: white;
            padding: 60px 40px;
        }

        .links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .link-card {
            padding: 30px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .link-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .link-card h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.5em;
        }

        .link-card a {
            color: #764ba2;
            text-decoration: none;
            font-weight: 600;
        }

        .link-card a:hover {
            text-decoration: underline;
        }

        @media (max-width: 768px) {
            .hero-content {
                grid-template-columns: 1fr;
                padding: 40px 20px;
            }

            .hero-text h1 {
                font-size: 2.5em;
            }

            .hero-text h2 {
                font-size: 1.4em;
            }

            .section-title {
                font-size: 2em;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="hero-text">
                <h1>JLGF</h1>
                <h2>Associate Professor of Atmospheric Sciences</h2>
                <p>📍 Escuela Nacional de Ciencias de la Tierra<br>
                Universidad Nacional Autónoma de México (UNAM)</p>
                <p>🌪️ Me gustan los tacos de tripa y las nubes que giran</p>
                <p>🌊 Adjunct Research Scientist at Lamont-Doherty Earth Observatory</p>
            </div>
            <div class="hero-image">
                <img src="docs/assets/imgs/foto_oficial.JPG" alt="Pretty Paris">
            </div>
        </div>
    </section>

    <!-- Research Section -->
    <section class="content-section">
        <div class="container">
            <h2 class="section-title">Research Focus</h2>
            <div class="research-intro">
                <p>My current research aims to better understand <strong>tropical climate variability and change</strong>, especially regarding monsoons in the Americas. I am also interested in tropical cyclone prediction at the extended-range, participating in several projects of sub-seasonal-to-seasonal prediction (S2S).</p>
            </div>

            <h2 class="section-title" style="margin-top: 60px;">Selected Publications</h2>
            <div class="papers-grid">
                <div class="paper-card">
                    <span class="paper-number">1</span>
                    <h3>MJO‐TC teleconnections and their influence on North American precipitation: Implications for subseasonal prediction.</h3>
                    <p> Geophysical Research Letters, 2025. </p>
                    <a href="papers/paper1.pdf" class="paper-link">
                        <span>Read Paper</span>
                        <span>→</span>
                    </a>
                </div>

                <div class="paper-card">
                    <span class="paper-number">2</span>
                    <h3>Paper Title Two</h3>
                    <p>Brief description of your second paper. This could include the journal name, year, and key findings or contributions.</p>
                    <a href="papers/paper2.pdf" class="paper-link">
                        <span>Read Paper</span>
                        <span>→</span>
                    </a>
                </div>

                <div class="paper-card">
                    <span class="paper-number">3</span>
                    <h3>Paper Title Three</h3>
                    <p>Brief description of your third paper. This could include the journal name, year, and key findings or contributions.</p>
                    <a href="papers/paper3.pdf" class="paper-link">
                        <span>Read Paper</span>
                        <span>→</span>
                    </a>
                </div>

                <div class="paper-card">
                    <span class="paper-number">4</span>
                    <h3>Paper Title Four</h3>
                    <p>Brief description of your fourth paper. This could include the journal name, year, and key findings or contributions.</p>
                    <a href="papers/paper4.pdf" class="paper-link">
                        <span>Read Paper</span>
                        <span>→</span>
                    </a>
                </div>

                <div class="paper-card">
                    <span class="paper-number">5</span>
                    <h3>Paper Title Five</h3>
                    <p>Brief description of your fifth paper. This could include the journal name, year, and key findings or contributions.</p>
                    <a href="papers/paper5.pdf" class="paper-link">
                        <span>Read Paper</span>
                        <span>→</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Group Photo Section -->
    <section class="group-section">
        <div class="container">
            <h2 class="section-title" style="color: white;">Grupo de Modelación Climática Tropical</h2>
            <div class="group-photo-container">
                <img src="imgs/group_photo.jpg" alt="Research Group Photo">
            </div>
            <p>Integrantes del grupo:</p>
            <p>Andrea Guadalupe Velázquez Cisneros</p>
            <p>Integrantes del grupo:</p>
            <p>Integrantes del grupo:</p>
            <p>Integrantes del grupo:</p>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section">
        <div class="cta-box">
            <h3>Looking for Graduate Students</h3>
            <p>Currently seeking motivated students interested in pursuing a Masters or PhD degree at UNAM focusing on tropical climate dynamics and prediction.</p>
            <a href="mailto:your.email@unam.mx" class="btn-primary">Get in Touch</a>
        </div>
    </section>

    <!-- Links Section -->
    <section class="links-section">
        <div class="container">
            <h2 class="section-title">Resources & Projects</h2>
            <div class="links-grid">
                <div class="link-card">
                    <h3>📚 About Me</h3>
                    <p><a href="./about.md">Learn more about my background</a></p>
                </div>
                <div class="link-card">
                    <h3>🔬 Research Projects</h3>
                    <p><a href="./research.md">Detailed project descriptions</a></p>
                </div>
                <div class="link-card">
                    <h3>👨‍🏫 Courses</h3>
                    <p><a href="./courses.md">Teaching materials (en Español)</a></p>
                </div>
                <div class="link-card">
                    <h3>🐍 PyDropsondes</h3>
                    <p><a href="https://jlgarciafranco.github.io/PyDropsondes/">Python package for TC dropsonde analysis</a></p>
                </div>
                <div class="link-card">
                    <h3>🌧️ MSTCP Dataset</h3>
                    <p><a href="https://zenodo.org/doi/10.5281/zenodo.8322962">Tropical cyclone precipitation estimates</a></p>
                </div>
                <div class="link-card">
                    <h3>🌍 Circulation Decomposition</h3>
                    <p><a href="https://github.com/JLGarciaFranco/Local_walker_hadley">Local Hadley & Walker circulation code</a></p>
                </div>
            </div>
        </div>
    </section>
</body>
</html>
