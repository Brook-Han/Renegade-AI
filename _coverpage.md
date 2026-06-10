<style>
  /* 字体由 index.html <link> 异步加载，此处不再重复 */
  :root {
    --bg:           #f8f9fc;
    --surface:      #f0f2f8;
    --border:       #e0e2ec;
    --border-bright:#c0c2d0;
    --text:         #2a2a40;
    --text-muted:   #6a6a80;
    --text-faint:   #a0a0b8;
    --accent:       #ff5c45;
    --accent-dim:   rgba(255,92,69,0.08);
    --accent2:      #d4af5c;
    --accent3:      #5ba3e6;
    --heading:      #2a2a40;
    
    --mono:         'Space Mono', monospace;
    --serif:        'Crimson Pro', Georgia, serif;
    --display:      'Bebas Neue', sans-serif;
    --ease:         cubic-bezier(0.4, 0, 0.2, 1);
  }

  /* ── DARK MODE (v5.4 · aligned with Radar) ── */
  :root.dark {
    --bg:           #0c0c18;
    --surface:      #12121e;
    --border:       #282840;
    --border-bright:#3a3a5a;
    --text:         #e2e2f0;
    --text-muted:   #a8a8d0;
    --text-faint:   #55557a;
    --heading:      #f4f4fc;
    --accent:       #ff5c45;
    --accent-dim:   rgba(255,92,69,0.12);
    --accent2:      #d4af5c;
    --accent3:      #5ba3e6;
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
    position: absolute;
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

  /* 系统信息 */
  .cover .cover-corner {
    position: absolute;
    top: 28px;
    left: 50%;                  /* 先将左边缘移动到屏幕中间 */
    transform: translateX(-50%); /* 向左反向平移自身宽度的 50%，实现完美居中 */
    font-family: var(--mono) !important;
    font-size: 0.725rem !important;
    letter-spacing: 3px !important;
    color: var(--text-faint) !important;
    text-transform: uppercase;
    z-index: 2;
    text-align: center;         /* 文字对齐改为居中 */
    line-height: 1.8;
    width: 100%;                /* 给定宽度防止文字换行折叠 */
    white-space: nowrap;        /* 强制不换行 */
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
    font-size: clamp(5.625rem, 15vw, 7.25rem) !important; /* 微调了最大上限，防止大屏破产 */
    line-height: 1.5 !important;
    color: var(--heading) !important;
    letter-spacing: 10px !important;
    margin: 0 0 20px 0 !important;
    font-weight: 900 !important;
    background: transparent !important;
    -webkit-text-fill-color: initial !important;
    text-shadow: 0 0 40px rgba(255,92,69,0.12);
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.15s forwards;
  }
  .cover h1.cover-title .accent-span { color: var(--accent) !important; }

  /* 副标题 */
  .cover .cover-subtitle {
    font-family: var(--display) !important;
    font-size: clamp(1.25rem, 2.5vw, 1.875rem) !important;
    color: var(--text-muted) !important;
    letter-spacing: 2px !important;
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
    font-size: 1.1rem !important;
    font-style: italic !important;
    color: var(--text) !important;
    line-height: 1.8 !important;
    margin: 0 0 8px 0 !important;
  }
  .cover .cover-quote .quote-sub {
    font-family: var(--mono) !important;
    font-size: 1.1rem !important;
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
    font-size: 0.725rem !important;
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
    font-size: 0.85rem !important;
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
    box-shadow: 0 0 24px rgba(255,92,69,0.25) !important;
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
  /* 全局焦点样式，与 Radar 主页对齐 */
  .cover :focus-visible {
    outline: 2px solid var(--accent) !important;
    outline-offset: 3px !important;
    border-radius: 2px !important;
  }
  .cover :focus:not(:focus-visible) { outline: none !important; }

  /* 键盘焦点样式，提升可访问性 */
  .cover .cover-buttons a.cover-btn:focus-visible {
    outline: 2px solid var(--accent) !important;
    outline-offset: 3px !important;
  }

  /* 底部的警告条 */
  .cover .cover-warning {
    font-family: var(--mono) !important;
    font-size: 0.775rem !important;
    color: var(--accent2) !important;
    letter-spacing: 1.5px !important;
    text-align: center;
    line-height: 1.9 !important;
    padding: 14px 24px !important;
    background: rgba(212,175,92,0.06) !important;
    border-top: 1px solid rgba(212,175,92,0.15) !important;
    border-bottom: 1px solid rgba(212,175,92,0.15) !important;
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

  /* 前庭功能障碍友好：关闭所有动画 */
  @media (prefers-reduced-motion: reduce) {
    .cover *, .cover *::before, .cover *::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      opacity: 1 !important;
    }
  }

  /* 手机适配（响应式） */
  @media (max-width: 768px) {
    .cover .cover-main { padding: 40px 20px !important; }
    .cover .cover-corner { top: 16px; font-size: 0.625rem !important; }
    .cover h1.cover-title { font-size: clamp(3.5rem, 15vw, 5.625rem) !important; margin-bottom: 15px !important; }
    .cover .cover-quote { padding-left: 16px !important; margin-bottom: 30px !important; }
    .cover .cover-buttons { flex-direction: column; width: 100%; gap: 8px !important; }
    .cover .cover-buttons a.cover-btn { width: 100%; justify-content: center; }
  }

  /* 强力清除冲突 */
  .cover .mask { display: none !important; }
  .cover h1:not(.cover-title), .cover h2, .cover blockquote { text-shadow: none !important; }
</style>

<div class="cover-corner"><span class="accent-dot"></span>System v5.4 &middot; Brooks Han / Independent Researcher</div>
<div class="cover-rule"></div>
<h1 class="cover-title">RENE<span class="accent-span">GADE </span> AI</h1>
<p class="cover-subtitle">Catalyst for Human Cognitive Evolution · v5.4</p>
<div class="cover-quote">
  <p>这不是一本关于AI的书。<br>这是一次以AI为手术刀、对人类文明进行的认知解剖。<br>它的野心不是告诉你什么——而是对你做什么。</p>
  <span class="quote-sub">人类认知进化的催化剂 · v5.4</span>
</div>
<div class="cover-tags">
  <span class="cover-tag">DOI: 10.5281/zenodo.18723061</span>
  <span class="cover-tag">CC BY 4.0</span>
  <span class="cover-tag">34+ Peer-Reviewed</span>
  <span class="cover-tag">Meta-Design Apparatus</span>
</div>
<div class="cover-buttons">
  <a class="cover-btn primary" href="https://doi.org/10.5281/zenodo.18723061" target="_blank" rel="noopener noreferrer" aria-label="下载 Zenodo 版本">↗ Zenodo 下载</a>
  <a class="cover-btn ghost" href="https://brook-han.github.io/Renegade-AI/reader.html" aria-label="在线全文阅读">◎ 在线全文阅读</a>
  <a class="cover-btn ghost" href="https://brook-han.github.io/renegade-ai-Updater/" target="_blank" rel="noopener noreferrer" aria-label="Radar 归档">⌥ Radar Archive</a>
</div>
<div class="cover-warning">⚠ &nbsp;你正在以"无摩擦摘要"的方式消费一本反对认知外包的书。这本身就是它最冰冷的物证。本书的核心完全不可总结——摩擦的丧失 = 效用的丧失。</div>
