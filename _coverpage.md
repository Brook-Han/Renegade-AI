<style>
  /* --- 从 Google 加载字体 --- */
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
    --white:        #2a2a40;
    
    --mono:         'Space Mono', monospace;
    --serif:        'Crimson Pro', Georgia, serif;
    --display:      'Bebas Neue', sans-serif;
    --ease:         cubic-bezier(0.4, 0, 0.2, 1);
  }

  /* --- 覆盖 Docsify 默认的封面样式 --- */
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

  /* 噪点纹理 */
  .cover::before {
    content: '';
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    opacity: 0.04;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='512' height='512' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
  }

  /* 核心容器 */
  .cover .cover-main {
    max-width: 880px !important;
    margin: 0 auto !important;
    position: relative !important;
    z-index: 1 !important;
    background: transparent !important;
    width: 100% !important;
    text-align: center !important;
    padding: 60px 40px !important;
    display: flex !important;
    flex-direction: column !important;
    align-items: center !important;
  }

  /* 右上角系统信息 */
  .cover .cover-corner {
    position: absolute;
    top: 28px;
    right: 40px;
    font-family: var(--mono) !important;
    font-size: 0.58rem !important;
    letter-spacing: 3px !important;
    color: var(--text-faint) !important;
    text-transform: uppercase;
    z-index: 2;
    text-align: right;
    line-height: 1.8;
  }
  .cover .cover-corner .accent-dot {
    display: inline-block;
    width: 5px;
    height: 5px;
    background: var(--accent);
    border-radius: 50%;
    margin-right: 6px;
    animation: pulse-dot 2s infinite;
  }

  /* 装饰红线 */
  .cover .cover-rule {
    width: 48px;
    height: 2px;
    background: var(--accent) !important;
    margin: 0 auto 24px auto !important;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.1s forwards;
  }

  /* 🏆 修复后的主标题：强制压制原主题字体大小 */
  .cover h1.cover-title {
    font-family: var(--display) !important;
    font-size: clamp(4.5rem, 14vw, 11rem) !important; /* 微调了最大上限，防止大屏破产 */
    line-height: 0.9 !important;
    color: var(--white) !important;
    letter-spacing: 4px !important;
    margin: 0 0 20px 0 !important;
    font-weight: 900 !important;
    background: transparent !important;
    -webkit-text-fill-color: initial !important;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.15s forwards;
  }
  .cover h1.cover-title .accent-span { color: var(--accent) !important; }

  /* 副标题 */
  .cover .cover-subtitle {
    font-family: var(--display) !important;
    font-size: clamp(1.1rem, 2.5vw, 1.8rem) !important;
    color: var(--text-muted) !important;
    letter-spacing: 4px !important;
    margin: 0 0 45px 0 !important; /* 控制与下方元素的间距 */
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.25s forwards;
  }

  /* 引用块 */
  .cover .cover-quote {
    max-width: 620px !important;
    margin: 0 auto 40px auto !important;
    padding: 4px 0 4px 22px !important;
    border-left: 3px solid var(--accent) !important;
    text-align: left !important;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.35s forwards;
  }
  .cover .cover-quote p {
    font-family: var(--serif) !important;
    font-size: 0.95rem !important;
    font-style: italic !important;
    color: var(--text) !important;
    line-height: 1.8 !important;
    margin: 0 0 8px 0 !important;
  }
  .cover .cover-quote .quote-sub {
    font-family: var(--mono) !important;
    font-size: 0.68rem !important;
    color: var(--text-faint) !important;
    letter-spacing: 1.5px;
    display: block;
  }

  /* 标签行 */
  .cover .cover-tags {
    display: flex !important;
    gap: 8px !important;
    flex-wrap: wrap;
    justify-content: center;
    margin: 20px 0 40px 0 !important;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.45s forwards;
  }
  .cover .cover-tag {
    font-family: var(--mono) !important;
    font-size: 0.58rem !important;
    letter-spacing: 1.5px !important;
    color: var(--text-muted) !important;
    background: var(--surface) !important;
    border: 1px solid var(--border) !important;
    padding: 5px 12px !important;
    text-transform: uppercase;
  }

  /* 按钮行 */
  .cover .cover-buttons {
    display: flex !important;
    gap: 12px !important;
    flex-wrap: wrap;
    justify-content: center;
    margin: 0 0 50px 0 !important;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.55s forwards;
  }

  /* 按钮定制 */
  .cover .cover-buttons a.cover-btn {
    display: inline-flex !important;
    align-items: center;
    gap: 8px;
    padding: 12px 24px !important;
    font-family: var(--mono) !important;
    font-size: 0.68rem !important;
    letter-spacing: 2px !important;
    text-transform: uppercase;
    text-decoration: none !important;
    border-radius: 0 !important;
    transition: all 0.25s var(--ease) !important;
    margin: 0 !important; /* 消除 Docsify 默认给按钮加的疯狂外边距 */
  }
  .cover .cover-buttons a.cover-btn.primary {
    background: var(--accent) !important;
    color: #fff !important;
    font-weight: 700 !important;
    border: 1px solid var(--accent) !important;
  }
  .cover .cover-buttons a.cover-btn.primary:hover {
    background: #d63d28 !important;
    box-shadow: 0 0 24px rgba(232,80,58,0.25) !important;
  }
  .cover .cover-buttons a.cover-btn.ghost {
    background: transparent !important;
    color: var(--text-muted) !important;
    border: 1px solid var(--border-bright) !important;
  }
  .cover .cover-buttons a.cover-btn.ghost:hover {
    border-color: var(--accent) !important;
    color: var(--accent) !important;
    background: var(--accent-dim) !important;
  }

  /* 底部的警告条 */
  .cover .cover-warning {
    font-family: var(--mono) !important;
    font-size: 0.62rem !important;
    color: var(--accent2) !important;
    letter-spacing: 1.5px !important;
    text-align: center;
    line-height: 1.9 !important;
    padding: 14px 24px !important;
    background: rgba(184,140,42,0.06) !important;
    border-top: 1px solid rgba(184,140,42,0.15) !important;
    border-bottom: 1px solid rgba(184,140,42,0.15) !important;
    max-width: 620px !important;
    margin: 0 auto !important;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.65s forwards;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes pulse-dot {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.2; }
  }

  /* 手机适配（响应式） */
  @media (max-width: 768px) {
    .cover .cover-main { padding: 40px 20px !important; }
    .cover .cover-corner { top: 16px; right: 20px; font-size: 0.5rem !important; }
    .cover h1.cover-title { font-size: clamp(2.8rem, 12vw, 4.5rem) !important; margin-bottom: 15px !important; }
    .cover .cover-quote { padding-left: 16px !important; margin-bottom: 30px !important; }
    .cover .cover-buttons { flex-direction: column; width: 100%; gap: 8px !important; }
    .cover .cover-buttons a.cover-btn { width: 100%; justify-content: center; }
  }

  /* 强力清除冲突 */
  .cover .mask { display: none !important; }
  .cover h1, .cover h2, .cover blockquote { text-shadow: none !important; }
</style>

<div class="cover-corner"><span class="accent-dot"></span>System v5.3 &middot; Brooks Han / HKUST</div>
<div class="cover-rule"></div>
<h1 class="cover-title">RENE<span class="accent-span">GADE</span><br>AI</h1>
<p class="cover-subtitle">人类认知进化的催化剂</p>
<div class="cover-quote">
  <p>这不是一本关于AI的书。<br>这是一次以AI为手术刀、对人类文明进行的认知解剖。<br>它的野心不是告诉你什么——而是对你做什么。</p>
  <span class="quote-sub">Catalyst for Human Cognitive Evolution · v5.3</span>
</div>
<div class="cover-tags">
  <span class="cover-tag">DOI: 10.5281/zenodo.18723061</span>
  <span class="cover-tag">CC BY 4.0</span>
  <span class="cover-tag">29+ Peer-Reviewed</span>
  <span class="cover-tag">Meta-Design Apparatus</span>
</div>
<div class="cover-buttons">
  <a class="cover-btn primary" href="https://doi.org/10.5281/zenodo.18723061" target="_blank">↗ Zenodo 下载</a>
  <a class="cover-btn ghost" href="#/README">◎ 在线全文阅读</a>
  <a class="cover-btn ghost" href="https://github.com/Brook-Han/Renegade-AI" target="_blank">⌥ GitHub</a>
</div>
<div class="cover-warning">⚠ &nbsp;你正在以"无摩擦摘要"的方式消费一本反对认知外包的书。这本身就是它最冰冷的物证。本书的核心完全不可总结——摩擦的丧失 = 效用的丧失。</div>