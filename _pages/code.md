---
layout: page
permalink: /code/
title: Code
description: "Selected open-source projects and paper implementations &mdash; more code references on the <a href='/publications/' style='color: var(--global-theme-color);'>Publications</a> page."
nav: true
nav_order: 4
---

<div class="code-grid">

  <a class="code-card" href="{{ '/projects/actflow/' | relative_url }}" target="_blank" rel="noopener">
    <div class="code-card__image">
      <img src="{{ '/projects/actflow/static/images/teaser_local_to_global.png' | relative_url }}"
           alt="Local-to-global reachability diagram from the ActFlow paper">
    </div>
    <div class="code-card__body">
      <h3 class="code-card__title">Active Flow Expansion (ActFlow)</h3>
      <p class="code-card__venue">2026 · Out-of-distribution generative discovery</p>
      <p class="code-card__desc">
        Continued pre-training that expands a flow model's <em>generable set</em> beyond its
        training distribution via verifier-guided active exploration — with statistical
        guarantees and empirical gains across small molecules, peptides, and proteins.
      </p>
    </div>
  </a>

  <a class="code-card" href="{{ '/projects/fdc/' | relative_url }}" target="_blank" rel="noopener">
    <div class="code-card__image">
      <img src="{{ '/projects/fdc/static/images/teaser_gen_opt.png' | relative_url }}"
           alt="Generative optimization diagram from the Flow Density Control paper">
    </div>
    <div class="code-card__body">
      <h3 class="code-card__title">Flow Density Control (FDC)</h3>
      <p class="code-card__venue">NeurIPS 2025 Spotlight · Distributional fine-tuning of flow &amp; diffusion models</p>
      <p class="code-card__desc">
        A mirror-descent fine-tuning scheme that reduces optimization of <em>arbitrary utilities</em>
        under <em>arbitrary divergences</em> to a sequence of standard linear fine-tuning problems,
        going beyond entropy-regularized reward maximization.
      </p>
    </div>
  </a>

</div>
