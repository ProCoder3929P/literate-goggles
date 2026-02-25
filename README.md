<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechMateJR | Your Tech Companion</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            /* TechMateJR Brand Colors */
            --primary-color: #2ea6fe; /* The Standard YouTube Red/Blue */
            --accent-color: #00e5ff;  /* Futuristic Cyan for TechMateJR vibe */
            --bg-dark: #0f0f0f;
            --bg-sidebar: #0f0f0f;
            --bg-hover: #1f1f1f;
            --text-main: #ffffff;
            --text-secondary: #aaaaaa;
            --border-color: #2e2e2e;
            --chip-bg: #272727;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            overflow-x: hidden;
            transition: all 0.3s ease;
        }

        /* --- HEADER --- */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            height: 56px;
            background-color: var(--bg-dark);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 16px;
            z-index: 1000;
            border-bottom: 1px solid var(--border-color);
        }

        .left-section {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .logo-container {
            display: flex;
            align-items: center;
            cursor: pointer;
            gap: 4px;
        }

        .logo-icon {
            color: var(--primary-color);
            font-size: 28px;
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .logo-text {
            font-weight: 700;
            font-size: 18px;
            letter-spacing: -0.5px;
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .search-bar {
            display: flex;
            align-items: center;
            flex: 0 1 600px;
            margin-left: 30px;
            gap: 10px;
        }

        .search-input-container {
            display: flex;
            width: 100%;
            border: 1px solid var(--border-color);
            border-radius: 40px 0 0 40px;
            background-color: #121212;
            padding: 0 15px;
            transition: 0.2s;
        }

        .search-input-container:focus-within {
            background-color: #000;
            border-color: var(--primary-color);
            box-shadow: 0 0 10px rgba(46, 166, 254, 0.3);
        }

        .search-input {
            width: 100%;
            background: transparent;
            border: none;
            color: white;
            padding: 10px;
            outline: none;
            font-size: 16px;
        }

        .search-btn {
            width: 64px;
            height: 40px;
            background-color: #222;
            border: 1px solid var(--border-color);
            border-left: none;
            border-radius: 0 40px 40px 0;
            cursor: pointer;
            color: var(--text-main);
            transition: background 0.2s;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .search-btn:hover {
            background-color: #333;
        }

        .mic-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: #181818;
            border: none;
            color: white;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: 0.3s;
        }

        .mic-btn:hover {
            background-color: #333;
            transform: scale(1.1);
        }

        .user-actions {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .icon-btn {
            background: none;
            border: none;
            color: white;
            cursor: pointer;
            font-size: 20px;
            padding: 8px;
            border-radius: 50%;
            transition: background 0.2s;
        }

        .icon-btn:hover {
            background-color: var(--bg-hover);
        }

        .channel-avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background: linear-gradient(135deg, #333, #555);
            overflow: hidden;
            cursor: pointer;
            position: relative;
        }
        
        /* TechMateJR Specific Overlay on Avatar */
        .channel-avatar::after {
            content: "TJ";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 12px;
            font-weight: bold;
            color: white;
        }

        /* --- SIDEBAR --- */
        aside {
            position: fixed;
            top: 56px;
            left: 0;
            width: 72px; /* Collapsed default */
            height: calc(100vh - 56px);
            background-color: var(--bg-sidebar);
            padding: 12px 8px;
            overflow-y: auto;
            transition: width 0.3s ease;
            z-index: 999;
        }

        aside.wide {
            width: 240px;
        }

        .nav-item {
            display: flex;
            align-items: center;
            padding: 12px 16px;
            color: var(--text-main);
            text-decoration: none;
            border-radius: 10px;
            cursor: pointer;
            transition: background 0.2s;
            margin-bottom: 4px;
        }

        .nav-item:hover, .nav-item.active {
            background-color: var(--bg-hover);
        }

        .nav-item i {
            font-size: 24px;
            min-width: 40px;
            text-align: center;
        }

        .nav-text {
            white-space: nowrap;
            overflow: hidden;
            opacity: 1;
            transition: opacity 0.2s;
            margin-left: 12px;
        }

        aside.wide .nav-text {
            opacity: 1;
            font-size: 14px;
        }

        aside:not(.wide) .nav-text {
            display: none;
        }

        .divider {
            height: 1px;
            background-color: var(--border-color);
            margin: 8px 0;
        }

        .channel-sub-header {
            display: flex;
            align-items: center;
            padding: 10px 16px;
            cursor: pointer;
            margin-top: auto;
        }

        .channel-sub-header:hover {
            background-color: var(--bg-hover);
        }

        .sub-avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--accent-color), var(--primary-color));
            margin-right: 12px;
            display: none; /* Hidden when sidebar collapsed */
            color: #000;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            font-size: 14px;
        }
        
        aside.wide .sub-avatar {
            display: flex;
        }

        /* --- MAIN CONTENT --- */
        main {
            margin-top: 56px;
            margin-left: 72px;
            padding: 24px;
            transition: margin-left 0.3s ease;
        }

        main.expanded {
            margin-left: 240px;
        }

        /* Filter Chips */
        .filters-container {
            position: sticky;
            top: 56px;
            z-index: 900;
            background-color: var(--bg-dark);
            padding-bottom: 10px;
            display: flex;
            gap: 12px;
            overflow-x: auto;
            padding-right: 20px;
            scrollbar-width: none;
        }

        .filter-chip {
            background-color: var(--chip-bg);
            color: #d3d3d3;
            padding: 6px 12px;
            border-radius: 18px;
            font-size: 14px;
            font-weight: 500;
            white-space: nowrap;
            cursor: pointer;
            transition: all 0.2s;
            border: 1px solid var(--border-color);
        }

        .filter-chip:hover {
            background-color: #3f3f3f;
        }

        .filter-chip.active {
            background-color: var(--text-main);
            color: var(--bg-dark);
        }

        /* Video Grid */
        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            row-gap: 40px;
        }

        .video-card {
            cursor: pointer;
            transition: transform 0.2s;
        }

        .thumbnail-container {
            position: relative;
            width: 100%;
            aspect-ratio: 16/9;
            border-radius: 12px;
            overflow: hidden;
            background-color: #222;
        }

        .thumbnail-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .video-card:hover .thumbnail-img {
            transform: scale(1.05);
        }

        .duration {
            position: absolute;
            bottom: 8px;
            right: 8px;
            background-color: rgba(0, 0, 0, 0.8);
            padding: 3px 6px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 500;
            color: white;
        }

        .video-info {
            display: flex;
            margin-top: 14px;
            gap: 12px;
        }

        .channel-img {
            width: 36px;
            height: 36px;
            border-radius: 50%;
            object-fit: cover;
        }

        .text-content {
            display: flex;
            flex-direction: column;
        }

        .video-title {
            font-size: 16px;
            font-weight: 500;
            line-height: 1.4;
            margin-bottom: 4px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .channel-name, .video-stats {
            font-size: 14px;
            color: var(--text-secondary);
        }

        .channel-name:hover {
            color: var(--text-main);
        }

        /* TechMateJR Featured Section (About the Channel) */
        .channel-hero {
            background: linear-gradient(135deg, #1a1a1a, #0d0d0d);
            border-radius: 20px;
            padding: 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 40px;
            border: 1px solid var(--border-color);
            position: relative;
            overflow: hidden;
        }

        /* Background decorative circles */
        .channel-hero::before {
            content: '';
            position: absolute;
            top: -50px;
            right: -50px;
            width: 200px;
            height: 200px;
            background: radial-gradient(circle, var(--accent-color) 0%, transparent 70%);
            opacity: 0.2;
        }
        
        .channel-hero::after {
            content: '';
            position: absolute;
            bottom: -20px;
            left: -20px;
            width: 100px;
            height: 100px;
            background: radial-gradient(circle, var(--primary-color) 0%, transparent 70%);
            opacity: 0.2;
        }

        .hero-content h1 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        .hero-content p {
            color: var(--text-secondary);
            max-width: 600px;
            line-height: 1.6;
        }

        .hero-btns {
            display: flex;
            gap: 15px;
        }

        .btn {
            padding: 12px 24px;
            border-radius: 24px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
            border: none;
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: white;
            box-shadow: 0 4px 15px rgba(46, 166, 254, 0.4);
        }

        .btn-primary:hover {
            background-color: #5eb0ff;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: transparent;
            border: 1px solid var(--border-color);
            color: var(--text-main);
        }

        .btn-secondary:hover {
            background-color: var(--bg-hover);
            border-color: #555;
        }

        /* Footer */
        footer {
            margin-top: 60px;
            padding: 40px;
            text-align: center;
            color: var(--text-secondary);
            border-top: 1px solid var(--border-color);
            font-size: 14px;
        }

        /* Responsive Design */
        @media (max-width: 1000px) {
            aside {
                display: none; /* Hide sidebar for tablet simple view */
            }
            main {
                margin-left: 0;
            }
            .search-bar {
                display: none; /* Simplify mobile UI */
            }
        }

        @media (max-width: 768px) {
            .hero-content h1 { font-size: 28px; }
            .video-grid { grid-template-columns: 1fr; }
            .channel-hero { flex-direction: column; text-align: center; gap: 20px; }
            .hero-btns { flex-direction: column; width: 100%; }
            .btn { width: 100%; justify-content: center; }
        }

        /* Floating TechMateJR Badge */
        .floating-badge {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color));
            padding: 15px 25px;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            animation: float 3s ease-in-out infinite;
            z-index: 999;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }

        .badge-text h4 { font-size: 16px; margin:0; }
        .badge-text p { font-size: 12px; margin:0; color: white; font-weight: 300;}
        .badge-icon { color: white; font-size: 24px; }

    </style>
</head>
<body>

    <!-- HEADER -->
    <header>
        <div class="left-section">
            <i class="fa-solid fa-bars" id="sidebar-toggle" style="font-size: 24px; cursor: pointer; color: white;"></i>
            <div class="logo-container" onclick="window.location.reload()">
                <i class="fa-brands fa-youtube logo-icon"></i>
                <span class="logo-text">TechMateJR</span>
            </div>
            
            <div class="search-bar">
                <div class="search-input-container">
                    <input type="text" class="search-input" id="searchBox" placeholder="Search TechMateJR & more...">
                    <button class="search-btn" onclick="simulateSearch()"><i class="fa-solid fa-magnifying-glass"></i></button>
                </div>
                <button class="mic-btn"><i class="fa-solid fa-microphone"></
</body>
</html>
