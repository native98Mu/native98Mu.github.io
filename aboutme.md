---
layout: page
title: "A" side life of Muji
subtitle: Let's get the ball rolling
---

<style>
  .about-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem 0;
  }

  .about-header {
    text-align: center;
    margin-bottom: 3rem;
    padding: 2rem;
    background: linear-gradient(135deg, rgba(102, 126, 234, 0.05) 0%, rgba(118, 75, 162, 0.05) 100%);
    border-radius: 1rem;
    border: 1px solid rgba(102, 126, 234, 0.2);
  }

  .about-header h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    background: linear-gradient(135deg, #667EEA 0%, #764BA2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .about-section {
    background: white;
    padding: 2rem;
    margin-bottom: 2rem;
    border-radius: 1rem;
    box-shadow: 0 2px 8px rgba(102, 126, 234, 0.08);
    border: 1px solid #E2E8F0;
    transition: all 0.3s ease;
  }

  .about-section:hover {
    box-shadow: 0 4px 16px rgba(102, 126, 234, 0.15);
    border-color: #667EEA;
  }

  .about-section h2 {
    color: #667EEA;
    margin-bottom: 1.5rem;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid transparent;
    background: linear-gradient(135deg, #667EEA 0%, #764BA2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
  }

  .about-section h2::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 60px;
    height: 3px;
    background: linear-gradient(135deg, #667EEA 0%, #764BA2 100%);
    border-radius: 2px;
  }

  .about-list {
    list-style: none;
    padding-left: 0;
  }

  .about-list li {
    padding: 0.75rem 0;
    padding-left: 2rem;
    position: relative;
    transition: all 0.3s ease;
  }

  .about-list li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: #667EEA;
    font-weight: bold;
    font-size: 1.2rem;
  }

  .about-list li:hover {
    color: #667EEA;
    transform: translateX(5px);
  }

  .highlight-box {
    background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);
    border-left: 4px solid #667EEA;
    padding: 1.5rem;
    margin: 1.5rem 0;
    border-radius: 0.5rem;
  }

  .tag-cloud {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
  }

  .tag {
    background: linear-gradient(135deg, #667EEA 0%, #764BA2 100%);
    color: white;
    padding: 0.4rem 1rem;
    border-radius: 2rem;
    font-size: 0.875rem;
    transition: all 0.3s ease;
    box-shadow: 0 2px 4px rgba(102, 126, 234, 0.2);
  }

  .tag:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(102, 126, 234, 0.3);
  }
</style>

<div class="about-container">
  <div class="about-header">
    <h1>👋 Hi, I'm Muji</h1>
    <p style="font-size: 1.25rem; color: #4A5568; margin: 0;">AI Product Solutions Architect & AI Product Manager</p>
  </div>

  <div class="about-section">
    <h2>🚀 About Me</h2>
    <p>Welcome to my learning record! I'm passionate about exploring the frontiers of artificial intelligence and building products that make a real impact.</p>

    <div class="highlight-box">
      <strong>Current Focus:</strong>
      <ul class="about-list">
        <li>Large Language Models (LLM) architecture and applications</li>
        <li>AI product development and solution architecture</li>
        <li>LLM security and safety research</li>
      </ul>
    </div>
  </div>

  <div class="about-section">
    <h2>💡 Research Interests</h2>
    <p>I'm particularly interested in:</p>
    <ul class="about-list">
      <li>LLM inference optimization and scaling</li>
      <li>Fine-tuning strategies (LoRA, MLA, etc.)</li>
      <li>AI safety and adversarial robustness</li>
      <li>Multimodal AI systems</li>
      <li>Evaluating AI products and tools</li>
    </ul>

    <div class="tag-cloud">
      <span class="tag">LLM</span>
      <span class="tag">Deep Learning</span>
      <span class="tag">AI Security</span>
      <span class="tag">Product Management</span>
      <span class="tag">System Architecture</span>
    </div>
  </div>

  <div class="about-section">
    <h2>⚡ My Philosophy</h2>
    <div class="highlight-box">
      <ul class="about-list">
        <li><strong>Protect your eyes first, then work.</strong> Health is the foundation of productivity.</li>
        <li><strong>Solve real problems, beyond the hype.</strong> Focus on practical solutions that matter.</li>
        <li><strong>Go and create, don't give up.</strong> The best way to learn is by building.</li>
      </ul>
    </div>
  </div>

  <div class="about-section">
    <h2>📚 Blog Content</h2>
    <p>On this blog, you'll find my notes and explorations on:</p>
    <ul class="about-list">
      <li>Technical deep-dives into AI models (e.g., DeepSeek series)</li>
      <li>LLM inference techniques and optimizations</li>
      <li>AI product evaluations and reviews</li>
      <li>Hands-on tutorials and experiments</li>
    </ul>
  </div>

  <div class="about-section">
    <h2>📬 Get in Touch</h2>
    <p>I'm always excited to discuss AI, technology, or collaboration opportunities!</p>
    <p>
      <strong>Email:</strong> <a href="mailto:limujin1998@outlook.com">limujin1998@outlook.com</a>
    </p>
  </div>
</div>