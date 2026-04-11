---
layout: home
title: xord.org
lang: en
---

<section class="hero">
  <div class="container hero-inner">
    <p class="hero-eyebrow">Apps &amp; Open Source</p>
    <h1 class="hero-title">
      Indie apps<br>
      and <span class="accent">open-source<br>libraries</span>.
    </h1>
    <p class="hero-lede">
      Building indie iOS apps and the open-source libraries that power them.
      Design, implementation, library maintenance — all handled solo.
    </p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="#apps">Apps</a>
      <a class="btn btn-ghost" href="#oss">Open Source</a>
    </div>
  </div>
  <div class="hero-blobs" aria-hidden="true">
    <span class="blob blob-1"></span>
    <span class="blob blob-2"></span>
    <span class="blob blob-3"></span>
  </div>
</section>

<section class="section about" id="about">
  <div class="container">
    <p class="section-eyebrow">01 — About</p>
    <h2 class="section-title">About</h2>
    <div class="about-grid">
      <p class="about-lead">
        Self-built <strong>iOS apps</strong> and the <strong>open-source libraries</strong>
        that make them possible. Apps ship via the App Store; libraries via RubyGems and GitHub.
      </p>
      <ul class="facts">
        <li><span class="fact-label">Focus</span><span class="fact-value">iOS apps / OSS libraries</span></li>
        <li><span class="fact-label">Stack</span><span class="fact-value">Ruby / C++ / Swift</span></li>
        <li><span class="fact-label">Based</span><span class="fact-value">Japan</span></li>
      </ul>
    </div>
  </div>
</section>

<section class="section apps" id="apps">
  <div class="container">
    <p class="section-eyebrow">02 — Apps</p>
    <h2 class="section-title">Apps</h2>
    <p class="section-lede">iOS apps currently on the App Store.</p>
    <div class="cards apps-grid">
      {% for app in site.data.apps %}
      <a class="card app-card accent-{{ app.accent }}" href="{{ app.url | relative_url }}">
        <h3 class="card-title">{{ app.name }}</h3>
        <p class="card-tagline">{{ app.description_en }}</p>
        <span class="card-link">Details →</span>
      </a>
      {% endfor %}
    </div>
  </div>
</section>

<section class="section oss" id="oss">
  <div class="container">
    <p class="section-eyebrow">03 — Open Source</p>
    <h2 class="section-title">Open Source</h2>
    <p class="section-lede">
      Open-source libraries I maintain. Most of them exist to power my own apps, and they're all distributed via RubyGems.
    </p>
    <div class="cards gems-grid">
      {% for gem in site.data.gems %}
      <div class="card gem-card">
        <h3 class="card-title mono">{{ gem.name }}</h3>
        <p class="card-tagline">{{ gem.tagline_en }}</p>
        <div class="card-links">
          <a class="card-link-btn" href="{{ gem.github }}">GitHub</a>
          <a class="card-link-btn" href="{{ gem.rubygems }}">RubyGems</a>
        </div>
      </div>
      {% endfor %}
    </div>
    <p class="oss-aside">
      The C++ / Objective-C layer is also distributed as a CocoaPod →
      <a href="https://github.com/xord/cruby">CRuby</a>
    </p>
  </div>
</section>

<section class="section contact" id="contact">
  <div class="container">
    <p class="section-eyebrow">04 — Contact</p>
    <h2 class="section-title">Contact</h2>
    <p class="contact-lede">For work inquiries, app feedback, or questions about the open-source libraries.</p>
    <ul class="contact-list">
      <li><a href="https://x.com/xordog"><span>X</span><strong>@xordog</strong></a></li>
      <li><a href="https://github.com/xord"><span>GitHub</span><strong>@xord</strong></a></li>
    </ul>
  </div>
</section>
