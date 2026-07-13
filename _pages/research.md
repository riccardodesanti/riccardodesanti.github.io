---
layout: page
permalink: /research/
title: Research Overview
nav_title: Research
display_title: "Research: Generative Discovery Beyond the Data"
nav: true
nav_order: 1
---

<style>
  /* Smaller page heading so the long title fits on one line */
  .post-title { font-size: 2rem; }
</style>

<!-- =============================================================
     Intro — short overview of the full-stack approach
     ============================================================= -->
<div class="research-intro">
  <div class="research-header">
    <div class="research-text">
      <p>
        My research centers on <strong>exploration for out-of-distribution discovery</strong>:
        from the theoretical foundations of exploration and discovery, to principled flow- and diffusion-based discovery methods, and applications in biochemistry. More broadly, I aim to understand and establish the principles of <strong>discovery systems</strong> at the intersection of generative modeling, optimization, and sequential decision-making, toward a <strong>science of generative discovery</strong>.
      </p>
    </div>
    <div class="research-figure">
      <img src="{{ '/assets/img/research_overview.png' | relative_url }}" alt="Research Overview">
    </div>
  </div>
</div>

<!-- =============================================================
     Section 1 — Mathematical Foundations
     ============================================================= -->
{% capture s1_html %}{% bibliography -f {{ site.scholar.bibliography }} --group_by none --query @*[area_foundations=true]* %}{% endcapture %}
<div class="research-area">
  <h3>Mathematical Foundations of Exploration and Discovery</h3>
  <div class="research-header">
    <div class="research-figure research-figure--small" style="flex: 0 0 27%; max-width: 27%;">
      <img src="{{ '/assets/img/theory_animation.webp' | relative_url }}" alt="Mathematical Foundations animation">
    </div>
    <div class="research-text">
      <p>
        I develop mathematical foundations for exploration and discovery, from discrete dynamical systems to flow- and diffusion-based generative models. My work showed that <strong>maximum-entropy exploration</strong> can require non-Markovian policies [<a href="https://arxiv.org/pdf/2202.03060" target="_blank" rel="noopener">M1</a>], developed frameworks for optimizing complex exploration and experimental-design objectives [<a href="https://arxiv.org/pdf/2407.09905" target="_blank" rel="noopener">M2</a>, <a href="https://proceedings.neurips.cc/paper_files/paper/2022/file/1cb5b3d64bdf3c6642c8d9a8fbecd019-Paper-Conference.pdf" target="_blank" rel="noopener">M3</a>], and studied how geometric priors can improve the statistical complexity of active exploration [<a href="https://arxiv.org/pdf/2407.13364" target="_blank" rel="noopener">M4</a>]. To understand generative discovery processes, I recently extended these principles to answer questions such as:
      </p>
      <ul>
        <li><em>How can exploration be formalized on spaces implicitly represented by flow models?</em> [<a href="https://arxiv.org/pdf/2506.15385" target="_blank" rel="noopener">M5</a>, <a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">M6</a>]</li>
        <li><em>When can local <strong>flow expansion</strong> yield global coverage of new valid design regions?</em> [<a href="https://arxiv.org/pdf/2602.15984" target="_blank" rel="noopener">M7</a>]</li>
        <li><em>What guarantees are possible for <strong>distributional flow adaptation</strong> beyond average reward?</em>  [<a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">M8</a>, <a href="https://arxiv.org/pdf/2602.16796" target="_blank" rel="noopener">M9</a>]</li>
      </ul>
    </div>
  </div>
  {% if s1_html contains '<li' %}
    <h4>Selected Papers</h4>
    <div class="publications">
      {{ s1_html }}
    </div>
    <p class="see-all"><a href="{{ '/publications/' | relative_url }}">See all publications &rarr;</a></p>
  {% endif %}
</div>

<!-- =============================================================
     Section 2 — Scalable Generative Methods
     ============================================================= -->
{% capture s2_html %}{% bibliography -f {{ site.scholar.bibliography }} --group_by none --query @*[area_methods=true]* %}{% endcapture %}
<div class="research-area research-area--highlight">
  <h3>Discovery Algorithms via Flow and Diffusion Models</h3>
  <div class="research-header">
    <div class="research-figure research-figure--small" style="flex: 0 0 45%; max-width: 45%; margin-top: calc(-0.5rem - 2%); margin-right: -3%;">
      <img src="{{ '/assets/img/methods_animation.webp' | relative_url }}" alt="Generative Discovery Algorithms animation">
    </div>
    <div class="research-text">
      <p>
        I develop scalable algorithms that turn flow and diffusion models into practical engines for out-of-distribution discovery. My methods go beyond standard reward-guided fine-tuning: they adapt pre-trained generative models to <strong>amplify low-probability modes</strong> hidden within the prior — effectively debiasing it from its pre-training data [<a href="https://arxiv.org/pdf/2506.15385" target="_blank" rel="noopener">A1</a>, <a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">A2</a>]; to <strong>expand into new valid regions</strong> through verifier-constrained entropy expansion, yielding higher novelty and diversity [<a href="https://arxiv.org/pdf/2602.15984" target="_blank" rel="noopener">A3</a>]; and to <strong>target rare, high-value outcomes</strong> via distributional fine-tuning [<a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">A4</a>, <a href="https://arxiv.org/pdf/2602.16796" target="_blank" rel="noopener">A5</a>], or access intermediate states via reward-guided merging [<a href="https://arxiv.org/pdf/2602.08012" target="_blank" rel="noopener">A6</a>]. Concretely, my algorithms contributed to answering questions such as:
      </p>
      <ul>
        <li><em>How can fine-tuning allow to access low-probability modes hidden in a pre-trained flow?</em> [<a href="https://arxiv.org/pdf/2506.15385" target="_blank" rel="noopener">A1</a>, <a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">A2</a>]</li>
        <li><em>How can verifier feedback drive flow expansion into new valid design regions?</em> [<a href="https://arxiv.org/pdf/2602.15984" target="_blank" rel="noopener">A3</a>]</li>
        <li><em>How can flow fine-tuning target rare outcomes in the tails of the reward distribution? </em>[<a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">A4</a>, <a href="https://arxiv.org/pdf/2602.16796" target="_blank" rel="noopener">A5</a>]</li>
      </ul>
    </div>
  </div>
  {% if s2_html contains '<li' %}
    <h4>Selected Papers</h4>
    <div class="publications">
      {{ s2_html }}
    </div>
    <p class="see-all"><a href="{{ '/publications/' | relative_url }}">See all publications &rarr;</a></p>
  {% endif %}
</div>

<!-- =============================================================
     Section 3 — Real-World Biochemistry Applications
     ============================================================= -->
{% capture s3_html %}{% bibliography -f {{ site.scholar.bibliography }} --group_by none --query @*[area_applications=true]* %}{% endcapture %}
<div class="research-area">
  <h3>Biochemistry Applications</h3>
  <div class="research-header">
    <div class="research-figure research-figure--small" style="flex: 0 0 53%; max-width: 52%;">
      <img src="{{ '/assets/img/applications_animation.webp' | relative_url }}" alt="Real-World Science Applications animation">
    </div>
    <div class="research-text">
      <p>
        I bring discovery algorithms to the design of <strong>drug-like molecules, therapeutic peptides, and proteins</strong>,
        partnering with chemistry and biology academic labs [e.g., <a href="http://fhalab.caltech.edu" target="_blank" rel="noopener">LAB1</a>, <a href="https://www.chatterjeelab.com" target="_blank" rel="noopener">LAB2</a>] and industry [e.g., <a href="https://www.genesis.ml" target="_blank" rel="noopener">LAB3</a>] to close the loop between generative exploration and out-of-distribution discovery on real-world data. This line focuses on translating principled methods into measurable
        impact for sustainable chemistry and biotechnology. Concretely, I work on questions such as:
      </p>
      <ul>
        <li><em>How should we measure diversity, novelty, and coverage across biochemical design spaces?</em> [<a href="https://arxiv.org/pdf/2602.15984" target="_blank" rel="noopener">B1</a>]</li>
        <li><em>How can we generate novel molecules that satisfy both functional and synthetic constraints?</em> [<a href="https://openreview.net/pdf?id=RbpkAUKvSf" target="_blank" rel="noopener">B2</a>]</li>
        <li><em>How can we sacrifice the average molecular quality to improve the top candidates?</em> [<a href="https://arxiv.org/pdf/2511.22640" target="_blank" rel="noopener">B3</a>, <a href="https://arxiv.org/pdf/2602.16796" target="_blank" rel="noopener">B4</a>]</li>
      </ul>
    </div>
  </div>
  {% if s3_html contains '<li' %}
    <h4>Selected Papers</h4>
    <div class="publications">
      {{ s3_html }}
    </div>
    <p class="see-all"><a href="{{ '/publications/' | relative_url }}">See all publications &rarr;</a></p>
  {% endif %}
</div>
