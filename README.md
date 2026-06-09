# s34858.github.io
ยินดีต้อนรับเข้าสู่เว็บไซต์สะสมผลงานของนายธนวันต์ ด่านซ้าย

     @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700;900&family=Noto+Sans+Thai:wght@300;400;500;700&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: #03020a;
    color: #c8c4e8;
    font-family: 'Noto Sans Thai', sans-serif;
    min-height: 100vh;
}

/* ===== PARTICLES CANVAS ===== */
#particles-canvas {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 0;
}

/* ===== PAGE LAYOUT ===== */
.page {
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1.5rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
    position: relative;
    z-index: 1;
}

/* ===== HEX BORDER SECTION ===== */
.hex-border {
    background: linear-gradient(145deg, #08071a 0%, #0d0b28 60%, #080718 100%);
    border: 1px solid #3a2d8a;
    border-radius: 2px;
    padding: 2.5rem 2rem;
    position: relative;
    overflow: hidden;
    clip-path: polygon(
        12px 0%,
        calc(100% - 12px) 0%,
        100% 12px,
        100% calc(100% - 12px),
        calc(100% - 12px) 100%,
        12px 100%,
        0% calc(100% - 12px),
        0% 12px
    );
    box-shadow:
        0 0 30px rgba(80, 60, 200, 0.12),
        inset 0 0 40px rgba(80, 60, 200, 0.05);
}

/* grid overlay */
.hex-border::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
        repeating-linear-gradient(
            0deg,
            transparent, transparent 34px,
            rgba(80, 60, 180, 0.04) 34px,
            rgba(80, 60, 180, 0.04) 35px
        ),
        repeating-linear-gradient(
            90deg,
            transparent, transparent 34px,
            rgba(80, 60, 180, 0.04) 34px,
            rgba(80, 60, 180, 0.04) 35px
        );
    pointer-events: none;
}

/* scan line */
.hex-border::after {
    content: '';
    position: absolute;
    top: -2px;
    left: 0;
    right: 0;
    height: 2px;
    background: linear-gradient(
        90deg,
        transparent 0%,
        rgba(120, 100, 255, 0.6) 50%,
        transparent 100%
    );
    animation: scan 6s linear infinite;
    pointer-events: none;
}

@keyframes scan {
    0%   { top: -2px; opacity: 0; }
    5%   { opacity: 1; }
    95%  { opacity: 1; }
    100% { top: 100%; opacity: 0; }
}

/* ===== CORNER ACCENTS ===== */
.corner-tl,
.corner-br {
    position: absolute;
    width: 28px;
    height: 28px;
    border-color: #7b65ff;
    border-style: solid;
}

.corner-tl {
    top: 8px;
    left: 8px;
    border-width: 2px 0 0 2px;
}

.corner-br {
    bottom: 8px;
    right: 8px;
    border-width: 0 2px 2px 0;
}

/* ===== SECTION LABEL ===== */
.section-label {
    font-family: 'Cinzel', serif;
    font-size: 10px;
    letter-spacing: 0.3em;
    color: #5e4ec9;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
}

/* ===== RANK BADGE ===== */
.rank-badge {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    letter-spacing: 0.25em;
    color: #a090f0;
    border: 1px solid #3a2d8a;
    padding: 4px 16px;
    display: inline-block;
    margin-bottom: 1.5rem;
    clip-path: polygon(
        8px 0%, calc(100% - 8px) 0%,
        100% 8px, 100% calc(100% - 8px),
        calc(100% - 8px) 100%, 8px 100%,
        0% calc(100% - 8px), 0% 8px
    );
    background: rgba(60, 40, 150, 0.3);
}

/* ===== PROFILE RING ===== */
.profile-ring {
    width: 140px;
    height: 140px;
    border-radius: 50%;
    border: 2px solid #5a46cc;
    box-shadow:
        0 0 20px rgba(90, 70, 200, 0.5),
        inset 0 0 20px rgba(90, 70, 200, 0.1);
    margin: 0 auto 1.5rem;
    overflow: hidden;
    position: relative;
}

.profile-ring img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
}

.no-img {
    display: none;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle at center, #1a1440, #080718);
    color: #7b65ff;
    font-family: 'Cinzel', serif;
    font-size: 12px;
    letter-spacing: 0.2em;
    gap: 4px;
}

.no-img-icon {
    font-size: 28px;
    color: #9080e0;
}

/* ===== COVER SECTION ===== */
#cover {
    text-align: center;
}

#cover h1 {
    font-family: 'Noto Sans Thai', sans-serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: #e8e4ff;
    letter-spacing: 0.05em;
    margin-bottom: 0.4rem;
}

.school {
    color: #7b65ff;
    font-size: 0.9rem;
    letter-spacing: 0.05em;
}

.divider {
    width: 60%;
    height: 1px;
    background: linear-gradient(90deg, transparent, #5a46cc, transparent);
    margin: 1.5rem auto 0;
}

/* ===== HEADINGS ===== */
h2 {
    font-family: 'Noto Sans Thai', sans-serif;
    font-size: 1.1rem;
    font-weight: 500;
    color: #c8c4e8;
    margin-bottom: 1.25rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.h2-icon {
    color: #7b65ff;
    font-size: 1rem;
    filter: drop-shadow(0 0 4px #5a46cc);
}

/* ===== STAT GRID (ประวัติส่วนตัว) ===== */
.stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.75rem;
}

.stat-item {
    background: rgba(30, 20, 70, 0.5);
    border: 1px solid #2a1f6a;
    padding: 0.75rem 1rem;
    clip-path: polygon(
        6px 0%, 100% 0%,
        100% calc(100% - 6px),
        calc(100% - 6px) 100%,
        0% 100%, 0% 6px
    );
    display: flex;
    flex-direction: column;
    gap: 2px;
}

.stat-key {
    font-family: 'Cinzel', serif;
    font-size: 10px;
    color: #5e4ec9;
    letter-spacing: 0.15em;
}

.stat-val {
    font-size: 0.875rem;
    color: #b8b0e0;
    font-weight: 500;
}

/* ===== EDUCATION ROWS ===== */
.edu-row {
    display: flex;
    gap: 1rem;
    padding: 0.75rem 0;
    border-bottom: 1px solid rgba(58, 45, 138, 0.3);
    align-items: center;
}

.edu-row:last-child {
    border-bottom: none;
}

.edu-level {
    font-family: 'Cinzel', serif;
    font-size: 10px;
    color: #7b65ff;
    letter-spacing: 0.1em;
    min-width: 80px;
    padding: 3px 8px;
    border: 1px solid #3a2d8a;
    text-align: center;
    clip-path: polygon(4px 0%, 100% 0%, calc(100% - 4px) 100%, 0% 100%);
    background: rgba(60, 40, 150, 0.2);
}

.edu-school {
    font-size: 0.875rem;
    color: #c8c4e8;
}

/* ===== LISTS (กิจกรรม / ความสามารถ) ===== */
ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
}

ul li {
    padding: 0.6rem 1rem;
    font-size: 0.875rem;
    color: #c8c4e8;
    background: rgba(20, 15, 55, 0.5);
    border-left: 2px solid #5a46cc;
    position: relative;
}

ul li::before {
    content: '◈';
    color: #7b65ff;
    margin-right: 8px;
    font-size: 10px;
}

/* ===== CONTACT ===== */
.contact-item {
    display: flex;
    gap: 1rem;
    padding: 0.7rem 0;
    border-bottom: 1px solid rgba(58, 45, 138, 0.25);
    align-items: center;
}

.contact-item:last-child {
    border-bottom: none;
}

.contact-item .label {
    font-family: 'Cinzel', serif;
    font-size: 10px;
    color: #5e4ec9;
    letter-spacing: 0.12em;
    min-width: 80px;
}

.contact-item span:last-child {
    font-size: 0.875rem;
    color: #a090f0;
}

/* ===== PREFACE ===== */
#preface p {
    font-size: 0.9rem;
    color: #9890c8;
    line-height: 1.9;
}

/* ===== FOOTER ===== */
footer {
    text-align: center;
    padding: 1.5rem 0 0.5rem;
    font-family: 'Cinzel', serif;
    font-size: 11px;
    color: #3a2d8a;
    letter-spacing: 0.2em;
    position: relative;
    z-index: 1;
}

/* ===== RESPONSIVE ===== */
@media (max-width: 480px) {
    .stat-grid {
        grid-template-columns: 1fr;
    }

    #cover h1 {
        font-size: 1.4rem;
    }

    .hex-border {
        padding: 2rem 1.25rem;
    }
}               
