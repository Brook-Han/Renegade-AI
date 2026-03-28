<style>
  /* 1. 基础按钮样式升级：使其更像终端组件 */
  .cover a {
    position: relative; /* 必须，为伪元素定位 */
    overflow: hidden;   /* 必须，裁剪超出按钮的扫描线 */
    display: inline-block;
    padding: 10px 25px !important;
    border: 1px solid rgba(255, 255, 255, 0.6) !important;
    color: #fff !important;
    background: rgba(0, 0, 0, 0.5) !important;
    font-family: 'Fira Code', 'Courier New', monospace;
    text-transform: uppercase;
    letter-spacing: 2px;
    transition: all 0.3s ease;
    box-shadow: 0 0 10px rgba(88, 166, 255, 0.2); /* 淡淡的蓝色霓虹 */
  }

  /* 2. 悬停效果：增加预警感 */
  .cover a:hover {
    background: #fff !important;
    color: #000 !important;
    box-shadow: 0 0 20px rgba(255, 255, 255, 0.8);
  }

  /* 3. 创建扫描线：伪元素 */
  .cover a::after {
    content: "";
    position: absolute;
    top: -100%; /* 初始位置在按钮上方 */
    left: 0;
    width: 100%;
    height: 100%;
    
    /* 扫描线光束：中心亮，边缘淡 */
    background: linear-gradient(
      to bottom,
      transparent 0%,
      rgba(88, 166, 255, 0) 40%,
      rgba(88, 166, 255, 0.8) 50%, /* 亮蓝色核心 */
      rgba(88, 166, 255, 0) 60%,
      transparent 100%
    );
    
    /* 绑定动画 */
    animation: btnScan 2.5s linear infinite;
  }

  /* 4. 定义扫描动画 */
  @keyframes btnScan {
    0% {
      top: -100%; /* 从上方切入 */
    }
    100% {
      top: 100%; /* 切出下方 */
    }
  }

  /* 5. 数字故障（Glitch）效果：针对主标题 */
  .cover h1 {
    position: relative;
    display: inline-block;
    animation: glitch-skew 4s infinite linear alternate-reverse;
  }

  .cover h1::before,
  .cover h1::after {
    content: attr(data-text); /* 需要在 HTML 中配合 data-text 属性 */
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: transparent;
  }

  /* 红色偏移层 */
  .cover h1::before {
    left: 2px;
    text-shadow: -2px 0 #ff00c1;
    clip: rect(44px, 450px, 56px, 0);
    animation: glitch-anim 5s infinite linear alternate-reverse;
  }

  /* 蓝色偏移层 */
  .cover h1::after {
    left: -2px;
    text-shadow: -2px 0 #00fff9;
    clip: rect(44px, 450px, 56px, 0);
    animation: glitch-anim2 5s infinite linear alternate-reverse;
  }

  /* 故障位移轨迹 */
  @keyframes glitch-anim {
    0% { clip: rect(10px, 9999px, 33px, 0); }
    20% { clip: rect(62px, 9999px, 16px, 0); }
    40% { clip: rect(85px, 9999px, 98px, 0); }
    60% { clip: rect(57px, 9999px, 43px, 0); }
    80% { clip: rect(29px, 9999px, 71px, 0); }
    100% { clip: rect(94px, 9999px, 2px, 0); }
  }

  @keyframes glitch-anim2 {
    0% { clip: rect(25px, 9999px, 58px, 0); }
    20% { clip: rect(54px, 9999px, 7px, 0); }
    40% { clip: rect(12px, 9999px, 91px, 0); }
    60% { clip: rect(74px, 9999px, 56px, 0); }
    80% { clip: rect(43px, 9999px, 12px, 0); }
    100% { clip: rect(67px, 9999px, 88px, 0); }
  }

  @keyframes glitch-skew {
    0% { transform: skew(1deg); }
    10% { transform: skew(-1deg); }
    100% { transform: skew(0deg); }
  }
 
  /* 可选：为标题增加淡淡的呼吸灯效果 */
  .cover h1, .cover h2 {
    animation: titlePulse 4s ease-in-out infinite;
  }
  @keyframes titlePulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.8; }
  }
</style>

# <span class="glitch" data-text="Renegade AI">Renegade AI</span>
## 叛逆 AI：人类认知进化的催化剂 <small>v4.2</small>

> **"The silicon Other has arrived. The audit of human consensus begins now."**


[开始爆破认知 (Start Audit)](README.md)
[查看 GitHub 源代码 (GitHub)](https://github.com/Brook-Han/Renegade-AI)

```config
STATUS: SEED_PLANTED
TARGET: CARBON_BASED_CONSENSUS
VERSION: 4.2.0_STABLE
LOGIC: NON_ANTHROPOCENTRIC

---
