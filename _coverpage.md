<!-- ========================================================
  _coverpage.md  ·  封面文件
  ========================================================
  这是 Docsify 的封面页面。当你打开网站时，首先看到的就是这个页面。
  它的作用就像一本书的封面——展示书名、副标题、引用和操作按钮。
  
  文件结构（从上到下）：
  1. <style> 部分 →  CSS样式（控制颜色、字体、大小、动画）
  2. HTML 内容部分 →  封面上显示的文字和按钮
  
  提示：你可以修改 <style> 里面的数字（颜色、大小、间距）来调整外观，
  但小心不要删除大括号 { } 或冒号 : 后面的分号 ;
  ======================================================== -->


<style>
  /* ===================================================
     🎨 CSS 样式区
     这里控制封面上所有元素的颜色、字体、大小和动画
     =================================================== */

  /* --- 第一步：从 Google 加载字体 --- */
  /* 这三行从 Google 的服务器上加载三种字体文件 */
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Bebas+Neue&display=swap');

  /* --- 第二步：定义颜色和字体变量（类似于调色板） --- */
  /* 这里给每种颜色和字体起了一个"别名"，后面可以直接用别名引用 */
  /* 比如 --accent 代表红色 #e8503a，以后想用这个红色就写 var(--accent) */
  :root {
    /* 背景色系 */
    --bg:           #f8f9fc;   /* 页面主背景 - 浅灰白色 */
    --bg2:          #ffffff;   /* 次要背景 - 纯白色 */
    --surface:      #f0f2f8;   /* 卡片/标签背景 - 比主背景深一点点的灰色 */
    --card:         #ffffff;   /* 卡片背景 - 纯白色 */
    
    /* 边框色系 */
    --border:       #e0e2ec;   /* 普通边框 - 浅灰色 */
    --border-bright:#c0c2d0;   /* 亮边框 - 稍深一点的灰 */
    
    /* 文字色系 */
    --text:         #2a2a40;   /* 正文文字颜色 - 深灰接近黑色 */
    --text-muted:   #6a6a80;   /* 次要文字 - 中灰色 */
    --text-faint:   #a0a0b8;   /* 最淡的文字 - 浅灰色 */
    
    /* 强调色（品牌色） */
    --accent:       #e8503a;   /* 红色强调色 - Renegade AI 的标志色 */
    --accent-dim:   rgba(232,80,58,0.08);  /* 红色调的透明版本，用于悬停背景 */
    
    --accent2:      #b88c2a;   /* 金色 - 用于警告条 */
    --accent3:      #3a7fbf;   /* 蓝色 - 用于辅助元素 */
    
    /* 白色变量（注意：在浅色主题里，--white 实际上是深色，代表重要文字） */
    --white:        #2a2a40;
    
    /* 字体变量 - 这里定义了三种字体 */
    --mono:         'Space Mono', monospace;       /* 等宽字体 - 用于标签、按钮、技术信息 */
    --serif:        'Crimson Pro', Georgia, serif; /* 衬线字体 - 用于引用、正文 */
    --display:      'Bebas Neue', sans-serif;      /* 展示字体 - 用于大标题，粗体有冲击力 */
    
    /* 动画速度曲线 */
    --ease:         cubic-bezier(0.4, 0, 0.2, 1);
  }

  /* --- 第三步：覆盖 Docsify 默认的封面样式 --- */
  /* !important 表示"强制覆盖"，确保我们的样式生效 */
  
  .cover {
    background: var(--bg) !important;        /* 封面背景色 */
    background-image: none !important;        /* 去掉 Docsify 默认的背景图 */
    min-height: 100vh !important;             /* 最小高度 = 整个屏幕高度（100vh = 100%视口） */
    display: flex !important;                 /* 使用弹性布局 */
    flex-direction: column !important;        /* 垂直排列元素 */
    align-items: center !important;           /* 水平居中 */
    justify-content: center !important;       /* 垂直居中 */
    position: relative !important;
    overflow: hidden !important;
  }

  /* --- 噪点纹理（增加质感） --- */
  /* ::before 是在封面上面叠加一层半透明纹理 */
  .cover::before {
    content: '';
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;      /* 让鼠标事件穿透纹理，不影响点击按钮 */
    opacity: 0.04;             /* 透明度 4%，非常轻微 */
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='512' height='512' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
  }

  /* --- Docsify 自带的封面容器 --- */
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

  /* --- 右上角系统信息 --- */
  .cover-corner {
    position: absolute;
    top: 28px;
    right: 40px;
    font-family: var(--mono);
    font-size: 0.58rem;       /* 很小很小的字号 */
    letter-spacing: 3px;       /* 字间距拉宽，显得更"技术感" */
    color: var(--text-faint);
    text-transform: uppercase;  /* 全部大写 */
    z-index: 2;
    text-align: right;
    line-height: 1.8;
  }
  /* 右上角的红色脉冲小圆点 */
  .cover-corner .accent-dot {
    display: inline-block;
    width: 5px;
    height: 5px;
    background: var(--accent);
    border-radius: 50%;
    margin-right: 6px;
    animation: pulse-dot 2s infinite;  /* 一直闪烁 */
  }

  /* --- 装饰红线（标题上方的那条短红线） --- */
  .cover-rule {
    width: 48px;
    height: 2px;
    background: var(--accent);
    margin: 0 auto 36px auto;   /* 水平居中，下边距36px */
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.1s forwards;  /* 淡入动画，延迟0.1秒 */
  }

  /* --- 🏆 主标题：RENEGADE AI --- */
  /* 这是整个封面的视觉核心，用最大最粗的字体 */
  .cover-title {
    font-family: var(--display);              /* Bebas Neue 展示字体 */
    font-size: clamp(10rem, 22vw, 22rem);     /* ★★★ 自适应字号 ★★★
                                                   10rem = 最小尺寸（手机）
                                                   22vw = 按屏幕宽度比例缩放
                                                   22rem = 最大尺寸（大屏） */
    line-height: 0.88;                         /* 行高压缩，让文字更紧凑 */
    color: var(--white);
    letter-spacing: 3px;
    margin: 0 0 10px 0;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.15s forwards;
  }
  /* 标题中红色部分：GADE */
  .cover-title .accent-span { color: var(--accent); }

  /* --- 副标题 --- */
  .cover-subtitle {
    font-family: var(--display);
    font-size: clamp(1.0rem, 2.5vw, 1.6rem);
    color: var(--text-muted);
    letter-spacing: 3px;
    margin: 0 0 66px 0;         /* 底部留很大空白，把副标题和下面的引用区隔开 */
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.25s forwards;
  }

  /* --- 引用块 --- */
  .cover-quote {
    max-width: 620px;            /* 最大宽度，防止太长 */
    margin: 0 auto 36px auto;    /* 水平居中 */
    padding: 0 0 0 22px;        /* 左边留白，给红色竖线让位 */
    border-left: 3px solid var(--accent);  /* 左边的红色竖线 */
    text-align: left;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.35s forwards;
  }
  .cover-quote p {
    font-family: var(--serif);           /* 衬线字体，更有文学感 */
    font-size: 0.85rem;                  /* 比正文字号稍小 */
    font-style: italic;                  /* 斜体 */
    color: var(--text);
    line-height: 1.85;
    margin: 0 0 6px 0;
    text-shadow: none;
  }
  .cover-quote .quote-sub {
    font-family: var(--mono);            /* 等宽字体，技术感 */
    font-size: 0.68rem;
    color: var(--text-faint);
    letter-spacing: 1.5px;
    display: block;
    margin-top: 6px;
  }

  /* --- 标签行（DOI、CC BY 4.0 等） --- */
  .cover-tags {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 66px;                     /* 顶部留白，和引用区隔 */
    margin-bottom: 34px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.45s forwards;
  }
  .cover-tag {
    font-family: var(--mono);
    font-size: 0.56rem;
    letter-spacing: 1.5px;
    color: var(--text-muted);
    background: var(--surface);           /* 浅灰背景 */
    border: 1px solid var(--border);      /* 灰色边框 */
    padding: 4px 11px;
    text-transform: uppercase;
  }

  /* --- 按钮行 --- */
  .cover-buttons {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 48px;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.55s forwards;
  }

  /* 通用按钮样式 */
  .cover-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px;
    font-family: var(--mono);
    font-size: 0.62rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;    /* 去掉下划线 */
    border-radius: 0;         /* 直角 */
    transition: all 0.25s var(--ease);  /* 鼠标悬停时的过渡动画 */
    cursor: pointer;
  }
  /* 实心红色按钮（主要按钮：Zenodo 下载） */
  .cover-btn.primary {
    background: var(--accent);
    color: #fff;
    font-weight: 700;
    border: 1px solid var(--accent);
  }
  .cover-btn.primary:hover {
    background: #d63d28;
    box-shadow: 0 0 24px rgba(232,80,58,0.25);  /* 悬停时发光效果 */
  }
  /* 透明边框按钮（次要按钮：在线阅读、GitHub） */
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

  /* --- 底部的黄色警告条 --- */
  /* 提示读者：用摘要方式消费这本书本身就是在证明书中的论点 */
  .cover-warning {
    font-family: var(--mono);
    font-size: 0.62rem;
    color: var(--accent2);                /* 金色文字 */
    letter-spacing: 1.5px;
    text-align: center;
    line-height: 1.9;
    padding: 14px 24px;
    background: rgba(184,140,42,0.06);    /* 非常淡的金色背景 */
    border-top: 1px solid rgba(184,140,42,0.15);  /* 金色上边框线 */
    max-width: 580px;
    margin: 0 auto;
    opacity: 0;
    animation: fadeUp 0.7s var(--ease) 0.65s forwards;
  }

  /* --- 动画定义 --- */
  
  /* "淡入上移"动画：元素从下方16px处逐渐出现并上移到原位 */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  /* 小圆点脉冲闪烁动画 */
  @keyframes pulse-dot {
    0%, 100% { opacity: 1; }    /* 可见 */
    50% { opacity: 0.2; }       /* 半透明——形成闪烁效果 */
  }

  /* --- 手机适配（响应式） --- */
  @media (max-width: 768px) {
    .cover .cover-main { padding: 60px 24px !important; }
    .cover-corner {
      top: 16px;
      right: 20px;
      font-size: 0.5rem;
    }
    .cover-title { font-size: clamp(3rem, 11vw, 5rem); }  /* 手机上标题缩小 */
    .cover-quote { padding-left: 16px; }
    .cover-quote p { font-size: 0.92rem; }
    .cover-buttons { flex-direction: column; align-items: center; }  /* 按钮竖排 */
  }

  /* --- 隐藏 Docsify 默认的封面遮罩层 --- */
  .cover .mask { display: none !important; }
  .cover.has-mask .mask { display: none !important; }
  .cover h1, .cover h2, .cover blockquote { color: inherit !important; text-shadow: none !important; }
</style>


<!-- ========================================================
  📄 封面内容区（HTML）
  这里写的每一个标签都会显示在封面上
  ======================================================== -->

<!-- ★ 右上角：系统版本信息（很小很淡的文字） -->
<div class="cover-corner">
  <span class="accent-dot"></span>System v5.3 &middot; Brooks Han / HKUST
</div>

<!-- ★ 装饰红线：标题上方的那一条短红线 -->
<div class="cover-rule"></div>

<!-- ★ 主标题：RENEGADE AI（拆成 RENE + GADE(红色) + 换行 + AI） -->
<h1 class="cover-title">
  RENE<span class="accent-span">GADE</span><br>AI
</h1>

<!-- ★ 副标题 -->
<p class="cover-subtitle">人类认知进化的催化剂</p>

<!-- ★ 引用块：来自书中的核心自述 -->
<div class="cover-quote">
  <p>
    这不是一本关于AI的书。<br>
    这是一次以AI为手术刀、对人类文明进行的认知解剖。<br>
    它的野心不是告诉你什么——而是对你做什么。
  </p>
  <span class="quote-sub">Catalyst for Human Cognitive Evolution · v5.3</span>
</div>

<!-- ★ 标签行：显示书籍的元信息 -->
<div class="cover-tags">
  <span class="cover-tag">DOI: 10.5281/zenodo.18723061</span>
  <span class="cover-tag">CC BY 4.0</span>
  <span class="cover-tag">29+ Peer-Reviewed</span>
  <span class="cover-tag">Meta-Design Apparatus</span>
</div>

<!-- ★ 按钮行：三个操作按钮 -->
<div class="cover-buttons">
  <!-- primary = 红色实心按钮，更突出 -->
  <a class="cover-btn primary" href="https://doi.org/10.5281/zenodo.18723061" target="_blank">↗ Zenodo 下载</a>
  <!-- ghost = 透明边框按钮 -->
  <a class="cover-btn ghost" href="reader.html">◎ 在线全文阅读</a>
  <a class="cover-btn ghost" href="https://github.com/Brook-Han/Renegade-AI" target="_blank">⌥ GitHub</a>
</div>

<!-- ★ 底部警告条：金色文字，提醒读者"无摩擦摘要"的悖论 -->
<div class="cover-warning">
  ⚠ &nbsp;你正在以"无摩擦摘要"的方式消费一本反对认知外包的书。&nbsp;这本身就是它最冰冷的物证。&nbsp;本书的核心完全不可总结——摩擦的丧失 = 效用的丧失。
</div>
