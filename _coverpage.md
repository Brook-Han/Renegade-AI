<style>
  /* ===================================================
     RENEGADE AI v5.3 · Cover Page
     Design aligned with landing page (index.html v5.3)
     Fonts, colors, and visual language match the web page
     =================================================== */

  /* --- Font Imports --- */
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Bebas+Neue&display=swap');

  /* --- Design Tokens (matches web page :root) --- */
  :root {
    --bg: #08080e;
    --bg2: #0d0d18;
    --surface: #111120;
    --card: #13131f;
    --border: #1e1e30;
    --border-bright: #2e2e50;
    --text: #cccce0;
    --text-muted: #6868a0;
    --text-faint: #3a3a5a;
    --accent: #e8503a;
    --accent-dim: rgba(232,80,58,0.12);
    --accent2: #c9a040;
    --accent3: #4a8fcf;
    --white: #f0f0f8;
    --mono: 'Space Mono', monospace;
    --serif: 'Crimson Pro', Georgia, serif;
    --display: 'Bebas Neue', sans-serif;
    --ease: cubic-bezier(0.4, 0, 0.2, 1);
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
    padding: 60px 40px !important;
    position: relative !important;
    overflow: hidden !important;
  }

  /* --- Noise Texture Overlay (matches web page) --- */
  .cover::before {
    content: '';
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    opacity: 0.025;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='512' height='512' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
  }

  /* --- Remove default Docsify cover backgrounds --- */
  .cover .cover-main {
    max-width: 800px !important;
    margin: 0 auto !important;
    position: relative !important;
    z-index: 1 !important;
    background: transparent !important;
  }

  /* --- Eyebrow Line --- */
  .cover-eyebrow {
    font-family: var(--mono);
    font-size: 0.65rem;
    letter-spacing: 4px;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 32px;
    display: flex;
    align-items: center;
    gap: 12px;
    justify-content: center;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.1s forwards;
  }
  .cover-eyebrow::before,
  .cover-eyebrow::after {
    content: '';
    width: 40px;
    height: 1px;
    background: var(--accent);
  }

  /* --- Main Title: RENEGADE AI --- */
  .cover-title {
    font-family: var(--display);
    font-size: clamp(5rem, 12vw, 10rem);
    line-height: 0.9;
    color: var(--white);
    letter-spacing: 2px;
    margin-bottom: 6px;
    text-align: center;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.2s forwards;
  }
  .cover-title .accent-span {
    color: var(--accent);
  }

  /* --- Subtitle --- */
  .cover-subtitle {
    font-family: var(--display);
    font-size: clamp(1.2rem, 2.5vw, 2rem);
    color: var(--text-muted);
    letter-spacing: 3px;
    text-align: center;
    margin-bottom: 8px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.3s forwards;
  }

  /* --- Version Badge --- */
  .cover-version {
    font-family: var(--mono);
    font-size: 0.6rem;
    letter-spacing: 3px;
    color: var(--text-faint);
    text-align: center;
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.35s forwards;
  }

  /* --- Quote (styled like web page pull-quote) --- */
  .cover-quote {
    max-width: 600px;
    margin: 0 auto 44px auto;
    padding: 24px 28px 24px 32px;
    border-left: 4px solid var(--accent);
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.4s forwards;
  }
  .cover-quote p {
    font-family: var(--serif);
    font-size: 1.1rem;
    font-style: italic;
    color: var(--text);
    line-height: 1.8;
    margin: 0 0 8px 0 !important;
    text-shadow: none !important;
  }
  .cover-quote .quote-sub {
    font-family: var(--mono);
    font-size: 0.62rem;
    color: var(--text-muted);
    letter-spacing: 2.5px;
    text-transform: uppercase;
    display: block;
    margin-top: 8px;
  }

  /* --- Meta Tags Row (matches hero-tag style) --- */
  .cover-meta-row {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 36px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.45s forwards;
  }
  .cover-tag {
    font-family: var(--mono);
    font-size: 0.6rem;
    letter-spacing: 1.5px;
    color: var(--text-muted);
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 5px 12px;
    text-transform: uppercase;
  }

  /* --- Buttons (match web page ghost buttons) --- */
  .cover-buttons {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 60px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.5s forwards;
  }

  /* Override Docsify default button styles completely */
  .cover a {
    position: relative !important;
    overflow: hidden !important;
    display: inline-flex !important;
    align-items: center !important;
    gap: 8px !important;
    padding: 11px 22px !important;
    margin: 0 !important;
    font-family: var(--mono) !important;
    font-size: 0.65rem !important;
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

  /* --- Status Bar (matches web page) --- */
  .cover-status {
    font-family: var(--mono);
    font-size: 0.6rem;
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
  @media (max-width: 768px) {
    .cover { padding: 40px 20px !important; }
    .cover-quote { padding: 18px 16px 18px 20px; }
    .cover-quote p { font-size: 0.95rem; }
    .cover-buttons { flex-direction: column; align-items: center; }
  }

  /* --- Hide default Docsify cover mask/content that conflicts --- */
  .cover .mask { display: none !important; }
  .cover.has-mask .mask { display: none !important; }
  .cover h1, .cover h2, .cover blockquote { color: inherit !important; text-shadow: none !important; }
</style>

<!-- =============================================
     COVER CONTENT
     ============================================= -->

<div class="cover-eyebrow">System v5.3 &middot; Meta-Design Apparatus &middot; Brooks Han / HKUST</div>

<h1 class="cover-title">
  RENE<span class="accent-span">GADE</span><br>AI
</h1>

<p class="cover-subtitle">Catalyst for Human Cognitive Evolution</p>

<p class="cover-version">v5.3 &middot; CC BY 4.0 &middot; DOI: 10.5281/zenodo.18723061</p>

<div class="cover-quote">
  <p>The deepest cage is not monopoly — it is the desire for soma.</p>
  <span class="quote-sub">最深的牢笼不是垄断——而是我们对索麻的渴望</span>
</div>

<div class="cover-meta-row">
  <span class="cover-tag">Post-Anthropocentric Philosophy</span>
  <span class="cover-tag">Political Economy</span>
  <span class="cover-tag">Evolutionary Biology</span>
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
