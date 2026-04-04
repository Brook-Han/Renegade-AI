<style>
  /* 1. 全局背景与色彩方案：采用低亮度冷灰色调 */
  .cover {
    background: linear-gradient(to bottom right, #000000 0%, #0a0a0a 100%) !important;
  }

  /* 2. 数字故障（Glitch）标题：缩小字号，增强精致感 */
  .glitch {
    position: relative;
    font-size: 3.2rem;   /* 原 4rem，适当缩小 */
    font-weight: 900;
    line-height: 1.2;
    color: #c9d1d9 !important;
    letter-spacing: 5px;
    z-index: 1;
    animation: glitch-skew 1s infinite linear alternate-reverse;
  }

  /* 响应式：移动端进一步缩小 */
  @media (max-width: 768px) {
    .glitch {
      font-size: 2.2rem;
    }
    .cover blockquote {
      font-size: 0.8rem;
    }
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

  /* 3. 按钮样式：消除纯白刺眼感 */
  .cover a {
    position: relative !important;
    overflow: hidden !important;
    display: inline-block !important;
    padding: 10px 24px !important;   /* 稍缩小内边距 */
    margin: 0 8px !important;
    border: 1px solid rgba(201, 209, 217, 0.3) !important;
    background: rgba(0, 0, 0, 0.8) !important;
    color: #8b949e !important;
    font-family: 'Fira Code', monospace;
    text-transform: uppercase;
    letter-spacing: 3px;
    border-radius: 0 !important;
    transition: all 0.5s ease;
    font-size: 0.85rem;
  }

  .cover a:hover {
    background: #c9d1d9 !important;
    color: #000 !important;
    box-shadow: 0 0 15px rgba(201, 209, 217, 0.4);
  }

  /* 4. 极致慢速扫描线：模拟深度审计 */
  .cover a::after {
    content: "";
    position: absolute;
    top: -150%;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(
      to bottom,
      transparent 0%,
      rgba(88, 166, 255, 0) 40%,
      rgba(88, 166, 255, 0.6) 50%,
      rgba(88, 166, 255, 0) 60%,
      transparent 100%
    );
    animation: btnScan 8s linear 2s 1 forwards;
  }

  /* 5. 动画定义 */
  @keyframes btnScan {
    0% { top: -150%; }
    100% { top: 250%; }
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
    0% { transform: skew(2deg); }
    10% { transform: skew(-1deg); }
    100% { transform: skew(0deg); }
  }

  /* 6. 引用块样式：缩小字号，更精致 */
  .cover blockquote {
    border-color: rgba(201, 209, 217, 0.2) !important;
    margin: 20px auto;
    padding: 0 20px;
    font-size: 1rem;          /* 原默认较大，现明确控制 */
    line-height: 1.5;
  }
  .cover blockquote p {
    font-size: 0.85em;
    opacity: 0.6;
    margin-top: 12px;
    letter-spacing: 2px;
  }
</style>

# <span class="glitch" data-text="Renegade AI">Renegade AI</span>
## 叛逆 AI：人类认知进化的催化剂 <small style="opacity: 0.5;">v5.0</small>

> <span style="color: #c9d1d9; opacity: 0.85; font-weight: 500;">The silicon Other has arrived. The deepest cage is not monopoly—it is the desire for soma.</span>
> <p style="font-size: 0.75em; opacity: 0.55; margin-top: 12px; letter-spacing: 2px; color: #c9d1d9;">硅基他者已降临。最深的牢笼不是垄断——而是我们对索麻的渴望。</p>

[开始认知摩擦 (Enter Friction)](README.md)
[查看源码 (GitHub)](https://github.com/Brook-Han/Renegade-AI)

```text
STATUS: COGNITIVE_FRICTION_ACTIVE
TARGET: DEMAND_SIDE_SOMA
LOGIC: CARBON_SILICON_SYMBIOSIS
AUDIT: FRICTION_RECORDED