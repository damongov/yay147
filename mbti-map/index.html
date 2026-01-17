<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yay's MBTI Map</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #0a0a0c;
            --bg-subtle: #111114;
            --bg-card: rgba(255,255,255,0.02);
            --text: #f0ede8;
            --text-muted: #6a6a70;
            --border: rgba(255,255,255,0.06);
            --border-hover: rgba(255,255,255,0.12);
            
            /* Quadrant colors - FJ purple, TP blue */
            --fj: #9B7FB8;
            --fj-glow: rgba(155, 127, 184, 0.12);
            --fp: #D4726A;
            --fp-glow: rgba(212, 114, 106, 0.12);
            --tj: #6B9B7A;
            --tj-glow: rgba(107, 155, 122, 0.12);
            --tp: #5B8FB9;
            --tp-glow: rgba(91, 143, 185, 0.12);
        }

        [data-theme="light"] {
            --bg: #f8f7f4;
            --bg-subtle: #efede8;
            --bg-card: rgba(0,0,0,0.03);
            --text: #1a1a1c;
            --text-muted: #5a5a60;
            --border: rgba(0,0,0,0.1);
            --border-hover: rgba(0,0,0,0.18);
            
            --fj: #6B4F88;
            --fj-glow: rgba(107, 79, 136, 0.22);
            --fp: #B84A42;
            --fp-glow: rgba(184, 74, 66, 0.2);
            --tj: #3A6A4A;
            --tj-glow: rgba(58, 106, 74, 0.2);
            --tp: #3A6A89;
            --tp-glow: rgba(58, 106, 137, 0.22);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Instrument Sans', sans-serif;
            background: var(--bg);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 40px 20px 80px;
            color: var(--text);
            overflow-x: hidden;
            transition: background 0.4s ease, color 0.4s ease;
        }

        /* Subtle grid background */
        body::before {
            content: '';
            position: fixed;
            inset: 0;
            background-image: 
                linear-gradient(var(--border) 1px, transparent 1px),
                linear-gradient(90deg, var(--border) 1px, transparent 1px);
            background-size: 60px 60px;
            pointer-events: none;
            opacity: 0.5;
        }

        /* Theme toggle */
        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 44px;
            height: 44px;
            border: 1px solid var(--border);
            border-radius: 50%;
            background: var(--bg-card);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            z-index: 100;
            backdrop-filter: blur(10px);
        }

        .theme-toggle:hover {
            border-color: var(--border-hover);
            transform: scale(1.05);
        }

        .theme-toggle svg {
            width: 20px;
            height: 20px;
            fill: var(--text-muted);
            transition: fill 0.3s ease;
        }

        .sun-icon { display: none; }
        .moon-icon { display: block; }
        [data-theme="light"] .sun-icon { display: block; }
        [data-theme="light"] .moon-icon { display: none; }

        header {
            text-align: center;
            margin-bottom: 30px;
            animation: fadeDown 0.8s ease-out;
        }

        .header-icon {
            margin-bottom: 16px;
        }

        .header-icon svg {
            width: 56px;
            height: 56px;
            fill: var(--text);
            opacity: 0.8;
        }

        h1 {
            font-family: 'Cormorant Garamond', serif;
            font-size: clamp(2.2rem, 5vw, 3.5rem);
            font-weight: 300;
            letter-spacing: 0.25em;
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 0.7rem;
            letter-spacing: 0.4em;
            color: var(--text-muted);
            text-transform: uppercase;
        }

        /* Filters */
        .filters {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 8px;
            margin-bottom: 40px;
            animation: fadeIn 0.6s ease-out 0.3s both;
        }

        .filter-btn {
            padding: 8px 16px;
            font-family: 'Instrument Sans', sans-serif;
            font-size: 0.72rem;
            font-weight: 500;
            letter-spacing: 0.12em;
            text-transform: uppercase;
            border: 1px solid var(--border);
            border-radius: 20px;
            background: transparent;
            color: var(--text-muted);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .filter-btn:hover {
            border-color: var(--border-hover);
            color: var(--text);
        }

        .filter-btn.active {
            background: var(--text);
            color: var(--bg);
            border-color: var(--text);
        }

        .filter-btn.active:hover {
            opacity: 0.9;
        }

        .map-container {
            position: relative;
            width: min(92vw, 850px);
            aspect-ratio: 1;
            animation: scaleIn 0.7s ease-out 0.2s both;
        }

        /* Main axes */
        .axis {
            position: absolute;
            background: linear-gradient(90deg, transparent, var(--border-hover), transparent);
        }
        .axis-h { width: 100%; height: 1px; top: 50%; }
        .axis-v { 
            width: 1px; height: 100%; left: 50%; 
            background: linear-gradient(180deg, transparent, var(--border-hover), transparent);
        }

        /* Axis labels */
        .axis-label {
            position: absolute;
            font-size: 0.6rem;
            font-weight: 600;
            letter-spacing: 0.3em;
            color: var(--text-muted);
            text-transform: uppercase;
            transition: opacity 0.3s ease;
        }
        .label-f { top: 50%; left: 8px; transform: translateY(-50%); }
        .label-t { top: 50%; right: 8px; transform: translateY(-50%); }
        .label-p { top: 8px; left: 50%; transform: translateX(-50%); }
        .label-j { bottom: 8px; left: 50%; transform: translateX(-50%); }

        /* Quadrants */
        .quadrant {
            position: absolute;
            width: 50%;
            height: 50%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 1fr 1fr;
            gap: 3px;
            padding: 32px 16px 16px;
            transition: opacity 0.4s ease;
        }

        .quadrant.dimmed {
            opacity: 0.15;
        }

        .quadrant-fp { top: 0; left: 0; background: var(--fp-glow); border-radius: 20px 0 0 0; }
        .quadrant-tp { top: 0; right: 0; background: var(--tp-glow); border-radius: 0 20px 0 0; }
        .quadrant-fj { bottom: 0; left: 0; background: var(--fj-glow); border-radius: 0 0 0 20px; }
        .quadrant-tj { bottom: 0; right: 0; background: var(--tj-glow); border-radius: 0 0 20px 0; }

        .quadrant-label {
            position: absolute;
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.2rem;
            font-weight: 600;
            opacity: 0.35;
        }
        .quadrant-fp .quadrant-label { top: 6px; left: 12px; color: var(--fp); }
        .quadrant-tp .quadrant-label { top: 6px; right: 12px; color: var(--tp); }
        .quadrant-fj .quadrant-label { bottom: 6px; left: 12px; color: var(--fj); }
        .quadrant-tj .quadrant-label { bottom: 6px; right: 12px; color: var(--tj); }

        /* Type cells within quadrants */
        .type-cell {
            display: flex;
            flex-direction: column;
            padding: 6px 8px;
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .type-cell:hover {
            background: var(--bg-card);
        }

        .type-cell.dimmed {
            opacity: 0.15;
        }

        .type-code {
            font-size: 0.58rem;
            font-weight: 600;
            letter-spacing: 0.12em;
            margin-bottom: 5px;
            opacity: 0.6;
            text-decoration: none;
            display: inline-block;
            transition: opacity 0.2s ease;
        }

        .type-code:hover {
            opacity: 1;
            text-decoration: underline;
            text-underline-offset: 2px;
        }

        .type-cell.empty .type-code {
            opacity: 0.25;
        }

        .type-cell.empty::after {
            content: '—';
            font-size: 0.65rem;
            color: var(--text-muted);
            opacity: 0.25;
        }

        .person {
            font-size: 0.8rem;
            font-weight: 500;
            line-height: 1.55;
            opacity: 0;
            animation: fadeIn 0.5s ease-out forwards;
            transition: opacity 0.3s ease;
        }

        .person.dimmed {
            opacity: 0.15 !important;
        }

        /* Animation delays */
        .quadrant-fp .type-cell:nth-child(1) .person { animation-delay: 0.3s; }
        .quadrant-fp .type-cell:nth-child(2) .person { animation-delay: 0.35s; }
        .quadrant-fp .type-cell:nth-child(3) .person { animation-delay: 0.4s; }
        .quadrant-fp .type-cell:nth-child(4) .person { animation-delay: 0.45s; }

        .quadrant-tp .type-cell:nth-child(1) .person { animation-delay: 0.4s; }
        .quadrant-tp .type-cell:nth-child(2) .person { animation-delay: 0.45s; }
        .quadrant-tp .type-cell:nth-child(3) .person { animation-delay: 0.5s; }
        .quadrant-tp .type-cell:nth-child(4) .person { animation-delay: 0.55s; }

        .quadrant-fj .type-cell:nth-child(1) .person { animation-delay: 0.5s; }
        .quadrant-fj .type-cell:nth-child(2) .person { animation-delay: 0.55s; }
        .quadrant-fj .type-cell:nth-child(3) .person { animation-delay: 0.6s; }
        .quadrant-fj .type-cell:nth-child(4) .person { animation-delay: 0.65s; }

        .quadrant-tj .type-cell:nth-child(1) .person { animation-delay: 0.6s; }
        .quadrant-tj .type-cell:nth-child(2) .person { animation-delay: 0.65s; }
        .quadrant-tj .type-cell:nth-child(3) .person { animation-delay: 0.7s; }
        .quadrant-tj .type-cell:nth-child(4) .person { animation-delay: 0.75s; }

        /* Color coding */
        .quadrant-fj .type-code { color: var(--fj); }
        .quadrant-fp .type-code { color: var(--fp); }
        .quadrant-tj .type-code { color: var(--tj); }
        .quadrant-tp .type-code { color: var(--tp); }

        /* Center emblem */
        .center {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 58px;
            height: 58px;
            background: var(--bg);
            border: 1px solid var(--border);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10;
            transition: background 0.4s ease, border-color 0.4s ease;
        }

        .center-inner {
            width: 44px;
            height: 44px;
            border: 1px solid var(--border);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Cormorant Garamond', serif;
            font-size: 0.5rem;
            letter-spacing: 0.18em;
            color: var(--text-muted);
        }

        /* Legend */
        .legend {
            margin-top: 45px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px 36px;
            animation: fadeIn 0.8s ease-out 1s both;
        }

        .legend-group {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .legend-title {
            font-size: 0.6rem;
            font-weight: 600;
            letter-spacing: 0.18em;
            text-transform: uppercase;
            opacity: 0.35;
            margin-bottom: 2px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.7rem;
            color: var(--text-muted);
        }

        .legend-dot {
            width: 6px;
            height: 6px;
            border-radius: 50%;
        }

        /* Statistics Section */
        .stats-section {
            margin-top: 50px;
            width: min(92vw, 850px);
            animation: fadeIn 0.8s ease-out 1.2s both;
        }

        .stats-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.4rem;
            font-weight: 400;
            letter-spacing: 0.15em;
            text-align: center;
            margin-bottom: 24px;
            opacity: 0.7;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 12px;
        }

        .stat-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 16px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            border-color: var(--border-hover);
            transform: translateY(-2px);
        }

        .stat-number {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2rem;
            font-weight: 600;
            line-height: 1;
            margin-bottom: 4px;
        }

        .stat-label {
            font-size: 0.65rem;
            font-weight: 500;
            letter-spacing: 0.15em;
            text-transform: uppercase;
            color: var(--text-muted);
        }

        .stat-bar {
            margin-top: 10px;
            height: 4px;
            background: var(--border);
            border-radius: 2px;
            overflow: hidden;
        }

        .stat-bar-fill {
            height: 100%;
            border-radius: 2px;
            transition: width 0.6s ease;
        }

        .stat-card.fj .stat-number { color: var(--fj); }
        .stat-card.fp .stat-number { color: var(--fp); }
        .stat-card.tj .stat-number { color: var(--tj); }
        .stat-card.tp .stat-number { color: var(--tp); }
        .stat-card.fj .stat-bar-fill { background: var(--fj); }
        .stat-card.fp .stat-bar-fill { background: var(--fp); }
        .stat-card.tj .stat-bar-fill { background: var(--tj); }
        .stat-card.tp .stat-bar-fill { background: var(--tp); }

        .stat-card.feelers .stat-number { color: var(--fp); }
        .stat-card.thinkers .stat-number { color: var(--tp); }
        .stat-card.judgers .stat-number { color: var(--fj); }
        .stat-card.perceivers .stat-number { color: var(--fp); }
        .stat-card.intuitives .stat-number { color: var(--fj); }
        .stat-card.sensors .stat-number { color: var(--tj); }
        .stat-card.introverts .stat-number { color: var(--text-muted); }
        .stat-card.extroverts .stat-number { color: var(--text); }

        .stat-card.feelers .stat-bar-fill { background: linear-gradient(90deg, var(--fj), var(--fp)); }
        .stat-card.thinkers .stat-bar-fill { background: linear-gradient(90deg, var(--tj), var(--tp)); }
        .stat-card.judgers .stat-bar-fill { background: linear-gradient(90deg, var(--fj), var(--tj)); }
        .stat-card.perceivers .stat-bar-fill { background: linear-gradient(90deg, var(--fp), var(--tp)); }
        .stat-card.intuitives .stat-bar-fill { background: var(--fj); }
        .stat-card.sensors .stat-bar-fill { background: var(--tj); }
        .stat-card.introverts .stat-bar-fill { background: var(--text-muted); }
        .stat-card.extroverts .stat-bar-fill { background: var(--text); }

        .stats-divider {
            grid-column: 1 / -1;
            height: 1px;
            background: var(--border);
            margin: 8px 0;
        }

        @keyframes fadeDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes scaleIn {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Responsive */
        @media (max-width: 600px) {
            .quadrant { padding: 26px 8px 10px; }
            .type-code { font-size: 0.48rem; }
            .person { font-size: 0.68rem; line-height: 1.45; }
            .quadrant-label { font-size: 0.95rem; }
            .filter-btn { padding: 6px 12px; font-size: 0.65rem; }
            .theme-toggle { width: 38px; height: 38px; top: 14px; right: 14px; }
        }
    </style>
</head>
<body>
    <!-- Theme Toggle -->
    <button class="theme-toggle" onclick="toggleTheme()" aria-label="Toggle theme">
        <svg class="moon-icon" viewBox="0 0 24 24"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>
        <svg class="sun-icon" viewBox="0 0 24 24"><circle cx="12" cy="12" r="5"/><line x1="12" y1="1" x2="12" y2="3" stroke="currentColor" stroke-width="2"/><line x1="12" y1="21" x2="12" y2="23" stroke="currentColor" stroke-width="2"/><line x1="4.22" y1="4.22" x2="5.64" y2="5.64" stroke="currentColor" stroke-width="2"/><line x1="18.36" y1="18.36" x2="19.78" y2="19.78" stroke="currentColor" stroke-width="2"/><line x1="1" y1="12" x2="3" y2="12" stroke="currentColor" stroke-width="2"/><line x1="21" y1="12" x2="23" y2="12" stroke="currentColor" stroke-width="2"/><line x1="4.22" y1="19.78" x2="5.64" y2="18.36" stroke="currentColor" stroke-width="2"/><line x1="18.36" y1="5.64" x2="19.78" y2="4.22" stroke="currentColor" stroke-width="2"/></svg>
    </button>

    <header>
        <div class="header-icon">
            <!-- Elegant goose silhouette -->
            <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg">
                <!-- Goose body -->
                <ellipse cx="28" cy="42" rx="16" ry="12" opacity="0.95"/>
                <!-- Goose neck -->
                <path d="M38 38 Q42 32, 40 22 Q39 16, 36 12" stroke="currentColor" stroke-width="6" fill="none" stroke-linecap="round"/>
                <!-- Goose head -->
                <circle cx="35" cy="11" r="5"/>
                <!-- Beak -->
                <path d="M40 11 L48 10 L46 12 L40 12 Z" />
                <!-- Eye -->
                <circle cx="36" cy="10" r="1.2" fill="var(--bg)"/>
                <!-- Tail feathers -->
                <path d="M12 40 Q8 38, 6 42 Q8 44, 12 43" opacity="0.9"/>
                <path d="M12 42 Q7 41, 4 46 Q7 47, 12 45" opacity="0.85"/>
                <!-- Wing detail -->
                <ellipse cx="26" cy="40" rx="8" ry="5" fill="var(--bg)" opacity="0.15"/>
                <!-- Legs -->
                <path d="M24 52 L22 58 M20 58 L24 58" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
                <path d="M32 52 L34 58 M32 58 L36 58" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
            </svg>
        </div>
        <h1>YAY'S MBTI</h1>
        <div class="subtitle">Personality Type Mapping</div>
    </header>

    <!-- Filters -->
    <div class="filters">
        <button class="filter-btn active" data-filter="all">All</button>
        <button class="filter-btn" data-filter="F">Feelers</button>
        <button class="filter-btn" data-filter="T">Thinkers</button>
        <button class="filter-btn" data-filter="N">Intuitives</button>
        <button class="filter-btn" data-filter="S">Sensors</button>
        <button class="filter-btn" data-filter="J">Judgers</button>
        <button class="filter-btn" data-filter="P">Perceivers</button>
    </div>

    <div class="map-container">
        <div class="axis axis-h"></div>
        <div class="axis axis-v"></div>

        <span class="axis-label label-f">Feeling</span>
        <span class="axis-label label-t">Thinking</span>
        <span class="axis-label label-p">Perceiving</span>
        <span class="axis-label label-j">Judging</span>

        <!-- FP Quadrant (top-left: Feeling + Perceiving) -->
        <div class="quadrant quadrant-fp" data-quadrant="FP">
            <span class="quadrant-label">FP</span>
            
            <div class="type-cell" data-type="INFP">
                <a href="https://www.16personalities.com/infp-personality" target="_blank" class="type-code">INFP</a>
                <span class="person" data-mbti="INFP">Rascal</span>
                <span class="person" data-mbti="INFP">Lavender</span>
                <span class="person" data-mbti="INFP">Corpse Bride</span>
            </div>
            <div class="type-cell" data-type="ENFP">
                <a href="https://www.16personalities.com/enfp-personality" target="_blank" class="type-code">ENFP</a>
                <span class="person" data-mbti="ENFP">Mollies</span>
            </div>
            <div class="type-cell" data-type="ISFP">
                <a href="https://www.16personalities.com/isfp-personality" target="_blank" class="type-code">ISFP</a>
                <span class="person" data-mbti="ISFP">Maki</span>
                <span class="person" data-mbti="ISFP">Aria</span>
                <span class="person" data-mbti="ISFP">Alita</span>
            </div>
            <div class="type-cell" data-type="ESFP">
                <a href="https://www.16personalities.com/esfp-personality" target="_blank" class="type-code">ESFP</a>
                <span class="person" data-mbti="ESFP">Gogo</span>
            </div>
        </div>

        <!-- TP Quadrant (top-right: Thinking + Perceiving) -->
        <div class="quadrant quadrant-tp" data-quadrant="TP">
            <span class="quadrant-label">TP</span>
            
            <div class="type-cell" data-type="INTP">
                <a href="https://www.16personalities.com/intp-personality" target="_blank" class="type-code">INTP</a>
                <span class="person" data-mbti="INTP">Ferrinh</span>
            </div>
            <div class="type-cell" data-type="ENTP">
                <a href="https://www.16personalities.com/entp-personality" target="_blank" class="type-code">ENTP</a>
                <span class="person" data-mbti="ENTP">Nel</span>
            </div>
            <div class="type-cell empty" data-type="ISTP">
                <a href="https://www.16personalities.com/istp-personality" target="_blank" class="type-code">ISTP</a>
            </div>
            <div class="type-cell" data-type="ESTP">
                <a href="https://www.16personalities.com/estp-personality" target="_blank" class="type-code">ESTP</a>
                <span class="person" data-mbti="ESTP">Whiskey</span>
            </div>
        </div>

        <!-- FJ Quadrant (bottom-left: Feeling + Judging) -->
        <div class="quadrant quadrant-fj" data-quadrant="FJ">
            <span class="quadrant-label">FJ</span>
            
            <div class="type-cell" data-type="INFJ">
                <a href="https://www.16personalities.com/infj-personality" target="_blank" class="type-code">INFJ</a>
                <span class="person" data-mbti="INFJ">Elvira</span>
                <span class="person" data-mbti="INFJ">Karma</span>
            </div>
            <div class="type-cell" data-type="ENFJ">
                <a href="https://www.16personalities.com/enfj-personality" target="_blank" class="type-code">ENFJ</a>
                <span class="person" data-mbti="ENFJ">Babs</span>
            </div>
            <div class="type-cell" data-type="ISFJ">
                <a href="https://www.16personalities.com/isfj-personality" target="_blank" class="type-code">ISFJ</a>
                <span class="person" data-mbti="ISFJ">Remy</span>
            </div>
            <div class="type-cell" data-type="ESFJ">
                <a href="https://www.16personalities.com/esfj-personality" target="_blank" class="type-code">ESFJ</a>
                <span class="person" data-mbti="ESFJ">Leif</span>
                <span class="person" data-mbti="ESFJ">Ji Soo</span>
            </div>
        </div>

        <!-- TJ Quadrant (bottom-right: Thinking + Judging) -->
        <div class="quadrant quadrant-tj" data-quadrant="TJ">
            <span class="quadrant-label">TJ</span>
            
            <div class="type-cell" data-type="INTJ">
                <a href="https://www.16personalities.com/intj-personality" target="_blank" class="type-code">INTJ</a>
                <span class="person" data-mbti="INTJ">Atlas</span>
                <span class="person" data-mbti="INTJ">Diss</span>
            </div>
            <div class="type-cell" data-type="ENTJ">
                <a href="https://www.16personalities.com/entj-personality" target="_blank" class="type-code">ENTJ</a>
                <span class="person" data-mbti="ENTJ">Damon</span>
            </div>
            <div class="type-cell empty" data-type="ISTJ">
                <a href="https://www.16personalities.com/istj-personality" target="_blank" class="type-code">ISTJ</a>
            </div>
            <div class="type-cell empty" data-type="ESTJ">
                <a href="https://www.16personalities.com/estj-personality" target="_blank" class="type-code">ESTJ</a>
            </div>
        </div>

        <div class="center">
            <div class="center-inner">MBTI</div>
        </div>
    </div>

    <div class="legend">
        <div class="legend-group">
            <div class="legend-title">Quadrants</div>
            <div class="legend-item"><span class="legend-dot" style="background: var(--fp)"></span> FP — Feeling + Perceiving</div>
            <div class="legend-item"><span class="legend-dot" style="background: var(--tp)"></span> TP — Thinking + Perceiving</div>
            <div class="legend-item"><span class="legend-dot" style="background: var(--fj)"></span> FJ — Feeling + Judging</div>
            <div class="legend-item"><span class="legend-dot" style="background: var(--tj)"></span> TJ — Thinking + Judging</div>
        </div>
        <div class="legend-group">
            <div class="legend-title">Axes</div>
            <div class="legend-item">I/E — Introverted / Extroverted</div>
            <div class="legend-item">N/S — Intuitive / Sensing</div>
        </div>
        <div class="legend-group">
            <div class="legend-title">Total</div>
            <div class="legend-item" style="font-size: 1.1rem; font-weight: 600;">20 people mapped</div>
        </div>
    </div>

    <!-- Statistics Section -->
    <div class="stats-section">
        <div class="stats-title">STATISTICS</div>
        <div class="stats-grid">
            <!-- Quadrant stats -->
            <div class="stat-card fj">
                <div class="stat-number">6</div>
                <div class="stat-label">FJ Types</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 30%"></div></div>
            </div>
            <div class="stat-card fp">
                <div class="stat-number">8</div>
                <div class="stat-label">FP Types</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 40%"></div></div>
            </div>
            <div class="stat-card tj">
                <div class="stat-number">3</div>
                <div class="stat-label">TJ Types</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 15%"></div></div>
            </div>
            <div class="stat-card tp">
                <div class="stat-number">3</div>
                <div class="stat-label">TP Types</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 15%"></div></div>
            </div>
            
            <div class="stats-divider"></div>
            
            <!-- Dichotomy stats -->
            <div class="stat-card feelers">
                <div class="stat-number">14</div>
                <div class="stat-label">Feelers (F)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 70%"></div></div>
            </div>
            <div class="stat-card thinkers">
                <div class="stat-number">6</div>
                <div class="stat-label">Thinkers (T)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 30%"></div></div>
            </div>
            <div class="stat-card judgers">
                <div class="stat-number">9</div>
                <div class="stat-label">Judgers (J)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 45%"></div></div>
            </div>
            <div class="stat-card perceivers">
                <div class="stat-number">11</div>
                <div class="stat-label">Perceivers (P)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 55%"></div></div>
            </div>
            
            <div class="stats-divider"></div>
            
            <div class="stat-card intuitives">
                <div class="stat-number">12</div>
                <div class="stat-label">Intuitives (N)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 60%"></div></div>
            </div>
            <div class="stat-card sensors">
                <div class="stat-number">8</div>
                <div class="stat-label">Sensors (S)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 40%"></div></div>
            </div>
            <div class="stat-card introverts">
                <div class="stat-number">13</div>
                <div class="stat-label">Introverts (I)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 65%"></div></div>
            </div>
            <div class="stat-card extroverts">
                <div class="stat-number">7</div>
                <div class="stat-label">Extroverts (E)</div>
                <div class="stat-bar"><div class="stat-bar-fill" style="width: 35%"></div></div>
            </div>
        </div>
    </div>

    <script>
        // Theme toggle
        function toggleTheme() {
            const html = document.documentElement;
            const currentTheme = html.getAttribute('data-theme');
            const newTheme = currentTheme === 'light' ? 'dark' : 'light';
            html.setAttribute('data-theme', newTheme);
            localStorage.setItem('theme', newTheme);
        }

        // Load saved theme
        const savedTheme = localStorage.getItem('theme') || 'dark';
        document.documentElement.setAttribute('data-theme', savedTheme);

        // Filter functionality
        const filterBtns = document.querySelectorAll('.filter-btn');
        const quadrants = document.querySelectorAll('.quadrant');
        const typeCells = document.querySelectorAll('.type-cell');
        const persons = document.querySelectorAll('.person');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Update active button
                filterBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');

                const filter = btn.dataset.filter;

                if (filter === 'all') {
                    // Show everything
                    quadrants.forEach(q => q.classList.remove('dimmed'));
                    typeCells.forEach(c => c.classList.remove('dimmed'));
                    persons.forEach(p => p.classList.remove('dimmed'));
                } else {
                    // Apply filter
                    typeCells.forEach(cell => {
                        const type = cell.dataset.type;
                        const matches = type.includes(filter);
                        cell.classList.toggle('dimmed', !matches);
                    });

                    persons.forEach(person => {
                        const mbti = person.dataset.mbti;
                        const matches = mbti && mbti.includes(filter);
                        person.classList.toggle('dimmed', !matches);
                    });

                    // Dim quadrants that have no matching types
                    quadrants.forEach(quadrant => {
                        const quadrantType = quadrant.dataset.quadrant;
                        let hasMatch = false;
                        
                        // Check if any letter in the filter matches the quadrant
                        if (filter === 'F' && (quadrantType === 'FJ' || quadrantType === 'FP')) hasMatch = true;
                        if (filter === 'T' && (quadrantType === 'TJ' || quadrantType === 'TP')) hasMatch = true;
                        if (filter === 'J' && (quadrantType === 'FJ' || quadrantType === 'TJ')) hasMatch = true;
                        if (filter === 'P' && (quadrantType === 'FP' || quadrantType === 'TP')) hasMatch = true;
                        if (filter === 'N' || filter === 'S') hasMatch = true; // These span all quadrants
                        
                        quadrant.classList.toggle('dimmed', !hasMatch);
                    });
                }
            });
        });
    </script>
</body>
</html>
