<style>
  /* ===================================================
     RENEGADE AI v5.3 · Cover Page v2
     Light theme · Single-line title · Radar-inspired
     Aligned with index.html & radar archive
     =================================================== */

  /* --- Fonts --- */
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Bebas+Neue&display=swap');

  /* --- Design Tokens: sync with radar index :root.light --- */
  :root {
    --bg:           #f8f9fc;
    --bg2:          #ffffff;
    --surface:      #f0f2f8;
    --card:         #ffffff;
    --border:       #e0e2ec;
    --border-bright:#c0c2d0;
    --text:         #2a2a40;
    --text-muted:   #6a6a80;
    --text-faint:   #a0a0b8;
    --accent:       #e8503a;
    --accent-dim:   rgba(232,80,58,0.08);
    --accent2:      #b88c2a;
    --accent3:      #3a7fbf;
    --accent3-dim:  rgba(74,143,207,0.08);
    --white:        #2a2a40;
    --mono:         'Space Mono', monospace;
    --serif:        'Crimson Pro', Georgia, serif;
    --display:      'Bebas Neue', sans-serif;
    --ease:         cubic-bezier(0.4, 0, 0.2, 1);
  }

  /* --- Global Cover Override --- */
  .cover {
    background: var(--bg) !important;
    background-image: none !important;
    min-height: 100vh !important;
    display: flex !important;
    flex-direction: column !important;
    align-items: center !important;
    justify-content: center !important;
    padding: 64px 48px !important;
    position: relative !important;
    overflow: hidden !important;
    transition: background 0.3s ease !important;
  }

  /* Subtle noise (matching radar light mode: opacity 0.05) */
  .cover::before {
    content: '';
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    opacity: 0.05;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='512' height='512' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
  }

  .cover .cover-main {
    max-width: 920px !important;
    margin: 0 auto !important;
    position: relative !important;
    z-index: 1 !important;
    background: transparent !important;
    width: 100% !important;
  }

  /* =============================================
     HERO STRIP — radar-inspired split layout
     Left: title block  |  Right: stat blocks
     ============================================= */
  .cover-hero {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 0;
    align-items: stretch;
    border-bottom: 1px solid var(--border);
    padding-bottom: 48px;
    margin-bottom: 40px;
  }

  .cover-hero-left {
    padding-right: 64px;
  }

  .cover-hero-right {
    padding-left: 48px;
    border-left: 1px solid var(--border);
    display: flex;
    flex-direction: column;
    gap: 32px;
    align-items: center;
    justify-content: center;
    min-width: 140px;
  }

  /* Stat blocks (radar-style) */
  .cover-stat { text-align: center; }
  .cover-stat .n {
    font-family: var(--display);
    font-size: 3.5rem;
    color: var(--accent);
    line-height: 1;
    display: block;
  }
  .cover-stat .l {
    font-family: var(--mono);
    font-size: 0.56rem;
    letter-spacing: 2.5px;
    color: var(--text-muted);
    text-transform: uppercase;
    display: block;
    margin-top: 4px;
  }
  .cover-stat-divider {
    width: 1px;
    height: 36px;
    background: var(--border);
  }

  /* --- Eyebrow --- */
  .cover-eyebrow {
    font-family: var(--mono);
    font-size: 0.62rem;
    letter-spacing: 4px;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 28px;
    display: flex;
    align-items: center;
    gap: 12px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.1s forwards;
  }
  .cover-eyebrow::before {
    content: '';
    width: 36px;
    height: 1px;
    background: var(--accent);
  }

  /* --- Main Title: RENEGADE AI — single line, very large --- */
  .cover-title {
    font-family: var(--display);
    font-size: clamp(5.5rem, 13vw, 11rem);
    line-height: 0.88;
    color: var(--white);
    letter-spacing: 2px;
    margin: 0 0 6px 0;
    white-space: nowrap;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.2s forwards;
  }
  .cover-title .accent-span { color: var(--accent); }

  /* --- Subtitle --- */
  .cover-subtitle {
    font-family: var(--display);
    font-size: clamp(1.5rem, 3vw, 2.4rem);
    color: var(--text-muted);
    letter-spacing: 3px;
    margin-bottom: 4px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.3s forwards;
  }

  /* --- Version --- */
  .cover-version {
    font-family: var(--mono);
    font-size: 0.62rem;
    letter-spacing: 3px;
    color: var(--text-faint);
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.35s forwards;
  }

  /* =============================================
     BELOW HERO — centered, full-width
     ============================================= */

  .cover-body {
    max-width: 640px;
    margin: 0 auto;
    text-align: left;
  }

  /* --- Quote (pull-quote style) --- */
  .cover-quote {
    margin: 0 0 32px 0;
    padding: 18px 20px 18px 24px;
    border-left: 4px solid var(--accent);
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.4s forwards;
  }
  .cover-quote p {
    font-family: var(--serif);
    font-size: 1.08rem;
    font-style: italic;
    color: var(--text);
    line-height: 1.8;
    margin: 0 0 6px 0 !important;
    text-shadow: none !important;
  }
  .cover-quote .quote-sub {
    font-family: var(--mono);
    font-size: 0.6rem;
    color: var(--text-muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    display: block;
    margin-top: 6px;
  }

  /* --- Meta Tags Row --- */
  .cover-meta-row {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    margin-bottom: 32px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.45s forwards;
  }
  .cover-tag {
    font-family: var(--mono);
    font-size: 0.58rem;
    letter-spacing: 1.5px;
    color: var(--text-muted);
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 5px 12px;
    text-transform: uppercase;
  }

  /* --- Buttons --- */
  .cover-buttons {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-bottom: 52px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.5s forwards;
  }

  .cover a {
    position: relative !important;
    overflow: hidden !important;
    display: inline-flex !important;
    align-items: center !important;
    gap: 8px !important;
    padding: 11px 22px !important;
    margin: 0 !important;
    font-family: var(--mono) !important;
    font-size: 0.62rem !important;
    letter-spacing: 2px !important;
    text-transform: uppercase !important;
    text-decoration: none !important;
    border: 1px solid var(--border-bright) !important;
    background: transparent !important;
    color: var(--text-muted) !important;
    border-radius: 0 !important;
    transition: all 0.25s var(--ease) !important;
    text-shadow: none !important;
    box-shadow: none !important;
  }
  .cover a:hover {
    border-color: var(--accent) !important;
    color: var(--accent) !important;
    background: var(--accent-dim) !important;
    box-shadow: none !important;
  }

  /* --- Status Bar --- */
  .cover-status {
    font-family: var(--mono);
    font-size: 0.58rem;
    color: var(--text-faint);
    letter-spacing: 2px;
    text-align: center;
    line-height: 1.8;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.55s forwards;
  }
  .cover-status .status-dot {
    display: inline-block;
    width: 5px;
    height: 5px;
    background: var(--accent);
    border-radius: 50%;
    margin-right: 6px;
    animation: pulse-dot 2s infinite;
  }

  /* --- Animations --- */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes pulse-dot {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.2; }
  }

  /* --- Responsive --- */
  @media (max-width: 860px) {
    .cover { padding: 48px 28px !important; }
    .cover-hero {
      grid-template-columns: 1fr;
      padding-bottom: 32px;
      margin-bottom: 28px;
    }
    .cover-hero-left {
      padding-right: 0;
      border-bottom: 1px solid var(--border);
      padding-bottom: 28px;
      margin-bottom: 0;
    }
    .cover-hero-right {
      padding-left: 0;
      padding-top: 24px;
      border-left: none;
      flex-direction: row;
      gap: 24px;
      min-width: auto;
    }
    .cover-title {
      font-size: clamp(3rem, 10vw, 5rem);
      white-space: normal;
    }
    .cover-stat-divider { width: 32px; height: 1px; }
    .cover-quote { padding: 14px 12px 14px 16px; }
    .cover-quote p { font-size: 0.92rem; }
    .cover-buttons { flex-direction: column; align-items: flex-start; }
  }

  /* --- Hide default Docsify conflicts --- */
  .cover .mask { display: none !important; }
  .cover.has-mask .mask { display: none !important; }
  .cover h1, .cover h2, .cover blockquote { color: inherit !important; text-shadow: none !important; }
</style>

<!-- =============================================
     HERO STRIP — title + stats (radar layout)
     ============================================= -->

<div class="cover-hero">
  <div class="cover-hero-left">
    <div class="cover-eyebrow">System v5.3 &middot; Meta-Design Apparatus &middot; Brooks Han / HKUST</div>

    <h1 class="cover-title">
      RENE<span class="accent-span">GADE</span>&thinsp;AI
    </h1>

    <p class="cover-subtitle">人类认知进化的催化剂</p>

    <p class="cover-version">v5.3 &middot; CC BY 4.0 &middot; DOI: 10.5281/zenodo.18723061</p>
  </div>

  <div class="cover-hero-right">
    <div class="cover-stat">
      <span class="n">16+</span>
      <span class="l">实证引用</span>
    </div>
    <div class="cover-stat-divider"></div>
    <div class="cover-stat">
      <span class="n">5.3</span>
      <span class="l">进化版</span>
    </div>
    <div class="cover-stat-divider"></div>
    <div class="cover-stat">
      <span class="n">3.5mo</span>
      <span class="l">翻倍周期</span>
    </div>
  </div>
</div>

<!-- =============================================
     BELOW — quote · tags · buttons · status
     ============================================= -->

<div class="cover-body">
  <div class="cover-quote">
    <p>The deepest cage is not monopoly — it is the desire for soma.</p>
    <span class="quote-sub">最深的牢笼不是垄断——而是我们对索麻的渴望</span>
  </div>

  <div class="cover-meta-row">
    <span class="cover-tag">Post-Anthropocentric</span>
    <span class="cover-tag">Evolutionary Biology</span>
    <span class="cover-tag">Political Economy</span>
    <span class="cover-tag">29 Peer-Reviewed</span>
  </div>

  <div class="cover-buttons">
    [← 进入认知摩擦 · Enter Friction](README.md)
    [↗ Zenodo](https://doi.org/10.5281/zenodo.18723061)
    [⌥ GitHub](https://github.com/Brook-Han/Renegade-AI)
  </div>

  <div class="cover-status">
    <span><span class="status-dot"></span>STATUS: [ META_DESIGN_APPARATUS_ACTIVATED · v5.3 ]</span><br>
    <span style="color: var(--text-faint);">NOT A CONTAINER OF CONCLUSIONS — A COGNITIVE DEVICE</span>
  </div>
</div>
