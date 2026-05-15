<style>
  /* ===================================================
     RENEGADE AI v5.3 · Cover Page
     小白优化版：修复了字体大小，增加了霸气感
     =================================================== */

  /* 导入字体（不用管这里，让网站变好看用的） */
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Bebas+Neue&display=swap');

  /* 定义颜色变量（方便统一管理颜色） */
  :root {
    --bg:           #f8f9fc;
    --text:         #2a2a40;
    --white:        #2a2a40; /* 其实这里是深灰色，因为主题是浅色的 */
    --accent:       #e8503a; /* 红色强调色 */
    --mono:         'Space Mono', monospace;
    --serif:        'Crimson Pro', Georgia, serif;
    --display:      'Bebas Neue', sans-serif; /* 标题用的字体 */
  }

  /* --- 封面整体布局 --- */
  .cover {
    background: var(--bg) !important;
    min-height: 100vh !important;
    display: flex !important;
    align-items: center !important;
    justify-content: center !important;
  }

  /* --- 中间内容区域 --- */
  .cover .cover-main {
    max-width: 900px !important;
    text-align: center !important;
    padding: 60px !important;
  }

  /* ===================================================
     重点修改区域：主标题 (Main Title)
     =================================================== */
  .cover-title {
    font-family: var(--display);
    
    /*
      👇👇👇 关键修改在这里！👇👇👇
      clamp(最小字号, 随屏幕变化的动态大小, 最大字号)
      原来的数字是反的，现在修正并放大了！
    */
    font-size: clamp(5rem, 15vw, 22rem); /* 手机上5个大字，电脑上22个大字 */
    
    line-height: 0.9; /* 行高调小一点，让大字看起来更紧凑 */
    color: var(--white);
    letter-spacing: 5px; /* 字母间距加大，更有气势 */
    margin: 0 0 20px 0;
    
    /* 动画效果保持不变 */
    opacity: 0;
    animation: fadeUp 0.7s ease forwards;
  }
  
  /* 标题里的红色部分 */
  .cover-title .accent-span { 
    color: var(--accent); 
  }

  /* --- 副标题 --- */
  .cover-subtitle {
    font-family: var(--display);
    font-size: clamp(1.2rem, 3vw, 1.8rem); /* 稍微放大了一点 */
    color: #666;
    letter-spacing: 4px;
    margin-bottom: 90px;
  }

  /* --- 引言文字 --- */
  .cover-quote {
    max-width: 600px;
    margin: 30px auto;
    padding-left: 20px;
    border-left: 3px solid var(--accent);
    text-align: left;
  }
  .cover-quote p {
    font-family: var(--serif);
    font-size: 1rem; /* 引言字体稍微清晰一点 */
    line-height: 1.8;
    color: #333;
  }

  /* --- 底部标签和按钮 --- */
  .cover-tags {
    margin-top: 60px;
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .cover-tag {
    font-family: var(--mono);
    font-size: 0.6rem;
    padding: 5px 10px;
    border: 1px solid #ddd;
    text-transform: uppercase;
  }

  /* --- 淡入上升动画定义 --- */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ===================================================
     手机适配（屏幕宽度小于 768px 时生效）
     =================================================== */
  @media (max-width: 768px) {
    .cover-title {
      /* 手机上的标题大小，如果你觉得手机上太大，改这里的第一个数字 */
      font-size: clamp(3.5rem, 12vw, 5rem);
      letter-spacing: 2px; /* 手机上字间距缩小一点 */
    }
    
    .cover .cover-main {
      padding: 20px !important;
    }
  }
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