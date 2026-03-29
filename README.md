<style>
  * {
    box-sizing: border-box;
  }

  body {
    background: linear-gradient(135deg, #0f0f1e 0%, #1a1a3e 100%);
    color: #e0e0e0;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  }

  .header-section {
    background: linear-gradient(135deg, #7c3aed 0%, #ec4899 50%, #f59e0b 100%);
    color: white;
    padding: 80px 20px;
    border-radius: 20px;
    margin-bottom: 60px;
    text-align: center;
    box-shadow: 0 20px 60px rgba(124, 58, 237, 0.4);
    position: relative;
    overflow: hidden;
  }

  .header-section::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
    background-size: 50px 50px;
    animation: float 20s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% { transform: translate(0, 0); }
    50% { transform: translate(25px, 25px); }
  }

  .header-content {
    position: relative;
    z-index: 2;
  }

  .header-title {
    font-size: 4em;
    font-weight: 900;
    margin: 0;
    text-shadow: 3px 3px 10px rgba(0,0,0,0.3);
    background: linear-gradient(135deg, #ffffff 0%, #f0f0f0 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .header-subtitle {
    font-size: 1.4em;
    margin: 15px 0 0 0;
    opacity: 0.95;
    font-weight: 300;
    letter-spacing: 1px;
  }

  .header-description {
    font-size: 1.1em;
    margin: 20px 0;
    opacity: 0.9;
  }

  .contact-badges {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
    margin-top: 30px;
  }

  .contact-badge {
    display: inline-block;
    background: rgba(255,255,255,0.25);
    color: white;
    padding: 12px 24px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: 700;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    border: 2px solid rgba(255,255,255,0.5);
    backdrop-filter: blur(10px);
  }

  .contact-badge:hover {
    background: rgba(255,255,255,0.4);
    border-color: white;
    transform: translateY(-4px) scale(1.05);
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
  }

  .about-card {
    background: linear-gradient(135deg, rgba(124, 58, 237, 0.15) 0%, rgba(236, 72, 153, 0.15) 100%);
    border: 2px solid rgba(124, 58, 237, 0.5);
    padding: 40px;
    border-radius: 15px;
    margin-bottom: 50px;
    box-shadow: 0 8px 32px rgba(124, 58, 237, 0.1);
  }

  .about-card h2 {
    color: #7c3aed;
    margin-top: 0;
    font-size: 1.8em;
    margin-bottom: 15px;
  }

  .about-card p {
    line-height: 1.8;
    font-size: 1.05em;
    margin: 12px 0;
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 25px;
    margin-bottom: 50px;
  }

  .skill-card {
    background: linear-gradient(135deg, rgba(124, 58, 237, 0.2) 0%, rgba(236, 72, 153, 0.2) 100%);
    padding: 35px;
    border-radius: 15px;
    box-shadow: 0 8px 30px rgba(0,0,0,0.2);
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    border: 1px solid rgba(124, 58, 237, 0.4);
    backdrop-filter: blur(10px);
  }

  .skill-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 50px rgba(124, 58, 237, 0.3);
    background: linear-gradient(135deg, rgba(124, 58, 237, 0.3) 0%, rgba(236, 72, 153, 0.3) 100%);
    border-color: rgba(124, 58, 237, 0.8);
  }

  .skill-card h3 {
    margin-top: 0;
    color: #7c3aed;
    font-size: 1.3em;
    border-bottom: 3px solid #ec4899;
    padding-bottom: 12px;
    margin-bottom: 15px;
  }

  .badge-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
  }

  .tech-badge {
    display: inline-flex;
    align-items: center;
    background: rgba(255,255,255,0.1);
    padding: 8px 16px;
    border-radius: 25px;
    font-size: 0.9em;
    font-weight: 700;
    color: #e0e0e0;
    border: 1.5px solid rgba(124, 58, 237, 0.6);
    transition: all 0.3s ease;
    backdrop-filter: blur(10px);
  }

  .tech-badge:hover {
    background: linear-gradient(135deg, #7c3aed 0%, #ec4899 100%);
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(124, 58, 237, 0.3);
    border-color: #7c3aed;
  }

  .section-title {
    font-size: 2.5em;
    color: #ffffff;
    margin-bottom: 40px;
    text-align: center;
    position: relative;
    padding-bottom: 20px;
    font-weight: 900;
    letter-spacing: 1px;
  }

  .section-title::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 5px;
    background: linear-gradient(90deg, #7c3aed, #ec4899, #f59e0b);
    border-radius: 3px;
    box-shadow: 0 0 20px rgba(124, 58, 237, 0.5);
  }

  .specialization-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-bottom: 50px;
  }

  .specialization-card {
    background: linear-gradient(135deg, #7c3aed 0%, #ec4899 100%);
    color: white;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 10px 40px rgba(124, 58, 237, 0.3);
    transition: all 0.4s ease;
    border: 2px solid rgba(255,255,255,0.2);
  }

  .specialization-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 60px rgba(124, 58, 237, 0.4);
    border-color: rgba(255,255,255,0.5);
  }

  .specialization-card h4 {
    margin-top: 0;
    font-size: 1.2em;
    margin-bottom: 10px;
  }

  .specialization-card p {
    margin: 0;
    font-size: 0.95em;
    opacity: 0.95;
  }

  .project-section {
    margin-bottom: 50px;
  }

  .project-card {
    background: linear-gradient(135deg, rgba(30, 30, 50, 0.8) 0%, rgba(40, 40, 70, 0.8) 100%);
    border-left: 6px solid #7c3aed;
    padding: 35px;
    margin-bottom: 25px;
    border-radius: 12px;
    box-shadow: 0 8px 30px rgba(124, 58, 237, 0.15);
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    border: 1px solid rgba(124, 58, 237, 0.3);
  }

  .project-card:hover {
    box-shadow: 0 15px 50px rgba(124, 58, 237, 0.3);
    transform: translateX(8px);
    border-left-color: #ec4899;
    border-color: rgba(236, 72, 153, 0.5);
  }

  .project-title {
    color: #7c3aed;
    font-size: 1.6em;
    margin: 0 0 15px 0;
    font-weight: 800;
  }

  .project-description {
    color: #d0d0d0;
    line-height: 1.8;
    margin: 0;
    font-size: 1.05em;
  }

  .highlight {
    color: #f59e0b;
    font-weight: 700;
  }

  .contact-section {
    text-align: center;
    background: linear-gradient(135deg, #7c3aed 0%, #ec4899 100%);
    color: white;
    padding: 60px;
    border-radius: 20px;
    margin-top: 60px;
    box-shadow: 0 20px 60px rgba(124, 58, 237, 0.3);
    border: 2px solid rgba(255,255,255,0.2);
  }

  .contact-section h3 {
    margin-top: 0;
    font-size: 2em;
    font-weight: 900;
    margin-bottom: 20px;
  }

  .contact-section p {
    font-size: 1.1em;
    margin: 15px 0;
    opacity: 0.95;
  }

  .email-list {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin: 30px 0;
  }

  .email-link {
    color: white;
    text-decoration: none;
    background: rgba(255,255,255,0.25);
    padding: 12px 24px;
    border-radius: 30px;
    transition: all 0.3s ease;
    font-weight: 700;
    border: 2px solid rgba(255,255,255,0.4);
    backdrop-filter: blur(10px);
  }

  .email-link:hover {
    background: rgba(255,255,255,0.4);
    transform: translateY(-3px);
    border-color: white;
  }

  .separator {
    height: 2px;
    background: linear-gradient(90deg, #7c3aed, #ec4899, #f59e0b, transparent);
    margin: 60px 0;
    border-radius: 1px;
  }

  .footer-text {
    text-align: center;
    margin-top: 40px;
    color: #888;
    font-size: 0.95em;
  }
</style>

<div class="header-section">
  <div class="header-content">
    <h1 class="header-title">Aguita</h1>
    <p class="header-subtitle">Full Stack Developer & ML Engineer</p>
    <p class="header-description">Creator of OpceanAI, Vexis, NHE, Gitsune, Flux, and Japy</p>
    <div class="contact-badges">
      <a href="https://discord.gg/CFs7tmhR" class="contact-badge">Discord</a>
      <a href="https://instagram.com/aguita_frexa" class="contact-badge">Instagram</a>
      <a href="https://youtube.com/@@アグイタちゃん" class="contact-badge">YouTube</a>
    </div>
  </div>
</div>

---

<div class="about-card">
  <h2>About Me</h2>
  <p>Full-stack developer and ML engineer based in Mexico (es-MX), age 18. Passionate about building scalable applications, advanced AI systems, and next-generation machine learning models. Currently focused on developing efficient LLM architectures, cryptographic systems, and AI benchmarking tools.</p>
  <p><strong>Hardware Setup:</strong> Snapdragon 685, 8GB RAM | <strong>Drink:</strong> Water</p>
</div>

<div class="separator"></div>

## <div class="section-title">Technical Stack</div>

<div class="skills-grid">
  <div class="skill-card">
    <h3>Programming Languages</h3>
    <div class="badge-container">
      <span class="tech-badge">Python</span>
      <span class="tech-badge">TypeScript</span>
      <span class="tech-badge">JavaScript</span>
      <span class="tech-badge">Rust</span>
      <span class="tech-badge">Go</span>
      <span class="tech-badge">Java</span>
      <span class="tech-badge">Kotlin</span>
      <span class="tech-badge">Bash</span>
    </div>
  </div>

  <div class="skill-card">
    <h3>Web Development</h3>
    <div class="badge-container">
      <span class="tech-badge">React</span>
      <span class="tech-badge">Next.js</span>
      <span class="tech-badge">Astro</span>
      <span class="tech-badge">Node.js</span>
      <span class="tech-badge">HTML5</span>
      <span class="tech-badge">CSS3</span>
    </div>
  </div>

  <div class="skill-card">
    <h3>Machine Learning & AI</h3>
    <div class="badge-container">
      <span class="tech-badge">PyTorch</span>
      <span class="tech-badge">TensorFlow</span>
      <span class="tech-badge">Transformers</span>
      <span class="tech-badge">Hugging Face</span>
      <span class="tech-badge">JAX</span>
      <span class="tech-badge">NumPy</span>
      <span class="tech-badge">Pandas</span>
      <span class="tech-badge">Unsloth</span>
    </div>
  </div>

  <div class="skill-card">
    <h3>Databases & Data</h3>
    <div class="badge-container">
      <span class="tech-badge">PostgreSQL</span>
      <span class="tech-badge">MongoDB</span>
      <span class="tech-badge">MySQL</span>
      <span class="tech-badge">Redis</span>
      <span class="tech-badge">SQLite</span>
    </div>
  </div>

  <div class="skill-card">
    <h3>DevOps & Tools</h3>
    <div class="badge-container">
      <span class="tech-badge">Docker</span>
      <span class="tech-badge">Git</span>
      <span class="tech-badge">Linux</span>
    </div>
  </div>

  <div class="skill-card">
    <h3>Operating Systems</h3>
    <div class="badge-container">
      <span class="tech-badge">Artix Linux</span>
      <span class="tech-badge">Arch Linux</span>
      <span class="tech-badge">Debian</span>
      <span class="tech-badge">Fedora</span>
    </div>
  </div>
</div>

<div class="separator"></div>

## <div class="section-title">Core Specializations</div>

<div class="specialization-grid">
  <div class="specialization-card">
    <h4>Large Language Models</h4>
    <p>Model development, fine-tuning, optimization, and evaluation</p>
  </div>

  <div class="specialization-card">
    <h4>AI Systems Architecture</h4>
    <p>LLM deployment, inference optimization, and benchmarking</p>
  </div>

  <div class="specialization-card">
    <h4>Cryptography & Security</h4>
    <p>Vector-based encryption systems and quantization techniques</p>
  </div>

  <div class="specialization-card">
    <h4>Full-Stack Development</h4>
    <p>React, Next.js, Node.js, TypeScript</p>
  </div>

  <div class="specialization-card">
    <h4>Backend Systems</h4>
    <p>REST APIs, distributed systems, database design</p>
  </div>

  <div class="specialization-card">
    <h4>DevOps & Infrastructure</h4>
    <p>Docker, containerization, deployment pipelines</p>
  </div>
</div>

<div class="separator"></div>

## <div class="section-title">Featured Projects</div>

<div class="project-section">
  <div class="project-card">
    <h2 class="project-title">🚀 OpceanAI</h2>
    <p class="project-description">
      Advanced language model development startup. Creator of <span class="highlight">YuuKi RxG 8B</span>, an 8-billion parameter model achieving <span class="highlight">96.6% accuracy on TruthfulQA</span> and excelling in truthfulness benchmarks. Focused on building efficient, reliable, and verifiable AI models. Our flagship model demonstrates superior performance in reasoning and truthfulness evaluation.
    </p>
  </div>

  <div class="project-card">
    <h2 class="project-title">🔐 Vexis</h2>
    <p class="project-description">
      <span class="highlight">Vector Encrypted Xor Interference System</span> - Revolutionary encryption system combining AI vector representations with advanced quantization techniques. Integrates machine learning with cryptographic principles to deliver a novel approach to data security. Bridges the gap between modern AI and traditional cryptography.
    </p>
  </div>

  <div class="project-card">
    <h2 class="project-title">🧠 NHE</h2>
    <p class="project-description">
      <span class="highlight">Neural Honesty Evaluation</span> - Specialized LLM benchmark measuring reasoning capabilities independent of learned human patterns. Evaluates model truthfulness and reasoning authenticity, ensuring outputs reflect genuine understanding rather than pattern memorization. A critical tool for assessing real AI reasoning.
    </p>
  </div>

  <div class="project-card">
    <h2 class="project-title">🌳 Gitsune</h2>
    <p class="project-description">
      Enhanced fork of Forgejo with optimized user interface and expanded tooling. Designed to maximize developer experience with streamlined workflows, improved collaboration tools, and additional features for modern development teams. A complete reimagining of Git repository management.
    </p>
  </div>

  <div class="project-card">
    <h2 class="project-title">⚡ Flux</h2>
    <p class="project-description">
      Next-generation LLM training framework designed to overcome transformer limitations. Implements novel training methodologies achieving superior performance, efficiency, and scalability beyond traditional transformer approaches. The future of language model architecture is here.
    </p>
  </div>

  <div class="project-card">
    <h2 class="project-title">🔗 Japy</h2>
    <p class="project-description">
      Functional JavaScript runtime enabling seamless execution of JavaScript within other programming languages via decorator-based syntax. Provides clean, native embedding without WebAssembly or language embedding overhead. Perfect for polyglot development and JavaScript interoperability.
    </p>
  </div>
</div>

<div class="separator"></div>

<div class="contact-section">
  <h3>Let&apos;s Connect</h3>
  <p>Open to collaborations in advanced AI research, machine learning optimization, and full-stack development. Interested in innovative approaches to model efficiency, security, and reasoning capabilities.</p>
  <div class="email-list">
    <a href="mailto:opceanai@gmail.com" class="email-link">opceanai@gmail.com</a>
    <a href="mailto:contact@opceanai.com" class="email-link">contact@opceanai.com</a>
    <a href="mailto:aguitachan3@gmail.com" class="email-link">aguitachan3@gmail.com</a>
  </div>
</div>

<div class="footer-text">
  <p>Built with passion, Python, and creativity | Made in Mexico 🇲🇽</p>
</div>
