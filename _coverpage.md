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
    padding: 40px !important;
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
    font-size: clamp(5rem, 15vw, 12rem); /* 手机上5个大字，电脑上12个大字 */
    
    line-height: 0.9; /* 行高调小一点，让大字看起来更紧凑 */
    color: var(--white);
    letter-spacing: 4px; /* 字母间距加大，更有气势 */
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
    margin-bottom: 40px;
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
    margin-top: 30px;
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