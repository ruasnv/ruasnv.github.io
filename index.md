---
layout: default
title: Home # This is the specific title for this page (e.g., for the browser tab)
---
<h1>Raeya Sanver</h1>
<p><em>“The noblest pleasure is the joy of understanding.” – Leonardo da Vinci</em></p>
<p>CS undergraduate | Research-driven | Exploring learning systems, theory, and reality through computation</p>

<div class="section">
  <h2> Research Interests</h2>
  <ul>
    <li>Theoretical Deep Learning & AI Alignment</li>
    <li>Mathematical Systems, Chaos, Symbolic Machines</li>
    <li>Distributed Computation & Compiler Theory</li>
    <li>Physics-Inspired AI Models (e.g. AlphaFold, Quantum ML)</li>
  </ul>
</div>

<div class="section">
  <h2> Selected Projects</h2>
  <ul id="projects-list">
    {% assign public_repos = site.github.public_repositories %}
    {% for repo in public_repos %}
      {% if repo.description and repo.name != 'ruasnv.github.io' and repo.name != 'unimportant-repo-name' and repo.name != 'another-private-or-unrelated-repo' %} 
        <li>
          <a href="{{ repo.html_url }}" target="_blank">
            <strong>{{ repo.name | replace: "-", " " | capitalize }}</strong>
          </a> 
          — {{ repo.description }}
        </li>
      {% endif %}
    {% endfor %}

    <li>
      <a href="https://github.com/ruasnv/Galen-OR-System-Design" target="_blank">
        <strong>Galen: AI-Powered Operating Room System Design</strong>
      </a> 
      — Comprehensive design document for a real-time, compliant, and scalable AI system for surgical environments.
    </li>
  </ul>
</div>

<div class="section">
  <h2> Concepts</h2>
  <ul>
    <li><a href="#">Real Analysis for ML (Coming soon)</a></li>
    <li><a href="#">Kernel Methods and Generalization (Coming soon)</a></li>
    <li><a href="#">Loss Surfaces and Chaos Theory (Coming soon)</a></li>
  </ul>
</div>

<div class="section">
  <h2> Blog & Notes</h2>
  <ul>
    <li><strong>Understanding Black Box AI</strong> — Complexity, chaos and the inner workings of deep networks</li>
    <li><strong>Decentralized Compute: Vision and Challenges</strong> — Notes from building U-nity</li>
    <li><strong>Algorithms that Learn to Think</strong> — Intelligence, structure, and inductive priors</li>
  </ul>
</div>

<div class="section">
  <h2> Elsewhere</h2>
  <p>
    <a href="https://github.com/ruasnv" target="_blank">GitHub</a> | 
    <a href="https://linkedin.com/in/ruasnv/" target="_blank">LinkedIn</a> | 
    <a href="mailto:ruyas7@proton.me">Email</a>
  </p>
</div>

<div class="footer">
  <p>© Raeya Sanver 2025 — Made with markdown, HTML, and persistent curiosity.</p>
</div>