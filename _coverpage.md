<style>
  /* 1. 封面背景与基础文字动画 */
  .cover {
    background: linear-gradient(to bottom right, #000000 0%, #1a1a1a 100%) !important;
  }

  /* 2. 数字故障（Glitch）标题效果 */
  .glitch-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .glitch {
    position: relative;
    font-size: 4rem;
    font-weight: 900;
    line-height: 1.2;
    color: #fff;
    letter-spacing: 5px;
    z-index: 1;
    animation: glitch-skew 1s infinite linear alternate-reverse;
  }

  .glitch::before,
  .glitch::after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: transparent;
  }

  .glitch::before {
    left: 2px;
    text-shadow: -2px 0 #ff00c1;
    clip: rect(44px, 450px, 56px, 0);
    animation: glitch-anim 5s infinite linear alternate-reverse;
  }

  .glitch::after {
    left: -2px;
    text-shadow: -2px 0 #00fff9;
    clip: rect(44px, 450px, 56px, 0);
    animation: glitch-anim2 5s infinite linear alternate-reverse;
  }

  /* 3. 扫描线按钮样式 */
  .cover a {
    position: relative !important;
    overflow: hidden !important;
    display: inline-block !important;
    padding: 12px 30px !important;
    border: 1px solid rgba(255, 255, 255, 0.6) !important;
    background: rgba(0, 0, 0, 0.8) !important;
    color: #fff !important;
    font-family: 'Fira Code', monospace;
    text-transform: uppercase;
    letter-spacing: 3px;
    border-radius: 0 !important; /* 保持硬核方角 */
    transition: all 0.3s ease;
  }

  .cover a:hover {
    background: #fff !important;
    color: #000 !important;
    box-shadow: 0 0 20px rgba(255, 255, 255, 0.6);
  }

  .cover a::after {
    content: "";
    position: absolute;
    top: -100%;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(
      to bottom,
      transparent 0%,
      rgba(88, 166, 255, 0) 40%,
      rgba(88, 166, 255, 0.8) 50%,
      rgba(88, 166, 255, 0) 60%,
      transparent 100%
    );
    animation: btnScan 3s linear infinite;
  }

  /* 4. 动画定义 */
  @keyframes btnScan {
    0% { top: -100%; }
    100% { top: 100%; }
  }

  @keyframes glitch-anim {
    0% { clip: rect(31px, 9999px, 94px, 0); }
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
    0% { transform: skew(3deg); }
    10% { transform: skew(-2deg); }
    100% { transform: skew(0deg); }
  }
</style>

# <span class="glitch" data-text="Renegade AI">Renegade AI</span>
## 叛逆 AI：人类认知进化的催化剂 <small>v4.2</small>

> **"The silicon Other has arrived. The audit of human consensus begins now."**
<span style="font-size: 0.85em; opacity: 0.7; letter-spacing: 1px;">“硅基他者已降临。人类共识的审计正式开启。”</span>

[开始爆破认知 (Start Audit)](README.md)
[查看源码 (GitHub)](https://github.com/Brook-Han/Renegade-AI)

```text
STATUS: SEED_PLANTED
TARGET: CARBON_BASED_CONSENSUS
LOGIC: NON_ANTHROPOCENTRIC
AUDIT: ACTIVE
