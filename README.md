<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Семён Юрьевтің дәйексөздері · музыка + таңдаулылар</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            transition: background-color 0.2s ease, border-color 0.2s, color 0.15s;
        }

        /* светлая тема */
        body.theme-light {
            background: linear-gradient(145deg, #f0f2fa 0%, #d9dff0 100%);
            color: #1e1f2b;
        }

        body.theme-light .container {
            background: rgba(245, 248, 255, 0.5);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 25px 50px -8px rgba(0, 0, 0, 0.2);
        }

        body.theme-light h1 {
            background: linear-gradient(120deg, #1d263a, #3f4b73);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        body.theme-light .subhead {
            color: #3f4b6e;
            border-left-color: #2f3d8a;
        }

        body.theme-light .random-block {
            background: rgba(235, 240, 255, 0.5);
            border: 1px solid rgba(0, 0, 0, 0.15);
            box-shadow: 0 12px 30px -15px #6b7c9e;
        }

        body.theme-light .random-label {
            background: #cbd2e9;
            color: #20273f;
            border: 1px solid #9dabcf;
        }

        body.theme-light .quote-large {
            color: #121725;
        }

        body.theme-light .quote-author {
            color: #2e3857;
            border-top-color: #b2bde0;
        }

        body.theme-light .quote-date {
            color: #42507c;
        }

        body.theme-light .btn, body.theme-light .music-btn, body.theme-light .lang-btn {
            background: #cfd7f0;
            color: #101624;
            border: 1px solid #7c89b1;
            box-shadow: 0 6px 12px -8px #2a314d;
        }

        body.theme-light .btn:hover, body.theme-light .music-btn:hover, body.theme-light .lang-btn:hover {
            background: #e1e8ff;
            border-color: #4e6191;
        }

        body.theme-light .section-title {
            color: #202845;
        }

        body.theme-light .quote-card {
            background: #e7ecfd;
            border: 1px solid #b2c0e8;
            box-shadow: 0 8px 0 #a5b1d1;
        }

        body.theme-light .quote-card:hover {
            background: #dce3fc;
            border-color: #6a7bb0;
            box-shadow: 0 12px 0 #97a5cc;
        }

        body.theme-light .quote-card p {
            color: #1b2137;
        }

        body.theme-light .quote-card .author {
            color: #2e3b62;
            border-top-color: #b1bfe4;
        }

        body.theme-light .quote-card .date {
            color: #48588b;
        }

        body.theme-light footer {
            color: #48516e;
        }

        body.theme-light .search-wrapper {
            background: rgba(220, 228, 255, 0.5);
            border-color: #a5b3d9;
        }

        body.theme-light .search-input {
            color: #121826;
        }

        body.theme-light .search-input::placeholder {
            color: #5b6a99;
        }

        body.theme-light .search-icon {
            color: #3d4b7a;
        }

        body.theme-light .search-clear {
            color: #5d6b99;
            background: #ced6f0;
        }

        body.theme-light .search-clear:hover {
            background: #b2beec;
        }

        body.theme-light .search-stats {
            color: #3b4570;
        }

        body.theme-light .no-results {
            color: #33406e;
            background: rgba(180, 198, 255, 0.3);
        }

        /* тёмная тема */
        body.theme-dark {
            background: linear-gradient(145deg, #1a1e2b 0%, #2a2f3f 100%);
            color: #e0e0e0;
        }

        body.theme-dark .container {
            background: rgba(20, 24, 36, 0.5);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.03);
            box-shadow: 0 25px 50px -8px rgba(0, 0, 0, 0.6);
        }

        body.theme-dark h1 {
            background: linear-gradient(120deg, #fff, #b9c7ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        body.theme-dark .subhead {
            color: #8f9bb3;
            border-left-color: #4f7df3;
        }

        body.theme-dark .random-block {
            background: rgba(12, 15, 26, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        body.theme-dark .random-label {
            background: #2d3349;
            color: #aab4d3;
            border: 1px solid #3f465e;
        }

        body.theme-dark .quote-large {
            color: #f0f3ff;
        }

        body.theme-dark .quote-author {
            color: #7f8aa8;
            border-top-color: #2b3042;
        }

        body.theme-dark .quote-date {
            color: #5f6b92;
        }

        body.theme-dark .btn, body.theme-dark .music-btn, body.theme-dark .lang-btn {
            background: #38405f;
            color: white;
            border: 1px solid #545e82;
        }

        body.theme-dark .btn:hover, body.theme-dark .music-btn:hover, body.theme-dark .lang-btn:hover {
            background: #4a5479;
            border-color: #7783b3;
        }

        body.theme-dark .section-title {
            color: #cbd5ff;
        }

        body.theme-dark .quote-card {
            background: #1d212f;
            border: 1px solid #2d3249;
            box-shadow: 0 8px 0 #0e1019;
        }

        body.theme-dark .quote-card:hover {
            background: #232837;
            border-color: #5f6b9b;
        }

        body.theme-dark .quote-card p {
            color: #eaeefb;
        }

        body.theme-dark .quote-card .author {
            color: #7d89b1;
            border-top-color: #2c3149;
        }

        body.theme-dark .quote-card .date {
            color: #5d6b97;
        }

        body.theme-dark footer {
            color: #5d6588;
        }

        body.theme-dark .search-wrapper {
            background: rgba(30, 35, 48, 0.8);
            border-color: #3a405b;
        }

        body.theme-dark .search-input {
            color: #f0f3fd;
        }

        body.theme-dark .search-input::placeholder {
            color: #7b86ab;
        }

        body.theme-dark .search-icon {
            color: #8f9fd5;
        }

        body.theme-dark .search-clear {
            color: #c2ceff;
            background: #2d344d;
        }

        body.theme-dark .search-clear:hover {
            background: #3e4770;
        }

        body.theme-dark .search-stats {
            color: #a0b0da;
        }

        body.theme-dark .no-results {
            color: #bfd0ff;
            background: rgba(45, 55, 90, 0.5);
        }

        /* ЛАЗУРНАЯ ТЕМА */
        body.theme-azure {
            background: linear-gradient(135deg, #8a4fff 0%, #ff6b9d 50%, #ffffff 100%);
            color: #1e1035;
        }

        body.theme-azure .container {
            background: rgba(255, 255, 255, 0.5);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 25px 50px -8px rgba(138, 79, 255, 0.4);
        }

        body.theme-azure h1 {
            background: linear-gradient(120deg, #4a1d8c, #c2185b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        body.theme-azure .subhead {
            color: #4a2c6d;
            border-left-color: #b23c7a;
        }

        body.theme-azure .random-block {
            background: rgba(255, 245, 250, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.8);
            box-shadow: 0 12px 30px -15px #aa6dc9;
        }

        body.theme-azure .random-label {
            background: #e6ccff;
            color: #3f1f6b;
            border: 1px solid #d0a1ff;
        }

        body.theme-azure .quote-large {
            color: #2c104b;
        }

        body.theme-azure .quote-author {
            color: #6a3b8c;
            border-top-color: #dbb5ff;
        }

        body.theme-azure .quote-date {
            color: #a03d6b;
        }

        body.theme-azure .btn, body.theme-azure .music-btn, body.theme-azure .lang-btn {
            background: #e3c9ff;
            color: #2d1152;
            border: 1px solid #c77dff;
            box-shadow: 0 6px 12px -8px #b066d9;
        }

        body.theme-azure .btn:hover, body.theme-azure .music-btn:hover, body.theme-azure .lang-btn:hover {
            background: #f0dcff;
            border-color: #b23c7a;
        }

        body.theme-azure .section-title {
            color: #4a2575;
        }

        body.theme-azure .quote-card {
            background: #f7ecff;
            border: 1px solid #e5baff;
            box-shadow: 0 8px 0 #cf9eff;
        }

        body.theme-azure .quote-card:hover {
            background: #ffe4f7;
            border-color: #c462a5;
            box-shadow: 0 12px 0 #c28eff;
        }

        body.theme-azure .quote-card p {
            color: #26133f;
        }

        body.theme-azure .quote-card .author {
            color: #7a42b3;
            border-top-color: #d9aeff;
        }

        body.theme-azure .quote-card .date {
            color: #b2427c;
        }

        body.theme-azure footer {
            color: #624b85;
        }

        body.theme-azure .search-wrapper {
            background: rgba(255, 240, 255, 0.9);
            border-color: #d8b0ff;
        }

        body.theme-azure .search-input {
            color: #32165c;
        }

        body.theme-azure .search-input::placeholder {
            color: #9b68c9;
        }

        body.theme-azure .search-icon {
            color: #963d9e;
        }

        body.theme-azure .search-clear {
            color: #601a8f;
            background: #e9cdff;
        }

        body.theme-azure .search-clear:hover {
            background: #ddb3ff;
        }

        body.theme-azure .search-stats {
            color: #5a2d82;
        }

        body.theme-azure .no-results {
            color: #501f77;
            background: rgba(255, 215, 245, 0.7);
        }

        /* ВИДЕО ФОН 1 — возьми телефон */
        body.theme-video1 {
            color: #f0f0ff;
        }

        body.theme-video1::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
            z-index: -1;
            pointer-events: none;
        }

        .video1-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -2;
            display: none;
        }

        body.theme-video1 .video1-bg {
            display: block;
        }

        /* ВИДЕО ФОН 2 — скилзскам */
        body.theme-video2 {
            color: #f0f0ff;
        }

        body.theme-video2::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
            z-index: -1;
            pointer-events: none;
        }

        .video2-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -2;
            display: none;
        }

        body.theme-video2 .video2-bg {
            display: block;
        }

        /* ФОТО ФОН */
        body.theme-photo {
            color: #f0f0ff;
        }

        body.theme-photo::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
            z-index: -1;
            pointer-events: none;
        }

        .photo-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -2;
            display: none;
        }

        body.theme-photo .photo-bg {
            display: block;
        }

        /* общие стили для видео и фото тем */
        body.theme-video1 .container,
        body.theme-video2 .container,
        body.theme-photo .container {
            background: rgba(20, 20, 40, 0.4);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 25px 50px -8px rgba(0, 0, 0, 0.7);
        }

        body.theme-video1 h1,
        body.theme-video2 h1,
        body.theme-photo h1 {
            background: linear-gradient(120deg, #ffffff, #d4b5ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        body.theme-video1 .subhead,
        body.theme-video2 .subhead,
        body.theme-photo .subhead {
            color: #cfc2ff;
            border-left-color: #b388ff;
        }

        body.theme-video1 .random-block,
        body.theme-video2 .random-block,
        body.theme-photo .random-block {
            background: rgba(25, 20, 45, 0.4);
            border: 1px solid rgba(255, 255, 255, 0.15);
        }

        body.theme-video1 .random-label,
        body.theme-video2 .random-label,
        body.theme-photo .random-label {
            background: #322b4d;
            color: #d7c9ff;
            border: 1px solid #635291;
        }

        body.theme-video1 .quote-large,
        body.theme-video2 .quote-large,
        body.theme-photo .quote-large {
            color: #ffffff;
        }

        body.theme-video1 .quote-author,
        body.theme-video2 .quote-author,
        body.theme-photo .quote-author {
            color: #c5b2ff;
            border-top-color: #4a3b70;
        }

        body.theme-video1 .quote-date,
        body.theme-video2 .quote-date,
        body.theme-photo .quote-date {
            color: #b39aff;
        }

        body.theme-video1 .btn, body.theme-video1 .music-btn,
        body.theme-video2 .btn, body.theme-video2 .music-btn,
        body.theme-photo .btn, body.theme-photo .music-btn, body.theme-video1 .lang-btn,
        body.theme-video2 .lang-btn, body.theme-photo .lang-btn {
            background: #3e3363;
            color: white;
            border: 1px solid #7a64b0;
        }

        body.theme-video1 .btn:hover, body.theme-video1 .music-btn:hover, body.theme-video1 .lang-btn:hover,
        body.theme-video2 .btn:hover, body.theme-video2 .music-btn:hover, body.theme-video2 .lang-btn:hover,
        body.theme-photo .btn:hover, body.theme-photo .music-btn:hover, body.theme-photo .lang-btn:hover {
            background: #524585;
            border-color: #a58bff;
        }

        body.theme-video1 .section-title,
        body.theme-video2 .section-title,
        body.theme-photo .section-title {
            color: #dbcaff;
        }

        body.theme-video1 .quote-card,
        body.theme-video2 .quote-card,
        body.theme-photo .quote-card {
            background: #26213b;
            border: 1px solid #4a3f6b;
            box-shadow: 0 8px 0 #1e1935;
        }

        body.theme-video1 .quote-card:hover,
        body.theme-video2 .quote-card:hover,
        body.theme-photo .quote-card:hover {
            background: #332d4f;
            border-color: #8573c2;
            box-shadow: 0 12px 0 #262041;
        }

        body.theme-video1 .quote-card p,
        body.theme-video2 .quote-card p,
        body.theme-photo .quote-card p {
            color: #f0eaff;
        }

        body.theme-video1 .quote-card .author,
        body.theme-video2 .quote-card .author,
        body.theme-photo .quote-card .author {
            color: #b9a6ff;
            border-top-color: #53487a;
        }

        body.theme-video1 .quote-card .date,
        body.theme-video2 .quote-card .date,
        body.theme-photo .quote-card .date {
            color: #b19cff;
        }

        body.theme-video1 footer,
        body.theme-video2 footer,
        body.theme-photo footer {
            color: #aaa0cc;
        }

        body.theme-video1 .search-wrapper,
        body.theme-video2 .search-wrapper,
        body.theme-photo .search-wrapper {
            background: rgba(40, 35, 65, 0.8);
            border-color: #6f5ca3;
        }

        body.theme-video1 .search-input,
        body.theme-video2 .search-input,
        body.theme-photo .search-input {
            color: #ffffff;
        }

        body.theme-video1 .search-input::placeholder,
        body.theme-video2 .search-input::placeholder,
        body.theme-photo .search-input::placeholder {
            color: #b3a2e6;
        }

        body.theme-video1 .search-icon,
        body.theme-video2 .search-icon,
        body.theme-photo .search-icon {
            color: #cbb5ff;
        }

        body.theme-video1 .search-clear,
        body.theme-video2 .search-clear,
        body.theme-photo .search-clear {
            color: #ffffff;
            background: #4d4077;
        }

        body.theme-video1 .search-clear:hover,
        body.theme-video2 .search-clear:hover,
        body.theme-photo .search-clear:hover {
            background: #6752a3;
        }

        body.theme-video1 .search-stats,
        body.theme-video2 .search-stats,
        body.theme-photo .search-stats {
            color: #cfc0ff;
        }

        body.theme-video1 .no-results,
        body.theme-video2 .no-results,
        body.theme-photo .no-results {
            color: #dacdff;
            background: rgba(45, 35, 75, 0.7);
        }

        body.theme-video1 .theme-btn.active,
        body.theme-video2 .theme-btn.active,
        body.theme-photo .theme-btn.active {
            background: rgba(170, 130, 255, 0.4);
            border-color: #b79eff;
            color: #ffffff;
        }

        /* общие стили */
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            margin: 0;
            position: relative;
        }

        .container {
            max-width: 1100px;
            width: 100%;
            border-radius: 48px;
            padding: 40px 35px;
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            margin-bottom: 0.25rem;
            line-height: 1.2;
        }

        .subhead {
            font-size: 1.2rem;
            margin-bottom: 30px;
            font-weight: 400;
            padding-left: 20px;
        }

        /* поиск */
        .search-section {
            margin-bottom: 40px;
        }

        .search-wrapper {
            display: flex;
            align-items: center;
            border-radius: 100px;
            padding: 4px 4px 4px 24px;
            border: 1.5px solid;
            transition: 0.1s;
        }

        .search-wrapper:focus-within {
            border-color: #6f8cff;
            box-shadow: 0 0 0 3px rgba(111, 140, 255, 0.3);
        }

        .search-icon {
            font-size: 1.4rem;
            line-height: 1;
            margin-right: 10px;
        }

        .search-input {
            flex: 1;
            background: transparent;
            border: none;
            font-size: 1.2rem;
            padding: 16px 0;
            outline: none;
            font-weight: 400;
        }

        .search-clear {
            border: none;
            background: transparent;
            font-size: 1.3rem;
            cursor: pointer;
            padding: 8px 20px;
            border-radius: 60px;
            font-weight: 500;
            margin-left: 8px;
            transition: 0.1s;
        }

        .search-stats {
            margin-top: 12px;
            margin-left: 20px;
            font-size: 1rem;
            font-weight: 400;
        }

        .random-block {
            border-radius: 32px;
            padding: 35px 30px;
            margin-bottom: 30px;
        }

        .random-label {
            display: inline-block;
            text-transform: uppercase;
            font-size: 0.8rem;
            letter-spacing: 3px;
            padding: 6px 16px;
            border-radius: 40px;
            margin-bottom: 20px;
        }

        .quote-large {
            font-size: 2rem;
            line-height: 1.4;
            font-weight: 450;
            quotes: "«" "»" "„" "“";
            margin-bottom: 15px;
            position: relative;
        }

        .quote-large::before {
            content: "„";
            font-size: 4rem;
            position: absolute;
            left: -25px;
            top: -15px;
            opacity: 0.2;
            font-family: serif;
        }

        .quote-author {
            text-align: right;
            font-size: 1.1rem;
            padding-top: 18px;
            margin-top: 10px;
        }

        .quote-date {
            text-align: right;
            font-size: 0.9rem;
            margin-top: 5px;
            letter-spacing: 0.3px;
        }

        .btn, .music-btn, .sort-btn, .lang-btn {
            border: none;
            font-size: 1rem;
            font-weight: 500;
            padding: 10px 20px;
            border-radius: 60px;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            margin-top: 5px;
        }

        .btn:active, .music-btn:active, .sort-btn:active, .lang-btn:active {
            transform: scale(0.98);
        }

        .theme-switcher {
            display: flex;
            gap: 12px;
            justify-content: flex-end;
            margin-bottom: 25px;
            flex-wrap: wrap;
        }

        .theme-btn, .lang-btn {
            background: transparent;
            border: 1.5px solid currentColor;
            border-radius: 40px;
            padding: 8px 22px;
            font-size: 0.9rem;
            font-weight: 500;
            cursor: pointer;
            opacity: 0.7;
            transition: 0.1s;
            color: inherit;
        }

        .theme-btn.active, .lang-btn.active {
            opacity: 1;
            background: rgba(128, 128, 255, 0.2);
            border-width: 2px;
            font-weight: 600;
        }

        body.theme-light .theme-btn.active, body.theme-light .lang-btn.active {
            background: #bed0ff;
            border-color: #1a1f3c;
            color: #131a30;
        }

        body.theme-azure .theme-btn.active, body.theme-azure .lang-btn.active {
            background: #f2d9ff;
            border-color: #9b4dff;
            color: #2b0d4a;
        }

        .section-title {
            font-size: 2rem;
            font-weight: 500;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .quotes-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 20px;
            min-height: 200px;
        }

        .quote-card {
            border-radius: 24px;
            padding: 24px 20px;
            display: flex;
            flex-direction: column;
            transition: 0.1s ease;
            position: relative;
        }

        .quote-card.favorite {
            border: 2px solid gold;
            box-shadow: 0 0 15px gold;
        }

        .quote-card p {
            font-size: 1.15rem;
            line-height: 1.45;
            flex: 1;
        }

        .quote-card .author {
            margin-top: 20px;
            text-align: right;
            font-size: 0.95rem;
            padding-top: 15px;
            border-top: 1px solid;
        }

        .quote-card .date {
            font-size: 0.85rem;
            text-align: right;
            margin-top: 6px;
        }

        .quote-card .card-actions {
            display: flex;
            justify-content: flex-end;
            gap: 15px;
            margin-top: 15px;
            opacity: 0.7;
        }

        .quote-card .card-actions button {
            background: none;
            border: none;
            font-size: 1.2rem;
            cursor: pointer;
            color: inherit;
        }

        .quote-card .card-actions button:hover {
            transform: scale(1.1);
        }

        .no-results {
            grid-column: 1 / -1;
            text-align: center;
            padding: 60px 20px;
            border-radius: 40px;
            font-size: 1.6rem;
            font-weight: 400;
            border: 2px dashed currentColor;
            opacity: 0.7;
        }

        footer {
            margin-top: 50px;
            text-align: center;
            font-size: 0.9rem;
        }

        /* музыкальный плеер */
        .music-player {
            display: flex;
            align-items: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-top: 20px;
            margin-bottom: 20px;
            padding: 15px 20px;
            border-radius: 60px;
            background: rgba(0,0,0,0.1);
            backdrop-filter: blur(5px);
        }

        .music-btn {
            margin-top: 0;
        }

        /* QR код */
        .qr-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .qr-modal.active {
            display: flex;
        }

        .qr-content {
            background: white;
            padding: 30px;
            border-radius: 30px;
            text-align: center;
            max-width: 400px;
            width: 90%;
        }

        .qr-content.dark {
            background: #1d212f;
            color: white;
        }

        .qr-content.light {
            background: #e7ecfd;
            color: #1e1f2b;
        }

        .qr-content.azure {
            background: #f7ecff;
            color: #2c104b;
        }

        #qrCanvas {
            margin: 20px auto;
            display: block;
            border-radius: 20px;
        }

        .close-qr {
            margin-top: 20px;
            padding: 10px 30px;
            border: none;
            border-radius: 60px;
            cursor: pointer;
            font-size: 1rem;
        }

        /* сортировка */
        .sort-controls {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }

        .sort-btn {
            background: var(--btn-bg, #38405f);
            color: var(--btn-color, white);
            border: 1px solid var(--btn-border, #545e82);
        }

        .sort-btn.active {
            background: #4f7df3;
            border-color: #6f8cff;
        }

        /* переключатель языков */
        .language-switcher {
            display: flex;
            gap: 10px;
            margin-left: 15px;
        }

        /* Медиа-запрос для мобильных устройств */
        @media (max-width: 600px) {
            .container { 
                padding: 25px 18px; 
            }
            h1 { 
                font-size: 2.5rem; 
            }
            .quote-large { 
                font-size: 1.6rem; 
            }
            .search-input { 
                font-size: 1rem; 
            }
            .search-clear { 
                padding: 8px 15px; 
            }
            .language-switcher {
                margin-left: 0;
                margin-top: 10px;
            }
        }
    </style>
    <!-- Библиотека для QR кода -->
    <script src="https://cdn.jsdelivr.net/npm/qrcode@1.5.4/build/qrcode.min.js"></script>
</head>
<body class="theme-dark">
    <!-- ВИДЕО ФОН 1 — возьми телефон -->
    <video class="video1-bg" autoplay muted loop playsinline>
        <source src="videoplayback.mp4" type="video/mp4">
        Ваш браузер не поддерживает видеофон.
    </video>

    <!-- ВИДЕО ФОН 2 — скилзскам -->
    <video class="video2-bg" autoplay muted loop playsinline>
        <source src="2881834453749.mp4" type="video/mp4">
        Ваш браузер не поддерживает видеофон.
    </video>

    <!-- ФОТО ФОН -->
    <img class="photo-bg" src="photo_2026-01-19_23-11-33.jpg" alt="Фоновое изображение">

    <!-- QR модальное окно -->
    <div class="qr-modal" id="qrModal">
        <div class="qr-content" id="qrContent">
            <h3 id="qrQuoteText">Цитата</h3>
            <canvas id="qrCanvas"></canvas>
            <button class="close-qr" id="closeQrBtn">Закрыть</button>
        </div>
    </div>

    <div class="container">
        <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 15px;">
            <h1 id="siteTitle">Семён Юрьев</h1>
            <div style="display: flex; gap: 15px; flex-wrap: wrap;">
                <div class="language-switcher">
                    <button class="lang-btn" id="langRuBtn" data-lang="ru">🇷🇺 Русский</button>
                    <button class="lang-btn" id="langKzBtn" data-lang="kz">🇰🇿 Қазақша</button>
                </div>
                <div class="theme-switcher">
                    <button class="theme-btn" id="themeDarkBtn" data-theme="dark">🌙 тёмная</button>
                    <button class="theme-btn" id="themeLightBtn" data-theme="light">☀️ светлая</button>
                    <button class="theme-btn" id="themeAzureBtn" data-theme="azure">💜 лазурная</button>
                    <button class="theme-btn" id="themeVideo1Btn" data-theme="video1">📱 возьми телефон</button>
                    <button class="theme-btn" id="themeVideo2Btn" data-theme="video2">🎬 скилзскам</button>
                    <button class="theme-btn" id="themePhotoBtn" data-theme="photo">🖼️ фото</button>
                </div>
            </div>
        </div>
        <div class="subhead" id="subheadText">цитаты, которые стали легендой</div>

        <!-- МУЗЫКАЛЬНЫЙ ПЛЕЕР -->
        <div class="music-player">
            <span>🎵 <span id="musicLabel">Музыка:</span></span>
            <audio id="bgMusic" loop autoplay>
                <source src="tisheyurev.mp3" type="audio/mpeg">
                Ваш браузер не поддерживает аудио.
            </audio>
            <button class="music-btn" id="playPauseBtn">⏸️ <span id="pauseLabel">Пауза</span></button>
            <button class="music-btn" id="stopBtn">⏹️ <span id="stopLabel">Стоп</span></button>
            <select id="musicSelect" class="music-btn" style="background: inherit;">
                <option value="tisheyurev.mp3" selected>🎵 tisheyurev.mp3</option>
                <option value="lowtabyurev.mp3">🎵 лоутаб таллин (1).mp3</option>
            </select>
        </div>

        <div class="random-block">
            <div class="random-label" id="randomLabel">случайная мысль</div>
            <div class="quote-large" id="randomQuoteDisplay">—</div>
            <div class="quote-author" id="randomQuoteAuthor">— Семён Юрьев</div>
            <div class="quote-date" id="randomQuoteDate"></div>
            <button class="btn" id="newQuoteBtn">🎲 <span id="newQuoteLabel">Показать другую</span></button>
            <button class="btn" id="copyRandomBtn">📋 <span id="copyLabel">Копировать</span></button>
            <button class="btn" id="shareRandomBtn">📱 <span id="shareLabel">Поделиться</span></button>
            <button class="btn" id="qrRandomBtn">📱 <span id="qrLabel">QR код</span></button>
            <button class="btn" id="favRandomBtn">⭐ <span id="favLabel">В избранное</span></button>
        </div>

        <div class="search-section">
            <div class="search-wrapper">
                <span class="search-icon">🔍</span>
                <input type="text" class="search-input" id="searchInput" placeholder="Поиск по цитатам..." autocomplete="off">
                <button class="search-clear" id="searchClearBtn" title="Очистить">✖ <span id="clearLabel">Очистить</span></button>
            </div>
            <div class="search-stats" id="searchStats">всего цитат: 12</div>
        </div>

        <div class="section-title">
            🗂️ <span id="collectionLabel">Полное собрание</span>
            <span style="font-size: 1rem; opacity: 0.7;" id="resultCount"></span>
            <button class="btn" id="showFavoritesBtn">⭐ <span id="showFavLabel">Показать избранное</span></button>
        </div>

        <!-- Сортировка -->
        <div class="sort-controls">
            <button class="sort-btn" id="sortDateNewBtn">📅 <span id="sortNewLabel">Сначала новые</span></button>
            <button class="sort-btn" id="sortDateOldBtn">📅 <span id="sortOldLabel">Сначала старые</span></button>
        </div>

        <div class="quotes-grid" id="quotesGrid"></div>

        <footer>
            <span id="footerText">© 2026 — сборник высказываний (по мотивам реальных событий)</span>
        </footer>
    </div>

    <script>
        (function() {
            // Массив цитат с добавленной новой фразой
            const quotes = [
                { text: "Я пошумлю, я пошумлю", date: "23.02.2026" },
                { text: "Меня убили через не прошиваемую стенку", date: "23.02.2026" },
                { text: "Это было когда было", date: "23.02.2026" },
                { text: "Я никогда не был охранником лоутаба", date: "15.01.2026" },
                { text: "Да что юрьев то опять", date: "29.12.2025" },
                { text: "Мне не нужны киллы, я хожу на б", date: "30.11.2025" },
                { text: "Вы сказали убрать я сказал убрать", date: "18.12.2025" },
                { text: "Я готовлюсь к контрольной по биологии", date: "10.12.2025" },
                { text: "У меня дела", date: "02.02.2025-н.в" },
                { text: "Казах калайсын купи мне дайсон", date: "01.12.2025-12.01.2025" },
                { text: "Лаки съели собаки", date: "12.12.2025" },
                { text: "Я из другой семьи", date: "25.02.2026" } // Новая цитата
            ];

            // Казахские переводы цитат
            const kzQuotes = [
                { text: "Мен шу шығарамын, мен шу шығарамын", date: "23.02.2026" },
                { text: "Мені өтпейтін қабырға арқылы өлтірді", date: "23.02.2026" },
                { text: "Бұл болған кезде болды", date: "23.02.2026" },
                { text: "Мен ешқашан лоутаб күзетшісі болған емеспін", date: "15.01.2026" },
                { text: "Юрьев тағы не істеді", date: "29.12.2025" },
                { text: "Маған килл қажет емес, мен б-ға барамын", date: "30.11.2025" },
                { text: "Сіз алып тастаңыз дедіңіз, мен алып тастадым", date: "18.12.2025" },
                { text: "Мен биологиядан бақылауға дайындалып жатырмын", date: "10.12.2025" },
                { text: "Менің істерім бар", date: "02.02.2025-қ.б" },
                { text: "Қазақ қалайсың, маған дайсон сатып ал", date: "01.12.2025-12.01.2025" },
                { text: "Лакиді иттер жеп қойды", date: "12.12.2025" },
                { text: "Мен басқа отбасынанмын", date: "25.02.2026" }
            ];

            // Словарь переводов
            const translations = {
                ru: {
                    siteTitle: "Семён Юрьев",
                    subheadText: "цитаты, которые стали легендой",
                    musicLabel: "Музыка:",
                    pauseLabel: "Пауза",
                    stopLabel: "Стоп",
                    randomLabel: "случайная мысль",
                    newQuoteLabel: "Показать другую",
                    copyLabel: "Копировать",
                    shareLabel: "Поделиться",
                    qrLabel: "QR код",
                    favLabel: "В избранное",
                    clearLabel: "Очистить",
                    collectionLabel: "Полное собрание",
                    showFavLabel: "Показать избранное",
                    sortNewLabel: "Сначала новые",
                    sortOldLabel: "Сначала старые",
                    footerText: "© 2026 — сборник высказываний (по мотивам реальных событий)",
                    searchPlaceholder: "Поиск по цитатам...",
                    noResults: "😕 ничего не найдено",
                    author: "— Семён Юрьев",
                    favorites: "в избранном",
                    total: "всего",
                    found: "найдено",
                    shown: "показано",
                    ruBtn: "🇷🇺 Русский",
                    kzBtn: "🇰🇿 Қазақша",
                    copied: "Цитата скопирована!",
                    shareCopied: "Ссылка скопирована в буфер обмена!",
                    qrError: "Не удалось сгенерировать QR код",
                    close: "Закрыть"
                },
                kz: {
                    siteTitle: "Семён Юрьев",
                    subheadText: "аңызға айналған дәйексөздер",
                    musicLabel: "Музыка:",
                    pauseLabel: "Үзіліс",
                    stopLabel: "Тоқтату",
                    randomLabel: "кездейсоқ ой",
                    newQuoteLabel: "Басқасын көрсету",
                    copyLabel: "Көшіру",
                    shareLabel: "Бөлісу",
                    qrLabel: "QR код",
                    favLabel: "Таңдаулыларға",
                    clearLabel: "Тазалау",
                    collectionLabel: "Толық жинақ",
                    showFavLabel: "Таңдаулыларды көрсету",
                    sortNewLabel: "Алдымен жаңалары",
                    sortOldLabel: "Алдымен ескілері",
                    footerText: "© 2026 — дәйексөздер жинағы (нақты оқиғалар негізінде)",
                    searchPlaceholder: "Дәйексөздерден іздеу...",
                    noResults: "😕 ештеңе табылмады",
                    author: "— Семён Юрьев",
                    favorites: "таңдаулыларда",
                    total: "барлығы",
                    found: "табылды",
                    shown: "көрсетілді",
                    ruBtn: "🇷🇺 Русский",
                    kzBtn: "🇰🇿 Қазақша",
                    copied: "Дәйексөз көшірілді!",
                    shareCopied: "Сілтеме алмасу буферіне көшірілді!",
                    qrError: "QR кодты генерациялау мүмкін болмады",
                    close: "Жабу"
                }
            };

            // Текущий язык
            let currentLang = localStorage.getItem('semenLang') || 'ru';

            // Функция парсинга даты для сортировки
            function parseDate(dateStr) {
                if (dateStr.includes('н.в') || dateStr.includes('қ.б')) {
                    return new Date(9999, 11, 31); // Бесконечность для "н.в" или "қ.б"
                }
                if (dateStr.includes('-')) {
                    // Берем первую дату из диапазона
                    dateStr = dateStr.split('-')[0];
                }
                const [day, month, year] = dateStr.split('.');
                return new Date(year, month - 1, day);
            }

            // Избранное (загружаем из localStorage)
            let favorites = JSON.parse(localStorage.getItem('semenFavorites')) || [];

            // Текущая сортировка
            let currentSort = 'new'; // 'new' или 'old'

            // DOM элементы
            const randomQuoteDisplay = document.getElementById('randomQuoteDisplay');
            const randomQuoteDate = document.getElementById('randomQuoteDate');
            const randomQuoteAuthor = document.getElementById('randomQuoteAuthor');
            const newQuoteBtn = document.getElementById('newQuoteBtn');
            const copyRandomBtn = document.getElementById('copyRandomBtn');
            const shareRandomBtn = document.getElementById('shareRandomBtn');
            const qrRandomBtn = document.getElementById('qrRandomBtn');
            const favRandomBtn = document.getElementById('favRandomBtn');
            const quotesGrid = document.getElementById('quotesGrid');
            const showFavoritesBtn = document.getElementById('showFavoritesBtn');

            const themeDarkBtn = document.getElementById('themeDarkBtn');
            const themeLightBtn = document.getElementById('themeLightBtn');
            const themeAzureBtn = document.getElementById('themeAzureBtn');
            const themeVideo1Btn = document.getElementById('themeVideo1Btn');
            const themeVideo2Btn = document.getElementById('themeVideo2Btn');
            const themePhotoBtn = document.getElementById('themePhotoBtn');
            const body = document.body;

            const searchInput = document.getElementById('searchInput');
            const searchClearBtn = document.getElementById('searchClearBtn');
            const searchStats = document.getElementById('searchStats');
            const resultCountSpan = document.getElementById('resultCount');

            // QR элементы
            const qrModal = document.getElementById('qrModal');
            const qrContent = document.getElementById('qrContent');
            const qrQuoteText = document.getElementById('qrQuoteText');
            const qrCanvas = document.getElementById('qrCanvas');
            const closeQrBtn = document.getElementById('closeQrBtn');

            // Кнопки сортировки
            const sortDateNewBtn = document.getElementById('sortDateNewBtn');
            const sortDateOldBtn = document.getElementById('sortDateOldBtn');

            // Кнопки языка
            const langRuBtn = document.getElementById('langRuBtn');
            const langKzBtn = document.getElementById('langKzBtn');

            // Музыкальные элементы
            const bgMusic = document.getElementById('bgMusic');
            const playPauseBtn = document.getElementById('playPauseBtn');
            const stopBtn = document.getElementById('stopBtn');
            const musicSelect = document.getElementById('musicSelect');

            let currentFilter = 'all'; // 'all' или 'favorites'

            // Функция обновления языка
            function setLanguage(lang) {
                currentLang = lang;
                localStorage.setItem('semenLang', lang);
                
                // Обновляем активные кнопки
                langRuBtn.classList.remove('active');
                langKzBtn.classList.remove('active');
                if (lang === 'ru') {
                    langRuBtn.classList.add('active');
                } else {
                    langKzBtn.classList.add('active');
                }
                
                // Обновляем текст на странице
                document.getElementById('siteTitle').textContent = translations[lang].siteTitle;
                document.getElementById('subheadText').textContent = translations[lang].subheadText;
                document.getElementById('musicLabel').textContent = translations[lang].musicLabel;
                document.getElementById('pauseLabel').textContent = translations[lang].pauseLabel;
                document.getElementById('stopLabel').textContent = translations[lang].stopLabel;
                document.getElementById('randomLabel').textContent = translations[lang].randomLabel;
                document.getElementById('newQuoteLabel').textContent = translations[lang].newQuoteLabel;
                document.getElementById('copyLabel').textContent = translations[lang].copyLabel;
                document.getElementById('shareLabel').textContent = translations[lang].shareLabel;
                document.getElementById('qrLabel').textContent = translations[lang].qrLabel;
                document.getElementById('favLabel').textContent = translations[lang].favLabel;
                document.getElementById('clearLabel').textContent = translations[lang].clearLabel;
                document.getElementById('collectionLabel').textContent = translations[lang].collectionLabel;
                document.getElementById('showFavLabel').textContent = translations[lang].showFavLabel;
                document.getElementById('sortNewLabel').textContent = translations[lang].sortNewLabel;
                document.getElementById('sortOldLabel').textContent = translations[lang].sortOldLabel;
                document.getElementById('footerText').textContent = translations[lang].footerText;
                
                // Обновляем placeholder поиска
                searchInput.placeholder = translations[lang].searchPlaceholder;
                
                // Обновляем автора в случайной цитате
                randomQuoteAuthor.textContent = translations[lang].author;
                
                // Перерисовываем сетку цитат
                renderFilteredQuotes(searchInput.value);
            }

            // Обработчики языка
            langRuBtn.addEventListener('click', () => setLanguage('ru'));
            langKzBtn.addEventListener('click', () => setLanguage('kz'));

            // ---- МУЗЫКА ----
            // Попытка автовоспроизведения (может быть заблокировано браузером)
            bgMusic.volume = 0.5;
            bgMusic.play().catch(e => console.log('Автовоспроизведение заблокировано:', e));

            playPauseBtn.addEventListener('click', () => {
                if (bgMusic.paused) {
                    bgMusic.play();
                    playPauseBtn.innerHTML = '⏸️ <span id="pauseLabel">' + translations[currentLang].pauseLabel + '</span>';
                } else {
                    bgMusic.pause();
                    playPauseBtn.innerHTML = '▶️ <span id="pauseLabel">' + translations[currentLang].pauseLabel + '</span>';
                }
            });

            stopBtn.addEventListener('click', () => {
                bgMusic.pause();
                bgMusic.currentTime = 0;
                playPauseBtn.innerHTML = '▶️ <span id="pauseLabel">' + translations[currentLang].pauseLabel + '</span>';
            });

            musicSelect.addEventListener('change', (e) => {
                const wasPlaying = !bgMusic.paused;
                bgMusic.src = e.target.value;
                bgMusic.load();
                if (wasPlaying) {
                    bgMusic.play();
                    playPauseBtn.innerHTML = '⏸️ <span id="pauseLabel">' + translations[currentLang].pauseLabel + '</span>';
                } else {
                    playPauseBtn.innerHTML = '▶️ <span id="pauseLabel">' + translations[currentLang].pauseLabel + '</span>';
                }
            });

            // ---- ТЕМЫ ----
            function setTheme(theme) {
                body.classList.remove('theme-dark', 'theme-light', 'theme-azure', 'theme-video1', 'theme-video2', 'theme-photo');
                body.classList.add(`theme-${theme}`);

                themeDarkBtn.classList.remove('active');
                themeLightBtn.classList.remove('active');
                themeAzureBtn.classList.remove('active');
                themeVideo1Btn.classList.remove('active');
                themeVideo2Btn.classList.remove('active');
                themePhotoBtn.classList.remove('active');
                
                if (theme === 'dark') themeDarkBtn.classList.add('active');
                else if (theme === 'light') themeLightBtn.classList.add('active');
                else if (theme === 'azure') themeAzureBtn.classList.add('active');
                else if (theme === 'video1') themeVideo1Btn.classList.add('active');
                else if (theme === 'video2') themeVideo2Btn.classList.add('active');
                else if (theme === 'photo') themePhotoBtn.classList.add('active');

                // Обновляем класс для QR контента
                qrContent.classList.remove('dark', 'light', 'azure');
                if (theme === 'dark' || theme === 'video1' || theme === 'video2' || theme === 'photo') {
                    qrContent.classList.add('dark');
                } else if (theme === 'light') {
                    qrContent.classList.add('light');
                } else if (theme === 'azure') {
                    qrContent.classList.add('azure');
                }

                localStorage.setItem('semenTheme', theme);
            }

            const savedTheme = localStorage.getItem('semenTheme') || 'dark';
            setTheme(savedTheme);

            themeDarkBtn.addEventListener('click', () => setTheme('dark'));
            themeLightBtn.addEventListener('click', () => setTheme('light'));
            themeAzureBtn.addEventListener('click', () => setTheme('azure'));
            themeVideo1Btn.addEventListener('click', () => setTheme('video1'));
            themeVideo2Btn.addEventListener('click', () => setTheme('video2'));
            themePhotoBtn.addEventListener('click', () => setTheme('photo'));

            // ---- РАБОТА С ИЗБРАННЫМ ----
            function saveFavorites() {
                localStorage.setItem('semenFavorites', JSON.stringify(favorites));
            }

            function isFavorite(quoteText) {
                return favorites.includes(quoteText);
            }

            function toggleFavorite(quoteText) {
                if (isFavorite(quoteText)) {
                    favorites = favorites.filter(f => f !== quoteText);
                } else {
                    favorites.push(quoteText);
                }
                saveFavorites();
                renderFilteredQuotes(searchInput.value);
                updateRandomFavoriteButton();
            }

            // Обновление кнопки в случайной цитате
            function updateRandomFavoriteButton() {
                const currentText = randomQuoteDisplay.textContent.slice(1, -1); // убираем кавычки
                if (isFavorite(currentText)) {
                    favRandomBtn.innerHTML = '⭐ <span id="favLabel">' + translations[currentLang].favLabel.replace('В избранное', 'В избранном') + '</span>';
                } else {
                    favRandomBtn.innerHTML = '⭐ <span id="favLabel">' + translations[currentLang].favLabel + '</span>';
                }
            }

            // Функция сортировки цитат
            function sortQuotes(quotesToSort) {
                return [...quotesToSort].sort((a, b) => {
                    const dateA = parseDate(a.date);
                    const dateB = parseDate(b.date);
                    
                    if (currentSort === 'new') {
                        return dateB - dateA; // Сначала новые
                    } else {
                        return dateA - dateB; // Сначала старые
                    }
                });
            }

            // ---- ОТОБРАЖЕНИЕ ЦИТАТ ----
            function renderFilteredQuotes(filterText = '') {
                const lowerFilter = filterText.toLowerCase().trim();
                
                // Выбираем правильный массив цитат в зависимости от языка
                const currentQuotes = currentLang === 'ru' ? quotes : kzQuotes;
                
                // Сначала фильтруем по поиску
                let filtered = currentQuotes.filter(q => 
                    q.text.toLowerCase().includes(lowerFilter) || 
                    q.date.includes(lowerFilter)
                );

                // Затем по избранному, если включен фильтр
                if (currentFilter === 'favorites') {
                    // Для избранного используем русские тексты для сравнения
                    filtered = filtered.filter((q, index) => favorites.includes(quotes[index].text));
                }

                // Сортируем
                filtered = sortQuotes(filtered);

                quotesGrid.innerHTML = '';

                if (filtered.length === 0) {
                    const noResults = document.createElement('div');
                    noResults.className = 'no-results';
                    noResults.textContent = translations[currentLang].noResults;
                    quotesGrid.appendChild(noResults);
                } else {
                    filtered.forEach((quote, index) => {
                        // Находим оригинальный индекс для избранного
                        const originalIndex = currentQuotes.findIndex(q => q.text === quote.text);
                        const originalQuote = quotes[originalIndex];
                        
                        const card = document.createElement('div');
                        card.className = `quote-card ${isFavorite(originalQuote.text) ? 'favorite' : ''}`;
                        
                        card.innerHTML = `
                            <p>«${quote.text}»</p>
                            <div class="author">${translations[currentLang].author}</div>
                            <div class="date">📅 ${quote.date}</div>
                            <div class="card-actions">
                                <button class="copy-btn" title="Копировать">📋</button>
                                <button class="share-btn" title="Поделиться">📱</button>
                                <button class="qr-btn" title="QR код">📱</button>
                                <button class="fav-btn" title="Избранное">${isFavorite(originalQuote.text) ? '⭐' : '☆'}</button>
                            </div>
                        `;

                        // Кнопка копирования
                        card.querySelector('.copy-btn').addEventListener('click', (e) => {
                            e.stopPropagation();
                            navigator.clipboard.writeText(`«${quote.text}» — Семён Юрьев (${quote.date})`);
                            alert(translations[currentLang].copied);
                        });

                        // Кнопка поделиться
                        card.querySelector('.share-btn').addEventListener('click', (e) => {
                            e.stopPropagation();
                            shareQuote(quote.text, quote.date);
                        });

                        // Кнопка QR кода
                        card.querySelector('.qr-btn').addEventListener('click', (e) => {
                            e.stopPropagation();
                            showQRCode(quote.text, quote.date);
                        });

                        // Кнопка избранного
                        card.querySelector('.fav-btn').addEventListener('click', (e) => {
                            e.stopPropagation();
                            toggleFavorite(originalQuote.text);
                            // Обновляем класс и кнопку
                            if (isFavorite(originalQuote.text)) {
                                card.classList.add('favorite');
                                e.target.textContent = '⭐';
                            } else {
                                card.classList.remove('favorite');
                                e.target.textContent = '☆';
                            }
                        });

                        quotesGrid.appendChild(card);
                    });
                }

                const total = currentQuotes.length;
                const found = filtered.length;
                searchStats.textContent = `${translations[currentLang].total}: ${total} · ${translations[currentLang].found}: ${found} · ${translations[currentLang].favorites}: ${favorites.length}`;
                resultCountSpan.textContent = (found !== total || currentFilter === 'favorites') ? `(${translations[currentLang].shown} ${found})` : '';
            }

            // ---- СЛУЧАЙНАЯ ЦИТАТА ----
            function getRandomIndex() {
                const currentQuotes = currentLang === 'ru' ? quotes : kzQuotes;
                return Math.floor(Math.random() * currentQuotes.length);
            }

            function showRandomQuote() {
                const currentQuotes = currentLang === 'ru' ? quotes : kzQuotes;
                const index = getRandomIndex();
                const quote = currentQuotes[index];
                randomQuoteDisplay.textContent = `«${quote.text}»`;
                randomQuoteAuthor.textContent = translations[currentLang].author;
                randomQuoteDate.textContent = `📅 ${quote.date}`;
                updateRandomFavoriteButton();
                return quote;
            }

            // ---- ПОДЕЛИТЬСЯ ----
            function shareQuote(text, date) {
                const shareText = `«${text}» — Семён Юрьев (${date})`;
                
                if (navigator.share) {
                    navigator.share({
                        title: translations[currentLang].siteTitle,
                        text: shareText,
                        url: window.location.href,
                    }).catch(err => {
                        console.log('Ошибка шаринга:', err);
                    });
                } else {
                    navigator.clipboard.writeText(shareText);
                    alert(translations[currentLang].shareCopied);
                }
            }

            // ---- QR КОД ----
            function showQRCode(text, date) {
                const fullText = `«${text}» — Семён Юрьев (${date})`;
                qrQuoteText.textContent = text.length > 50 ? text.substring(0, 50) + '...' : text;
                
                // Очищаем canvas
                const canvas = document.getElementById('qrCanvas');
                const context = canvas.getContext('2d');
                context.clearRect(0, 0, canvas.width, canvas.height);
                
                // Генерируем QR код
                QRCode.toCanvas(canvas, fullText, { 
                    width: 250,
                    margin: 2,
                    color: {
                        dark: '#000000',
                        light: '#ffffff'
                    }
                }, function(error) {
                    if (error) {
                        console.error('Ошибка генерации QR:', error);
                        alert(translations[currentLang].qrError);
                    } else {
                        qrModal.classList.add('active');
                    }
                });
            }

            // ---- ОБРАБОТЧИКИ ----
            newQuoteBtn.addEventListener('click', () => {
                showRandomQuote();
            });

            copyRandomBtn.addEventListener('click', () => {
                const text = randomQuoteDisplay.textContent + ' ' + randomQuoteAuthor.textContent + ' ' + randomQuoteDate.textContent;
                navigator.clipboard.writeText(text);
                alert(translations[currentLang].copied);
            });

            shareRandomBtn.addEventListener('click', () => {
                const currentText = randomQuoteDisplay.textContent.slice(1, -1);
                const currentDate = randomQuoteDate.textContent.replace('📅 ', '');
                shareQuote(currentText, currentDate);
            });

            qrRandomBtn.addEventListener('click', () => {
                const currentText = randomQuoteDisplay.textContent.slice(1, -1);
                const currentDate = randomQuoteDate.textContent.replace('📅 ', '');
                showQRCode(currentText, currentDate);
            });

            favRandomBtn.addEventListener('click', () => {
                const currentText = randomQuoteDisplay.textContent.slice(1, -1);
                // Находим оригинальный русский текст
                const ruQuote = quotes.find(q => q.text === currentText || 
                    (currentLang === 'kz' && kzQuotes.find(kz => kz.text === currentText) === kzQuotes[quotes.indexOf(q)]));
                
                if (ruQuote) {
                    toggleFavorite(ruQuote.text);
                }
                renderFilteredQuotes(searchInput.value);
            });

            showFavoritesBtn.addEventListener('click', () => {
                if (currentFilter === 'favorites') {
                    currentFilter = 'all';
                    showFavoritesBtn.innerHTML = '⭐ <span id="showFavLabel">' + translations[currentLang].showFavLabel + '</span>';
                } else {
                    currentFilter = 'favorites';
                    showFavoritesBtn.innerHTML = '📋 <span id="showFavLabel">' + translations[currentLang].showFavLabel.replace('Показать избранное', 'Показать всё').replace('Таңдаулыларды көрсету', 'Барлығын көрсету') + '</span>';
                }
                renderFilteredQuotes(searchInput.value);
            });

            // Сортировка
            sortDateNewBtn.addEventListener('click', () => {
                currentSort = 'new';
                sortDateNewBtn.classList.add('active');
                sortDateOldBtn.classList.remove('active');
                renderFilteredQuotes(searchInput.value);
            });

            sortDateOldBtn.addEventListener('click', () => {
                currentSort = 'old';
                sortDateOldBtn.classList.add('active');
                sortDateNewBtn.classList.remove('active');
                renderFilteredQuotes(searchInput.value);
            });

            // Поиск
            function handleSearch() {
                renderFilteredQuotes(searchInput.value);
            }

            searchInput.addEventListener('input', handleSearch);

            searchClearBtn.addEventListener('click', () => {
                searchInput.value = '';
                renderFilteredQuotes('');
                searchInput.focus();
            });

            // Закрытие QR модалки
            closeQrBtn.addEventListener('click', () => {
                qrModal.classList.remove('active');
            });

            qrModal.addEventListener('click', (e) => {
                if (e.target === qrModal) {
                    qrModal.classList.remove('active');
                }
            });

            // ---- ИНИЦИАЛИЗАЦИЯ ----
            // Устанавливаем сохранённый язык или русский по умолчанию
            const savedLang = localStorage.getItem('semenLang') || 'ru';
            setLanguage(savedLang);
            
            showRandomQuote();
            renderFilteredQuotes('');
            
            // Активируем кнопку сортировки по умолчанию
            sortDateNewBtn.classList.add('active');
        })();
    </script>
</body>
</html>
