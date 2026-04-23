---
layout: home
title: xord.org
lang: en
---

<section class="hero">
  <div class="container hero-inner">
    <p class="hero-eyebrow">Apps · Games · Libraries</p>
    <h1 class="hero-title">
      Creative tools,<br>
      games,<br>
      and <span class="accent">open-source libraries</span>.
    </h1>
    <p class="hero-lede">
      Building creative tools, indie games, and the open-source libraries that power them.
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
        Self-built <strong>creative tools &amp; games</strong> for iOS, plus the
        <strong>open-source libraries</strong> that make them possible.
        Apps ship via the App Store; libraries via GitHub and RubyGems.
      </p>
      <ul class="facts">
        <li><span class="fact-label">Makes</span><span class="fact-value">Creative Tools / Games</span></li>
        <li><span class="fact-label">Stack</span><span class="fact-value">Ruby / C++ / Swift</span></li>
        <li><span class="fact-label">Mode</span><span class="fact-value">Indie Developer</span></li>
      </ul>
    </div>
  </div>
</section>

<section class="section apps" id="apps">
  <div class="container">
    <p class="section-eyebrow">02 — Apps</p>
    <h2 class="section-title">Apps</h2>
    <p class="section-lede">Creative tools and indie games currently on the App Store.</p>
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
      Open-source libraries I maintain. Most of them exist to power my own creative tools and games, and they're all distributed via RubyGems.
    </p>
    <div class="cards gems-grid">
      {% for gem in site.data.gems %}
      <div class="card gem-card">
        <a class="gem-card-main" href="{{ gem.github }}" aria-label="{{ gem.name }} on GitHub"></a>
        <h3 class="card-title mono">{{ gem.name }}</h3>
        <p class="card-tagline">{{ gem.tagline_en }}</p>
        <a class="card-link" href="{{ gem.rubygems }}">RubyGems →</a>
      </div>
      {% endfor %}
    </div>
    <p class="oss-aside">
      The C++ / Objective-C layer is also distributed as a CocoaPod →
      <a href="https://github.com/xord/cruby">CRuby</a>
    </p>
  </div>
</section>

<section class="section talks-writing" id="talks-writing">
  <div class="container">
    <p class="section-eyebrow">04 — Talks & Writing</p>
    <h2 class="section-title">Talks & Writing</h2>
    <p class="section-lede">Conference talks, technical articles, and other published work.</p>

    <h3 class="subsection-title">Talks</h3>
    <ul class="tw-list">
      {% for talk in site.data.talks %}
      <li class="tw-item">
        <span class="tw-title">{{ talk.title_en }} <span class="tw-lang">JA</span></span>
        <span class="tw-meta">
          {% if talk.event %}<span class="tw-event">{{ talk.event }}</span>{% endif %}
          {% if talk.year %}<span class="tw-year">{{ talk.year }}</span>{% endif %}
        </span>
        <span class="tw-links">
          <a href="{{ talk.slides }}">Slides</a>
          {% if talk.video %}<a href="{{ talk.video }}">Video</a>{% endif %}
        </span>
      </li>
      {% endfor %}
    </ul>

    <h3 class="subsection-title">Writing</h3>
    <ul class="tw-list">
      {% for article in site.data.writing %}
      <li class="tw-item">
        <a class="tw-title" href="{{ article.url }}">{{ article.title_en }} <span class="tw-lang">JA</span></a>
        <span class="tw-meta">
          <span class="tw-platform">{{ article.platform }}</span>
          <span class="tw-year">{{ article.year }}</span>
        </span>
      </li>
      {% endfor %}
    </ul>
  </div>
</section>

<section class="section contact" id="contact">
  <div class="container">
    <p class="section-eyebrow">05 — Contact</p>
    <h2 class="section-title">Contact</h2>
    <p class="contact-lede">For app feedback, questions about the open-source libraries, or work inquiries.</p>
    <ul class="contact-list">
      <li><a href="https://x.com/tokujiros"><span>X</span><strong>@tokujiros</strong></a></li>
      <li><a href="https://github.com/xord"><span>GitHub</span><strong>@xord</strong></a></li>
    </ul>
  </div>
</section>
