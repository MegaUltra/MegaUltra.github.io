<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MegaUltra Gaming & Hacking Hub</title>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    
    <!-- Google Fonts - Cyberpunk Style -->
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;400;600;700&family=Press+Start+2P&display=swap" rel="stylesheet">
    
    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0a0a0f;
            color: #e0f2fe;
            font-family: 'Rajdhani', sans-serif;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* ===== ANIMATED BACKGROUND ===== */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 255, 200, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 80% 50%, rgba(255, 0, 200, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 50% 100%, rgba(0, 100, 255, 0.03) 0%, transparent 50%);
            overflow: hidden;
        }

        .bg-animation .grid-line {
            position: absolute;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 200, 0.05), transparent);
            height: 1px;
            width: 100%;
            animation: gridMove 8s linear infinite;
        }

        .bg-animation .grid-line:nth-child(1) { top: 10%; animation-delay: 0s; }
        .bg-animation .grid-line:nth-child(2) { top: 30%; animation-delay: 2s; }
        .bg-animation .grid-line:nth-child(3) { top: 50%; animation-delay: 4s; }
        .bg-animation .grid-line:nth-child(4) { top: 70%; animation-delay: 6s; }
        .bg-animation .grid-line:nth-child(5) { top: 90%; animation-delay: 3s; }

        @keyframes gridMove {
            0% { transform: translateX(-100%); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateX(100%); opacity: 0; }
        }

        /* Floating Particles */
        .particle {
            position: absolute;
            width: 3px;
            height: 3px;
            background: #00ffcc;
            border-radius: 50%;
            animation: floatParticle 15s infinite linear;
            opacity: 0.3;
        }

        @keyframes floatParticle {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 0.5; }
            90% { opacity: 0.5; }
            100% { transform: translateY(-10vh) rotate(720deg); opacity: 0; }
        }

        /* ===== MAIN CONTAINER ===== */
        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* ===== HEADER ===== */
        .header {
            text-align: center;
            padding: 30px 20px 20px;
            background: rgba(10, 10, 20, 0.6);
            backdrop-filter: blur(10px);
            border-radius: 30px;
            border: 1px solid rgba(0, 255, 200, 0.15);
            box-shadow: 0 0 60px rgba(0, 255, 200, 0.05);
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, rgba(0, 255, 200, 0.03), transparent, rgba(255, 0, 200, 0.03), transparent);
            animation: rotateGlow 20s linear infinite;
        }

        @keyframes rotateGlow {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .logo {
            font-family: 'Orbitron', monospace;
            font-size: 4.5rem;
            font-weight: 900;
            background: linear-gradient(135deg, #00ffcc, #00ff88, #00ccff, #ff00cc);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientShift 3s ease-in-out infinite;
            text-shadow: none;
            letter-spacing: 8px;
            position: relative;
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .logo-sub {
            font-family: 'Press Start 2P', cursive;
            font-size: 0.8rem;
            color: #ffdd44;
            -webkit-text-fill-color: #ffdd44;
            letter-spacing: 4px;
            margin-top: 5px;
            opacity: 0.8;
        }

        .badge-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 15px 0 10px;
        }

        .badge {
            background: rgba(0, 255, 200, 0.08);
            border: 1px solid rgba(0, 255, 200, 0.3);
            padding: 6px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            color: #00ffcc;
            font-weight: 600;
            backdrop-filter: blur(4px);
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .badge i {
            font-size: 1rem;
        }

        .badge.gold {
            border-color: #ffdd44;
            color: #ffdd44;
            background: rgba(255, 220, 68, 0.08);
        }

        .owners-display {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin: 15px 0 5px;
        }

        .owner-card {
            background: rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(255, 215, 0, 0.3);
            padding: 8px 25px;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 700;
            color: #ffdd77;
            display: flex;
            align-items: center;
            gap: 12px;
            backdrop-filter: blur(4px);
            transition: all 0.3s;
        }

        .owner-card:hover {
            transform: scale(1.05);
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.2);
            border-color: #ffdd44;
        }

        .owner-card .crown {
            font-size: 1.5rem;
            animation: crownSpin 4s linear infinite;
        }

        @keyframes crownSpin {
            0% { transform: rotate(0deg) scale(1); }
            50% { transform: rotate(10deg) scale(1.1); }
            100% { transform: rotate(0deg) scale(1); }
        }

        .status-bar {
            margin-top: 15px;
            padding: 10px 20px;
            background: rgba(0, 255, 200, 0.05);
            border-radius: 20px;
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            font-size: 0.9rem;
            border: 1px solid rgba(0, 255, 200, 0.08);
        }

        .status-item {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #88ddcc;
        }

        .status-item .dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            display: inline-block;
            animation: dotPulse 2s infinite;
        }

        .dot.green { background: #00ff88; }
        .dot.pink { background: #ff44aa; }
        .dot.blue { background: #4488ff; }

        @keyframes dotPulse {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.3; transform: scale(0.8); }
        }

        /* ===== STATS SECTION ===== */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: rgba(10, 10, 20, 0.6);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(0, 255, 200, 0.1);
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: #00ffcc;
            box-shadow: 0 0 30px rgba(0, 255, 200, 0.05);
        }

        .stat-card .number {
            font-family: 'Orbitron', monospace;
            font-size: 2.2rem;
            font-weight: 700;
            background: linear-gradient(135deg, #00ffcc, #44ddff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-card .label {
            font-size: 0.85rem;
            color: #88aacc;
            margin-top: 5px;
        }

        /* ===== UPLOAD SECTION ===== */
        .upload-section {
            background: rgba(10, 10, 20, 0.6);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(0, 255, 200, 0.1);
            border-radius: 25px;
            padding: 30px;
            margin-bottom: 35px;
        }

        .upload-section h2 {
            font-family: 'Orbitron', monospace;
            font-size: 1.5rem;
            color: #00ffcc;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .upload-area {
            border: 2px dashed rgba(0, 255, 200, 0.2);
            border-radius: 20px;
            padding: 40px 20px;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
        }

        .upload-area:hover {
            border-color: #00ffcc;
            background: rgba(0, 255, 200, 0.02);
        }

        .upload-area.dragover {
            border-color: #ff44aa;
            background: rgba(255, 68, 170, 0.05);
        }

        .upload-area .icon {
            font-size: 4rem;
            color: #00ffcc;
            margin-bottom: 15px;
        }

        .upload-area p {
            font-size: 1.1rem;
            color: #88ddcc;
        }

        .upload-area .sub {
            font-size: 0.85rem;
            color: #6688aa;
            margin-top: 8px;
        }

        #fileInput {
            display: none;
        }

        .upload-progress {
            margin-top: 20px;
            display: none;
        }

        .progress-bar {
            width: 100%;
            height: 6px;
            background: rgba(0, 255, 200, 0.1);
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-bar .fill {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, #00ffcc, #44ddff, #ff44aa);
            border-radius: 10px;
            transition: width 0.3s;
        }

        /* ===== FILE GRID ===== */
        .file-section {
            background: rgba(10, 10, 20, 0.4);
            backdrop-filter: blur(8px);
            border-radius: 25px;
            padding: 25px 30px;
            border: 1px solid rgba(0, 255, 200, 0.05);
        }

        .file-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin-bottom: 25px;
        }

        .file-header h2 {
            font-family: 'Orbitron', monospace;
            font-size: 1.5rem;
            color: #ffdd77;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .file-header .count {
            background: rgba(0, 255, 200, 0.1);
            padding: 4px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            color: #88ddcc;
        }

        .file-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 18px;
        }

        .file-card {
            background: rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(0, 255, 200, 0.08);
            border-radius: 18px;
            padding: 18px 20px;
            display: flex;
            align-items: center;
            gap: 16px;
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }

        .file-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(0, 255, 200, 0.03), transparent);
            opacity: 0;
            transition: opacity 0.4s;
        }

        .file-card:hover::before {
            opacity: 1;
        }

        .file-card:hover {
            transform: translateX(8px);
            border-color: rgba(0, 255, 200, 0.3);
            box-shadow: 0 0 40px rgba(0, 255, 200, 0.05);
        }

        .file-card .file-icon {
            font-size: 2.5rem;
            width: 55px;
            height: 55px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(0, 255, 200, 0.05);
            border-radius: 15px;
            color: #00ffcc;
            flex-shrink: 0;
        }

        .file-card .file-info {
            flex: 1;
            min-width: 0;
        }

        .file-card .file-info .name {
            font-weight: 600;
            font-size: 1rem;
            color: #e0f2fe;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .file-card .file-info .meta {
            font-size: 0.8rem;
            color: #6688aa;
            display: flex;
            gap: 15px;
            margin-top: 4px;
        }

        .file-card .file-actions {
            display: flex;
            gap: 8px;
            flex-shrink: 0;
        }

        .file-card .file-actions button {
            background: none;
            border: 1px solid rgba(0, 255, 200, 0.15);
            color: #88ddcc;
            width: 36px;
            height: 36px;
            border-radius: 12px;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 1rem;
        }

        .file-card .file-actions button:hover {
            background: rgba(0, 255, 200, 0.1);
            border-color: #00ffcc;
            color: #00ffcc;
            transform: scale(1.05);
        }

        .file-card .file-actions button.danger:hover {
            border-color: #ff4466;
            color: #ff4466;
            background: rgba(255, 68, 102, 0.1);
        }

        /* ===== GAMING ELEMENTS ===== */
        .gaming-banner {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 25px 0 30px;
        }

        .game-card {
            background: rgba(10, 10, 20, 0.5);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(0, 255, 200, 0.05);
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
        }

        .game-card:hover {
            transform: scale(1.03);
            border-color: rgba(255, 68, 170, 0.3);
            box-shadow: 0 0 40px rgba(255, 68, 170, 0.05);
        }

        .game-card .emoji {
            font-size: 3rem;
            display: block;
            margin-bottom: 10px;
        }

        .game-card .title {
            font-weight: 600;
            color: #e0f2fe;
        }

        .game-card .desc {
            font-size: 0.8rem;
            color: #6688aa;
            margin-top: 5px;
        }

        /* ===== FOOTER ===== */
        .footer {
            margin-top: 40px;
            padding: 25px;
            text-align: center;
            border-top: 1px solid rgba(0, 255, 200, 0.05);
            color: #6688aa;
            font-size: 0.85rem;
        }

        .footer .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 15px;
        }

        .footer .social-links a {
            color: #6688aa;
            font-size: 1.5rem;
            transition: all 0.3s;
        }

        .footer .social-links a:hover {
            color: #00ffcc;
            transform: translateY(-3px);
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 768px) {
            .logo {
                font-size: 2.5rem;
                letter-spacing: 4px;
            }
            .logo-sub {
                font-size: 0.6rem;
            }
            .owners-display {
                flex-direction: column;
                align-items: center;
                gap: 12px;
            }
            .status-bar {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            .file-grid {
                grid-template-columns: 1fr;
            }
            .header {
                padding: 20px 15px;
            }
            .upload-section {
                padding: 20px 15px;
            }
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .gaming-banner {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 480px) {
            .stats-grid {
                grid-template-columns: 1fr;
            }
            .gaming-banner {
                grid-template-columns: 1fr;
            }
            .file-card {
                flex-wrap: wrap;
            }
            .file-card .file-actions {
                width: 100%;
                justify-content: flex-end;
            }
        }

        /* ===== SCROLLBAR ===== */
        ::-webkit-scrollbar {
            width: 8px;
            background: #0a0a0f;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(180deg, #00ffcc, #ff44aa);
            border-radius: 10px;
        }
        ::-webkit-scrollbar-track {
            background: rgba(0, 0, 0, 0.3);
        }

        /* ===== UTILITY ===== */
        .glow-text {
            text-shadow: 0 0 20px rgba(0, 255, 200, 0.3);
        }
    </style>
</head>
<body>

<!-- ===== ANIMATED BACKGROUND ===== -->
<div class="bg-animation">
    <div class="grid-line"></div>
    <div class="grid-line"></div>
    <div class="grid-line"></div>
    <div class="grid-line"></div>
    <div class="grid-line"></div>
    <div class="particle" style="left: 10%; animation-duration: 18s; animation-delay: 0s;"></div>
    <div class="particle" style="left: 30%; animation-duration: 22s; animation-delay: 3s;"></div>
    <div class="particle" style="left: 50%; animation-duration: 16s; animation-delay: 6s;"></div>
    <div class="particle" style="left: 70%; animation-duration: 20s; animation-delay: 2s;"></div>
    <div class="particle" style="left: 90%; animation-duration: 24s; animation-delay: 8s;"></div>
    <div class="particle" style="left: 15%; animation-duration: 19s; animation-delay: 4s;"></div>
    <div class="particle" style="left: 60%; animation-duration: 21s; animation-delay: 7s;"></div>
</div>

<!-- ===== MAIN CONTAINER ===== -->
<div class="container">

    <!-- ===== HEADER ===== -->
    <header class="header">
        <div class="header-content">
            <div class="logo">MEGAULTRA</div>
            <div class="logo-sub">// GAMING & HACKING HUB //</div>
            
            <div class="badge-container">
                <span class="badge"><i class="fas fa-code"></i> Version 2.0</span>
                <span class="badge gold"><i class="fas fa-trophy"></i> Elite Edition</span>
                <span class="badge"><i class="fas fa-shield-alt"></i> Secure</span>
            </div>

            <div class="owners-display">
                <div class="owner-card">
                    <span class="crown">👑</span>
                    DachAshkan
                </div>
                <div class="owner-card">
                    <span class="crown">👑</span>
                    DachNima
                </div>
            </div>

            <div class="status-bar">
                <span class="status-item">
                    <span class="dot green"></span> Online
                </span>
                <span class="status-item">
                    <i class="fas fa-users"></i> 1,284 Members
                </span>
                <span class="status-item">
                    <i class="fas fa-database"></i> 47 Files
                </span>
                <span class="status-item">
                    <i class="fas fa-gamepad"></i> Gaming Active
                </span>
            </div>
        </div>
    </header>

    <!-- ===== STATS ===== -->
    <div class="stats-grid">
        <div class="stat-card">
            <div class="number">1.2K</div>
            <div class="label"><i class="fas fa-code"></i> Code Snippets</div>
        </div>
        <div class="stat-card">
            <div class="number">894</div>
            <div class="label"><i class="fas fa-bug"></i> Exploits</div>
        </div>
        <div class="stat-card">
            <div class="number">52</div>
            <div class="label"><i class="fas fa-gamepad"></i> Games</div>
        </div>
        <div class="stat-card">
            <div class="number">14.7K</div>
            <div class="label"><i class="fas fa-download"></i> Downloads</div>
        </div>
    </div>

    <!-- ===== GAMING BANNER ===== -->
    <div class="gaming-banner">
        <div class="game-card">
            <span class="emoji">🎮</span>
            <div class="title">Cyber Strike</div>
            <div class="desc">FPS • Online • 128 Players</div>
        </div>
        <div class="game-card">
            <span class="emoji">🕹️</span>
            <div class="title">Neon Racer</div>
            <div class="desc">Racing • Arcade • Multiplayer</div>
        </div>
        <div class="game-card">
            <span class="emoji">⚔️</span>
            <div class="title">Shadow Arena</div>
            <div class="desc">Battle Royale • 4K • HD</div>
        </div>
        <div class="game-card">
            <span class="emoji">🧠</span>
            <div class="title">Code Warriors</div>
            <div class="desc">Programming • Puzzle • 2D</div>
        </div>
    </div>

    <!-- ===== UPLOAD SECTION ===== -->
    <section class="upload-section">
        <h2><i class="fas fa-cloud-upload-alt"></i> Upload Files & Codes</h2>
        <div class="upload-area" id="dropZone">
            <div class="icon"><i class="fas fa-file-upload"></i></div>
            <p><strong>Drop files here</strong> or click to browse</p>
            <div class="sub">Supports: .py, .js, .html, .css, .zip, .txt, .pdf, .exe</div>
            <input type="file" id="fileInput" multiple>
        </div>
        <div class="upload-progress" id="uploadProgress">
            <div style="display: flex; justify-content: space-between; margin-bottom: 8px;">
                <span id="progressText">Uploading...</span>
                <span id="progressPercent">0%</span>
            </div>
            <div class="progress-bar">
                <div class="fill" id="progressFill"></div>
            </div>
        </div>
    </section>

    <!-- ===== FILE SECTION ===== -->
    <section class="file-section">
        <div class="file-header">
            <h2><i class="fas fa-folder-open"></i> File Repository</h2>
            <span class="count" id="fileCount">0 files</span>
        </div>
        <div class="file-grid" id="fileGrid">
            <!-- Sample Files -->
            <div class="file-card" data-file="exploit_ssh.py">
                <div class="file-icon"><i class="fas fa-file-code"></i></div>
                <div class="file-info">
                    <div class="name">exploit_ssh.py</div>
                    <div class="meta">
                        <span>3.2 KB</span>
                        <span>Python</span>
                        <span>2026-07-09</span>
                    </div>
                </div>
                <div class="file-actions">
                    <button onclick="downloadFile(this)"><i class="fas fa-download"></i></button>
                    <button class="danger" onclick="deleteFile(this)"><i class="fas fa-trash"></i></button>
                </div>
            </div>

            <div class="file-card" data-file="tools_2026.zip">
                <div class="file-icon"><i class="fas fa-file-archive"></i></div>
                <div class="file-info">
                    <div class="name">tools_2026.zip</div>
                    <div class="meta">
                        <span>14.8 MB</span>
                        <span>Archive</span>
                        <span>2026-07-08</span>
                    </div>
                </div>
                <div class="file-actions">
                    <button onclick="downloadFile(this)"><i class="fas fa-download"></i></button>
                    <button class="danger" onclick="deleteFile(this)"><i class="fas fa-trash"></i></button>
                </div>
            </div>

            <div class="file-card" data-file="payload_generator.js">
                <div class="file-icon"><i class="fas fa-file-code"></i></div>
                <div class="file-info">
                    <div class="name">payload_generator.js</div>
                    <div class="meta">
                        <span>1.7 KB</span>
                        <span>JavaScript</span>
                        <span>2026-07-07</span>
                    </div>
                </div>
                <div class="file-actions">
                    <button onclick="downloadFile(this)"><i class="fas fa-download"></i></button>
                    <button class="danger" onclick="deleteFile(this)"><i class="fas fa-trash"></i></button>
                </div>
            </div>

            <div class="file-card" data-file="hack_handbook.pdf">
                <div class="file-icon"><i class="fas fa-file-pdf"></i></div>
                <div class="file-info">
                    <div class="name">hack_handbook.pdf</div>
                    <div class="meta">
                        <span>2.1 MB</span>
                        <span>PDF</span>
                        <span>2026-07-06</span>
                    </div>
                </div>
                <div class="file-actions">
                    <button onclick="downloadFile(this)"><i class="fas fa-download"></i></button>
                    <button class="danger" onclick="deleteFile(this)"><i class="fas fa-trash"></i></button>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer class="footer">
        <div class="social-links">
            <a href="#"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-discord"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-telegram"></i></a>
            <a href="#"><i class="fas fa-envelope"></i></a>
        </div>
        <p>
            <i class="fas fa-skull"></i> MegaUltra Gaming & Hacking Hub · 
            <i class="fas fa-terminal"></i> Root Access · 
            <i class="fas fa-gamepad"></i> Gaming Mode
        </p>
        <p style="margin-top: 8px; font-size: 0.75rem; opacity: 0.5;">
            © 2026 DachAshkan & DachNima · All rights reserved for real hackers
        </p>
    </footer>

</div>

<!-- ===== JAVASCRIPT ===== -->
<script>
    (function() {
        'use strict';

        // ===== DOM REFS =====
        const dropZone = document.getElementById('dropZone');
        const fileInput = document.getElementById('fileInput');
        const fileGrid = document.getElementById('fileGrid');
        const fileCount = document.getElementById('fileCount');
        const progressDiv = document.getElementById('uploadProgress');
        const progressFill = document.getElementById('progressFill');
        const progressText = document.getElementById('progressText');
        const progressPercent = document.getElementById('progressPercent');

        // ===== STATE =====
        let fileStore = [];
        let isUploading = false;

        // ===== LOAD FROM LOCALSTORAGE =====
        function loadFromStorage() {
            try {
                const data = localStorage.getItem('megaultra_files_v2');
                if (data) {
                    fileStore = JSON.parse(data);
                    renderFiles();
                }
            } catch (e) {
                console.error('Load error:', e);
            }
        }

        // ===== SAVE TO LOCALSTORAGE =====
        function saveToStorage() {
            try {
                localStorage.setItem('megaultra_files_v2', JSON.stringify(fileStore));
            } catch (e) {
                console.error('Save error:', e);
            }
            updateCount();
        }

        // ===== RENDER FILES =====
        function renderFiles() {
            fileGrid.innerHTML = '';
            if (fileStore.length === 0) {
                fileGrid.innerHTML = `
                    <div style="grid-column: 1/-1; text-align: center; padding: 40px; color: #6688aa;">
                        <i class="fas fa-inbox" style="font-size: 3rem; display: block; margin-bottom: 15px;"></i>
                        No files uploaded yet. Drop some files!
                    </div>
                `;
            } else {
                fileStore.forEach((file, index) => {
                    const card = createFileCard(file, index);
                    fileGrid.appendChild(card);
                });
            }
            updateCount();
        }

        // ===== CREATE FILE CARD =====
        function createFileCard(file, index) {
            const card = document.createElement('div');
            card.className = 'file-card';
            card.dataset.index = index;

            const iconMap = {
                '.py': 'fa-file-code',
                '.js': 'fa-file-code',
                '.html': 'fa-file-code',
                '.css': 'fa-file-code',
                '.zip': 'fa-file-archive',
                '.rar': 'fa-file-
