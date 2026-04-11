---
layout: home
title: xord.org
lang: ja
permalink: /ja/
---

<section class="hero">
  <div class="container hero-inner">
    <p class="hero-eyebrow">Apps &amp; Open Source</p>
    <h1 class="hero-title">
      Indie apps<br>
      and <span class="accent">open-source<br>libraries</span>.
    </h1>
    <p class="hero-lede">
      iOS アプリと、その開発を支える OSS ライブラリを公開しています。
      企画から実装、OSS のメンテまで、基本的に全部ひとりでやっています。
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
        自作の <strong>iOS アプリ</strong> と、その開発を支えるための <strong>OSS ライブラリ</strong> を公開しています。
        アプリは App Store で、ライブラリは RubyGems / GitHub で配布しています。
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
    <p class="section-lede">公開中の iOS アプリです。</p>
    <div class="cards apps-grid">
      {% for app in site.data.apps %}
      <a class="card app-card accent-{{ app.accent }}" href="{{ app.url | relative_url }}">
        <h3 class="card-title">{{ app.name }}</h3>
        <p class="card-tagline">{{ app.description_ja }}</p>
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
      公開中の OSS ライブラリです。主にアプリの足回りを作るためのもので、RubyGems で配布しています。
    </p>
    <div class="cards gems-grid">
      {% for gem in site.data.gems %}
      <a class="card gem-card" href="{{ gem.url }}">
        <h3 class="card-title mono">{{ gem.name }}</h3>
        <p class="card-tagline">{{ gem.tagline_ja }}</p>
        <span class="card-link">RubyGems →</span>
      </a>
      {% endfor %}
    </div>
    <p class="oss-aside">
      C++ / Objective-C レイヤは CocoaPod でも配布しています →
      <a href="https://github.com/xord/cruby">CRuby</a>
    </p>
  </div>
</section>

<section class="section contact" id="contact">
  <div class="container">
    <p class="section-eyebrow">04 — Contact</p>
    <h2 class="section-title">Contact</h2>
    <p class="contact-lede">お仕事の相談、アプリへのフィードバック、OSS のお問い合わせなどはこちらから。</p>
    <ul class="contact-list">
      <li><a href="https://x.com/xordog"><span>X</span><strong>@xordog</strong></a></li>
      <li><a href="https://github.com/xord"><span>GitHub</span><strong>@xord</strong></a></li>
    </ul>
  </div>
</section>
