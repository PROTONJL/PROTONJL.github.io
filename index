<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>你的名字 | UE 作品集</title>
<style>
  /* ========== 全局 ========== */
  * { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #0a0a0f;
    --bg-2: #12121a;
    --card: #16161f;
    --border: #26263a;
    --text: #e8e8f0;
    --text-dim: #9a9ab0;
    --accent: #00d4ff;
    --accent-2: #7b2fff;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: "Segoe UI", "PingFang SC", "Microsoft YaHei", sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.7;
    overflow-x: hidden;
  }

  a { color: inherit; text-decoration: none; }

  /* ========== 导航 ========== */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 18px 6vw;
    background: rgba(10, 10, 15, 0.75);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid transparent;
    transition: border-color 0.3s;
  }
  nav.scrolled { border-bottom-color: var(--border); }

  .logo {
    font-weight: 700;
    font-size: 1.1rem;
    letter-spacing: 1px;
  }
  .logo span { color: var(--accent); }

  .nav-links {
    display: flex;
    gap: 28px;
    font-size: 0.92rem;
  }
  .nav-links a {
    color: var(--text-dim);
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  .menu-btn {
    display: none;
    background: none;
    border: none;
    color: var(--text);
    font-size: 1.5rem;
    cursor: pointer;
  }

  /* ========== Hero ========== */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 6vw;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: "";
    position: absolute;
    top: -30%; right: -15%;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(0,212,255,0.15), transparent 70%);
    border-radius: 50%;
    pointer-events: none;
  }
  .hero::after {
    content: "";
    position: absolute;
    bottom: -20%; left: -10%;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(123,47,255,0.15), transparent 70%);
    border-radius: 50%;
    pointer-events: none;
  }

  .hero-tag {
    color: var(--accent);
    font-size: 0.9rem;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 18px;
  }

  .hero h1 {
    font-size: clamp(2.2rem, 6vw, 4.5rem);
    line-height: 1.15;
    font-weight: 800;
    margin-bottom: 20px;
  }
  .hero h1 .gradient {
    background: linear-gradient(90deg, var(--accent), var(--accent-2));
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }

  .hero p {
    color: var(--text-dim);
    max-width: 560px;
    font-size: 1.05rem;
    margin-bottom: 36px;
  }

  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }

  .btn {
    padding: 12px 28px;
    border-radius: 8px;
    font-size: 0.95rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.25s;
    border: 1px solid transparent;
  }
  .btn-primary {
    background: linear-gradient(90deg, var(--accent), var(--accent-2));
    color: #fff;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,212,255,0.3); }

  .btn-ghost {
    border-color: var(--border);
    color: var(--text);
  }
  .btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

  /* ========== 通用 Section ========== */
  section { padding: 100px 6vw; }

  .section-title {
    font-size: clamp(1.6rem, 3vw, 2.2rem);
    font-weight: 700;
    margin-bottom: 12px;
  }
  .section-title span { color: var(--accent); }

  .section-sub {
    color: var(--text-dim);
    margin-bottom: 50px;
    font-size: 0.95rem;
  }

  /* ========== 关于 ========== */
  .about-grid {
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    gap: 60px;
    align-items: center;
  }
  .about-text p { color: var(--text-dim); margin-bottom: 16px; }

  .stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  .stat {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px;
    text-align: center;
  }
  .stat .num {
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(90deg, var(--accent), var(--accent-2));
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  .stat .label { color: var(--text-dim); font-size: 0.85rem; margin-top: 6px; }

  /* ========== 技能 ========== */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
  }
  .skill-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 26px;
    transition: all 0.25s;
  }
  .skill-card:hover {
    border-color: var(--accent);
    transform: translateY(-4px);
  }
  .skill-card h3 {
    font-size: 1.05rem;
    margin-bottom: 10px;
    color: var(--accent);
  }
  .skill-card p { color: var(--text-dim); font-size: 0.88rem; }

  /* ========== 作品集 ========== */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 26px;
  }
  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    overflow: hidden;
    transition: all 0.3s;
    display: flex;
    flex-direction: column;
  }
  .project-card:hover {
    transform: translateY(-6px);
    border-color: var(--accent);
    box-shadow: 0 12px 40px rgba(0,212,255,0.12);
  }
  .project-thumb {
    height: 180px;
    background: linear-gradient(135deg, #1a1a2e, #16213e);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--text-dim);
    font-size: 0.85rem;
    position: relative;
    overflow: hidden;
  }
  .project-thumb::after {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(0,212,255,0.1), rgba(123,47,255,0.1));
    opacity: 0;
    transition: opacity 0.3s;
  }
  .project-card:hover .project-thumb::after { opacity: 1; }

  .project-body { padding: 22px; flex: 1; display: flex; flex-direction: column; }
  .project-body h3 { font-size: 1.1rem; margin-bottom: 8px; }
  .project-body p {
    color: var(--text-dim);
    font-size: 0.88rem;
    margin-bottom: 16px;
    flex: 1;
  }
  .tags { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 16px; }
  .tag {
    font-size: 0.75rem;
    padding: 4px 10px;
    border-radius: 20px;
    background: rgba(0,212,255,0.1);
    color: var(--accent);
    border: 1px solid rgba(0,212,255,0.25);
  }
  .project-link {
    color: var(--accent);
    font-size: 0.85rem;
    font-weight: 600;
    display: inline-flex;
    align-items: center;
    gap: 6px;
  }
  .project-link:hover { gap: 10px; }

  /* ========== 联系 ========== */
  .contact {
    text-align: center;
    background: var(--bg-2);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
  }
  .contact h2 { margin-bottom: 16px; }
  .contact p { color: var(--text-dim); margin-bottom: 32px; }
  .contact-links {
    display: flex;
    justify-content: center;
    gap: 18px;
    flex-wrap: wrap;
  }
  .contact-links a {
    padding: 12px 26px;
    border: 1px solid var(--border);
    border-radius: 8px;
    font-size: 0.9rem;
    transition: all 0.25s;
  }
  .contact-links a:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-2px);
  }

  /* ========== Footer ========== */
  footer {
    text-align: center;
    padding: 30px;
    color: var(--text-dim);
    font-size: 0.82rem;
  }

  /* ========== 滚动淡入 ========== */
  .reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: all 0.7s ease;
  }
  .reveal.active {
    opacity: 1;
    transform: translateY(0);
  }

  /* ========== 响应式 ========== */
  @media (max-width: 768px) {
    .nav-links {
      position: fixed;
      top: 64px; right: 0;
      flex-direction: column;
      background: var(--bg-2);
      width: 220px;
      padding: 24px;
      gap: 20px;
      border-left: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      transform: translateX(100%);
      transition: transform 0.3s;
    }
    .nav-links.open { transform: translateX(0); }
    .menu-btn { display: block; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    section { padding: 70px 6vw; }
  }
</style>
</head>
<body>

<!-- ========== 导航 ========== -->
<nav id="nav">
  <div class="logo">YOUR<span>NAME</span></div>
  <div class="nav-links" id="navLinks">
    <a href="#about">关于</a>
    <a href="#skills">技能</a>
    <a href="#projects">作品</a>
    <a href="#contact">联系</a>
  </div>
  <button class="menu-btn" id="menuBtn">☰</button>
</nav>

<!-- ========== Hero ========== -->
<header class="hero">
  <div class="hero-tag">Unreal Engine Developer</div>
  <h1>你好，我是 <span class="gradient">你的名字</span><br />用 UE 做有温度的作品</h1>
  <p>
    专注于 Unreal Engine 关卡设计、蓝图系统、材质与 Niagara 特效。
    这里记录我做的项目、踩过的坑，以及一些还在折腾中的想法。
  </p>
  <div class="hero-btns">
    <a href="#projects" class="btn btn-primary">查看作品</a>
    <a href="#contact" class="btn btn-ghost">联系我</a>
  </div>
</header>

<!-- ========== 关于 ========== -->
<section id="about">
  <h2 class="section-title reveal">关于<span>我</span></h2>
  <p class="section-sub reveal">简单介绍一下自己</p>
  <div class="about-grid">
    <div class="about-text reveal">
      <p>
        我是 XXX，一名 Unreal Engine 开发者 / 学习者。从 XX 年开始接触 UE，
        做过 FPS 关卡、开放世界场景、交互式漫游等项目。
      </p>
      <p>
        熟悉蓝图可视化编程、C++ 基础、材质编辑器、Niagara 粒子系统、Sequencer 过场动画。
        平时喜欢研究光照、后处理、性能优化，也喜欢把做出来的东西整理成教程。
      </p>
      <p>
        这个网站用来展示我的项目，也用来督促自己持续输出。
      </p>
    </div>
    <div class="stats reveal">
      <div class="stat"><div class="num">3+</div><div class="label">年 UE 经验</div></div>
      <div class="stat"><div class="num">10+</div><div class="label">完成项目</div></div>
      <div class="stat"><div class="num">5+</div><div class="label">上线作品</div></div>
      <div class="stat"><div class="num">∞</div><div class="label">折腾热情</div></div>
    </div>
  </div>
</section>

<!-- ========== 技能 ========== -->
<section id="skills" style="background: var(--bg-2); border-top: 1px solid var(--border); border-bottom: 1px solid var(--border);">
  <h2 class="section-title reveal">技能<span>栈</span></h2>
  <p class="section-sub reveal">我常用的工具和技术</p>
  <div class="skills-grid">
    <div class="skill-card reveal">
      <h3>蓝图系统</h3>
      <p>熟练使用蓝图实现角色控制、交互逻辑、UI、AI 行为树、动画状态机。</p>
    </div>
    <div class="skill-card reveal">
      <h3>C++ 开发</h3>
      <p>掌握 UE C++ 基础，能编写 Actor、Component、GameMode、自定义函数库。</p>
    </div>
    <div class="skill-card reveal">
      <h3>材质与渲染</h3>
      <p>熟悉材质编辑器、PBR 流程、后处理、光照烘焙、Lumen / Nanite 基础。</p>
    </div>
    <div class="skill-card reveal">
      <h3>Niagara 特效</h3>
      <p>能制作粒子、烟雾、火焰、魔法等特效，了解 GPU / CPU 粒子区别。</p>
    </div>
    <div class="skill-card reveal">
      <h3>关卡设计</h3>
      <p>掌握地形、植被、模块化搭建、光照氛围、玩家动线设计。</p>
    </div>
    <div class="skill-card reveal">
      <h3>Sequencer</h3>
      <p>能制作过场动画、相机运镜、角色动画、音画同步。</p>
    </div>
    <div class="skill-card reveal">
      <h3>性能优化</h3>
      <p>了解 Draw Call、LOD、剔除、光照复杂度、Stat 命令、Profiler 分析。</p>
    </div>
    <div class="skill-card reveal">
      <h3>版本管理</h3>
      <p>使用 Git / Perforce 管理 UE 项目，了解 LFS、二进制资产处理。</p>
    </div>
  </div>
</section>

<!-- ========== 作品集 ========== -->
<section id="projects">
  <h2 class="section-title reveal">我的<span>作品</span></h2>
  <p class="section-sub reveal">一些做过的项目和练习</p>
  <div class="projects-grid">

    <div class="project-card reveal">
      <div class="project-thumb">项目截图 / 视频封面</div>
      <div class="project-body">
        <h3>FPS 关卡：废弃工厂</h3>
        <p>使用 UE5 搭建的 FPS 关卡，包含敌人 AI、武器系统、可破坏物、任务流程。</p>
        <div class="tags">
          <span class="tag">UE5</span>
          <span class="tag">蓝图</span>
          <span class="tag">AI</span>
        </div>
        <a href="#" class="project-link">查看详情 →</a>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-thumb">项目截图 / 视频封面</div>
      <div class="project-body">
        <h3>开放世界场景：山谷清晨</h3>
        <p>使用 Lumen + Nanite 制作的开放世界场景，重点在光照、植被和氛围。</p>
        <div class="tags">
          <span class="tag">Lumen</span>
          <span class="tag">Nanite</span>
          <span class="tag">场景</span>
        </div>
        <a href="#" class="project-link">查看详情 →</a>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-thumb">项目截图 / 视频封面</div>
      <div class="project-body">
        <h3>交互式漫游：虚拟展厅</h3>
        <p>第一人称漫游项目，包含 UI 交互、展品介绍、灯光控制、背景音乐。</p>
        <div class="tags">
          <span class="tag">交互</span>
          <span class="tag">UI</span>
          <span class="tag">漫游</span>
        </div>
        <a href="#" class="project-link">查看详情 →</a>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-thumb">项目截图 / 视频封面</div>
      <div class="project-body">
        <h3>Niagara 特效合集</h3>
        <p>火焰、烟雾、魔法阵、爆炸等特效练习，包含 GPU 粒子优化。</p>
        <div class="tags">
          <span class="tag">Niagara</span>
          <span class="tag">特效</span>
          <span class="tag">GPU</span>
        </div>
        <a href="#" class="project-link">查看详情 →</a>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-thumb">项目截图 / 视频封面</div>
      <div class="project-body">
        <h3>Sequencer 过场动画</h3>
        <p>使用 Sequencer 制作的短片，包含相机运镜、角色动画、音画同步。</p>
        <div class="tags">
          <span class="tag">Sequencer</span>
          <span class="tag">动画</span>
        </div>
        <a href="#" class="project-link">查看详情 →</a>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-thumb">项目截图 / 视频封面</div>
      <div class="project-body">
        <h3>UE C++ 插件练习</h3>
        <p>用 C++ 写的自定义 Actor 和 Component，练习 UE 的反射和生命周期。</p>
        <div class="tags">
          <span class="tag">C++</span>
          <span class="tag">插件</span>
        </div>
        <a href="#" class="project-link">查看详情 →</a>
      </div>
    </div>

  </div>
</section>

<!-- ========== 联系 ========== -->
<section id="contact" class="contact">
  <h2 class="section-title reveal">联系<span>我</span></h2>
  <p class="reveal">想聊聊 UE、项目合作，或者只是打个招呼，都欢迎。</p>
  <div class="contact-links reveal">
    <a href="mailto:your@email.com">📧 Email</a>
    <a href="https://github.com/yourname" target="_blank">🐙 GitHub</a>
    <a href="https://space.bilibili.com/yourid" target="_blank">📺 Bilibili</a>
    <a href="https://www.artstation.com/yourname" target="_blank">🎨 ArtStation</a>
  </div>
</section>

<!-- ========== Footer ========== -->
<footer>
  © 2026 你的名字 · 用 Unreal Engine 和 HTML 搭建
</footer>

<script>
  // 导航滚动效果
  const nav = document.getElementById('nav');
  window.addEventListener('scroll', () => {
    nav.classList.toggle('scrolled', window.scrollY > 20);
  });

  // 移动端菜单
  const menuBtn = document.getElementById('menuBtn');
  const navLinks = document.getElementById('navLinks');
  menuBtn.addEventListener('click', () => {
    navLinks.classList.toggle('open');
  });
  navLinks.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', () => navLinks.classList.remove('open'));
  });

  // 滚动淡入
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('active');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));
</script>

</body>
</html>
