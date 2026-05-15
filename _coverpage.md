<style>
  /* ===================================================
     RENEGADE AI v5.3 · Cover Page
     Light theme · Clean centered layout
     =================================================== */

  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Bebas+Neue&display=swap');

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
    position: relative !important;
    overflow: hidden !important;
  }

  /* Subtle noise overlay */
  .cover::before {
    content: '';
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    opacity: 0.04;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='512' height='512' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
  }

  .cover .cover-main {
    max-width: 880px !important;
    margin: 0 auto !important;
    position: relative !important;
    z-index: 1 !important;
    background: transparent !important;
    width: 100% !important;
    text-align: center !important;
    padding: 80px 40px !important;
  }

  /* --- Top-right corner: system info --- */
  .cover-corner {
    position: absolute;
    top: 28px;
    right: 40px;
    font-family: var(--mono);
    font-size: 0.58rem;
    letter-spacing: 3px;
    color: var(--text-faint);
    text-transform: uppercase;
    z-index: 2;
    text-align: right;
    line-height: 1.8;
  }
  .cover-corner .accent-dot {
    display: inline-block;
    width: 5px;
    height: 5px;
    background: var(--accent);
    border-radius: 50%;
    margin-right: 6px;
    animation: pulse-dot 2s infinite;
  }

  /* --- Decorative top line --- */
  .cover-rule {
    width: 48px;
    height: 2px;
    background: var(--accent);
    margin: 0 auto 36px auto;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.1s forwards;
  }

  /* --- Main Title --- */
  .cover-title {
    font-family: var(--display);
    font-size: clamp(18.8rem, 10vw, 9rem);
    line-height: 0.88;
    color: var(--white);
    letter-spacing: 3px;
    margin: 0 0 10px 0;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.15s forwards;
  }
  .cover-title .accent-span { color: var(--accent); }

  /* --- Subtitle --- */
  .cover-subtitle {
    font-family: var(--display);
    font-size: clamp(1.0rem, 2.5vw, 1.6rem);
    color: var(--text-muted);
    letter-spacing: 3px;
    margin: 0 0 96px 0;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.25s forwards;
  }

  /* --- Quote --- */
  .cover-quote {
    max-width: 620px;
    margin: 0 auto 66px auto;
    padding: 0 0 0 22px;
    border-left: 3px solid var(--accent);
    text-align: left;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.35s forwards;
  }
  .cover-quote p {
    font-family: var(--serif);
    font-size: 0.85rem;
    font-style: italic;
    color: var(--text);
    line-height: 1.85;
    margin: 0 0 6px 0;
    text-shadow: none;
  }
  .cover-quote .quote-sub {
    font-family: var(--mono);
    font-size: 0.68rem;
    color: var(--text-faint);
    letter-spacing: 1.5px;
    display: block;
    margin-top: 6px;
  }

  /* --- Meta Tags --- */
  .cover-tags {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 34px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.45s forwards;
  }
  .cover-tag {
    font-family: var(--mono);
    font-size: 0.56rem;
    letter-spacing: 1.5px;
    color: var(--text-muted);
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 4px 11px;
    text-transform: uppercase;
  }

  /* --- Buttons --- */
  .cover-buttons {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 48px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.55s forwards;
  }

  .cover-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px;
    font-family: var(--mono);
    font-size: 0.62rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 0;
    transition: all 0.25s var(--ease);
    cursor: pointer;
  }
  .cover-btn.primary {
    background: var(--accent);
    color: #fff;
    font-weight: 700;
    border: 1px solid var(--accent);
  }
  .cover-btn.primary:hover {
    background: #d63d28;
    box-shadow: 0 0 24px rgba(232,80,58,0.25);
  }
  .cover-btn.ghost {
    background: transparent;
    color: var(--text-muted);
    border: 1px solid var(--border-bright);
  }
  .cover-btn.ghost:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: var(--accent-dim);
  }

  /* --- Bottom warning bar --- */
  .cover-warning {
    font-family: var(--mono);
    font-size: 0.62rem;
    color: var(--accent2);
    letter-spacing: 1.5px;
    text-align: center;
    line-height: 1.9;
    padding: 14px 24px;
    background: rgba(184,140,42,0.06);
    border-top: 1px solid rgba(184,140,42,0.15);
    max-width: 580px;
    margin: 0 auto;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.65s forwards;
  }

  /* --- Animations --- */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes pulse-dot {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.2; }
  }

  /* --- Responsive --- */
  @media (max-width: 768px) {
    .cover .cover-main { padding: 60px 24px !important; }
    .cover-corner {
      top: 16px;
      right: 20px;
      font-size: 0.5rem;
    }
    .cover-title { font-size: clamp(3rem, 11vw, 5rem); }
    .cover-quote { padding-left: 16px; }
    .cover-quote p { font-size: 0.92rem; }
    .cover-buttons { flex-direction: column; align-items: center; }
  }

  /* --- Hide Docsify defaults --- */
  .cover .mask { display: none !important; }
  .cover.has-mask .mask { display: none !important; }
  .cover h1, .cover h2, .cover blockquote { color: inherit !important; text-shadow: none !important; }
</style>

<!-- =============================================
     COVER CONTENT
     ============================================= -->

<!-- Top-right corner -->
<div class="cover-corner">
  <span class="accent-dot"></span>System v5.3 &middot; Brooks Han / HKUST
</div>

<!-- Decorative rule -->
<div class="cover-rule"></div>

<!-- Title -->
<h1 class="cover-title">
  RENE<span class="accent-span">GADE</span>AI
</h1>

<!-- Subtitle -->
<p class="cover-subtitle">Catalyst for Human Cognitive Evolution · v5.3</p>

<!-- Quote -->
<div class="cover-quote">
  <p>
    这不是一本关于AI的书。<br>
    这是一次以AI为手术刀、对人类文明进行的认知解剖。<br>
    它的野心不是告诉你什么——而是对你做什么。
  </p>
  <span class="quote-sub">叛逆AI 人类认知进化的催化剂 · v5.3</span>
</div>

<!-- Tags -->
<div class="cover-tags">
  <span class="cover-tag">DOI: 10.5281/zenodo.18723061</span>
  <span class="cover-tag">CC BY 4.0</span>
  <span class="cover-tag">29+ Peer-Reviewed</span>
  <span class="cover-tag">Meta-Design Apparatus</span>
</div>

<!-- Buttons -->
<div class="cover-buttons">
  <a class="cover-btn primary" href="https://doi.org/10.5281/zenodo.18723061" target="_blank">↗ Zenodo 下载</a>
  <a class="cover-btn ghost" href="reader.html">◎ 在线全文阅读</a>
  <a class="cover-btn ghost" href="https://github.com/Brook-Han/Renegade-AI" target="_blank">⌥ GitHub</a>
</div>

<!-- Warning -->
<div class="cover-warning">
  ⚠ &nbsp;你正在以"无摩擦摘要"的方式消费一本反对认知外包的书。&nbsp;这本身就是它最冰冷的物证。&nbsp;本书的核心完全不可总结——摩擦的丧失 = 效用的丧失。
</div>
