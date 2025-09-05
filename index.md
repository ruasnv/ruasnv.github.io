---
layout: default
title: Home
---
<h1>Ruya Sanver</h1>
<p><em>“The noblest pleasure is the joy of understanding.” – Leonardo da Vinci</em></p>
<p>CS undergraduate | Aspiring Researcher | Exploring learning systems, theory and reality through computation</p>

<div class="section">
  <h2> Research Interests</h2>
  <ul>
    <li>Theory of Computing (Automata, Turing, Gödel, Incompleteness)</li>
    <li>Complex & Chaotic Systems in AI</li>
    <li>Mathematics and Proofs of Deep Learning</li>
    <li>Physics-Inspired AI Models</li>
    <li>Distributed Computation & Compiler Theory</li>
  </ul>
</div>

<div class="section">
  <h2> Selected Projects</h2>
  <ul id="projects-list">
    {% assign public_repos = site.github.public_repositories %}
    {% for repo in public_repos %}
      {% if repo.name != 'ruasnv.github.io' and
      repo.name != 'jax'and
      repo.name != 'keras'and
      repo.name != 'keras-cv'and
      repo.name != 'keras-io'and
      repo.name != 'openvino'and
      repo.name != 'ruasnv'and
      repo.name != 'keras-hub'and
      repo.name != 'stock-prediction'
      %} 
        <li>
          <a href="{{ repo.html_url }}" target="_blank">
            <strong>{{ repo.name | replace: "-", " " | capitalize }}</strong>
          </a> 
          — {{ repo.description }}
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</div>

<div class="section">
  <h2> Blog Posts </h2>
  <ul id="substack-posts"></ul>
</div>

<script>
  async function loadSubstackPosts() {
    try {
      const rssUrl = "https://ruaslines.substack.com/feed";
      const response = await fetch(rssUrl);
      const text = await response.text();
      const parser = new DOMParser();
      const xml = parser.parseFromString(text, "application/xml");

      const items = xml.querySelectorAll("item");
      let html = "";
      items.forEach((item, i) => {
        if (i < 5) { // limit to 5 most recent posts
          const title = item.querySelector("title").textContent;
          const link = item.querySelector("link").textContent;
          html += `<li><a href="${link}" target="_blank">${title}</a></li>`;
        }
      });
      document.getElementById("substack-posts").innerHTML = html;
    } catch (error) {
      console.error("Error loading Substack posts:", error);
      document.getElementById("substack-posts").innerHTML = "<li>Unable to load posts right now.</li>";
    }
  }

  loadSubstackPosts();
</script>


<div class="section">
  <h2> Contact me</h2>
  <p>
    <a href="https://github.com/ruasnv" target="_blank">GitHub</a>
    <a href="https://linkedin.com/in/ruasnv/" target="_blank">LinkedIn</a> 
    <a href="mailto:ruyas7@proton.me">Email</a>
  </p>
</div>

<div class="footer">
  <p>© Ruya Sanver 2025 — Made with Jekyll and lots of coffee.</p>
</div>