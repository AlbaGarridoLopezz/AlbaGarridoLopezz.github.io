---
permalink: /
title: "About me"
excerpt: "AI, optimization, and signal processing for healthcare, autonomous systems, and industry"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% assign all_pubs        = site.data.publications %}
{% assign journals        = all_pubs | where: "type", "journal" %}
{% assign q1_pubs         = journals | where: "quartile", "Q1" %}
{% assign all_projects    = site.data.projects %}
{% assign eu_projects     = all_projects | where: "funding_type", "european" %}
{% assign all_theses      = site.data.theses %}
{% assign recent_pubs     = all_pubs | slice: 0, 5 %}
{% assign metrics = site.data.metrics %}

<style>
.about-page * { box-sizing: border-box; }

.about-page {
  font-family: 'IBM Plex Sans', sans-serif;
  font-weight: 300;
  color: #141416;
  max-width: 860px;
}

/* ── Hero ───────────────────────────────────────────── */
.hero {
  margin: 0.6rem 0 2rem;
}
.hero-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.05rem;
  font-weight: 600;
  color: #0d2b5e;
  white-space: nowrap;
  letter-spacing: 0.01em;
  margin-bottom: 0.6rem;
}
.hero-subtitle {
  font-size: 0.9rem;
  line-height: 1.8;
  color: #333;
}
.hero-cta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
  margin-top: 1.2rem;
}
.hero-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.5rem 0.95rem;
  border: 1px solid #d8d3cc;
  border-radius: 3px;
  text-decoration: none;
  font-size: 0.82rem;
  font-weight: 500;
  letter-spacing: 0.03em;
  transition: all 0.15s;
}
.hero-btn-primary {
  background: #0d2b5e;
  color: #fff;
  border-color: #0d2b5e;
}
.hero-btn-primary:hover {
  background: #0a2147;
  color: #fff;
}
.hero-btn-secondary {
  color: #0d2b5e;
  background: #fff;
}
.hero-btn-secondary:hover {
  border-color: #0d2b5e;
  color: #0d2b5e;
  background: #faf7f3;
}

/* ── Logos ──────────────────────────────────────────── */
.logo-strip {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 1.2rem;
  margin: 1.6rem 0 2.1rem;
  padding: 1rem 0;
  border-top: 1px solid #eceae6;
  border-bottom: 1px solid #eceae6;
}

.logo-item {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 56px;
  padding: 0.35rem 0.55rem;
  border-radius: 4px;
}

.logo-item img {
  height: 44px;
  width: auto;
  object-fit: contain;
  display: block;
  opacity: 0.98;
}

.logo-item.logo-iptc {
  background: #0d2b5e;
  padding: 0.45rem 0.7rem;
}

/* ── Metrics ────────────────────────────────────────── */
.metrics-bar {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 0;
  border: 1px solid #e2ddd8;
  border-radius: 4px;
  margin: 2rem 0 2.4rem;
  overflow: hidden;
}
.metric-item {
  padding: 1.3rem 0.8rem;
  text-align: center;
  border-right: 1px solid #e2ddd8;
  transition: background 0.18s;
}
.metric-item:last-child { border-right: none; }
.metric-item:hover { background: #faf7f3; }
.metric-number {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: 2rem;
  font-weight: 700;
  color: #0d2b5e;
  line-height: 1;
}
.metric-label {
  display: block;
  font-size: 0.66rem;
  font-weight: 500;
  letter-spacing: 0.09em;
  text-transform: uppercase;
  color: #8a8789;
  margin-top: 0.4rem;
}

/* ── Sections ───────────────────────────────────────── */
.about-section {
  margin: 2.4rem 0 1.4rem;
}
.about-section-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}
.about-section-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.05rem;
  font-weight: 600;
  color: #0d2b5e;
  white-space: nowrap;
}
.about-section-line {
  flex: 1;
  height: 1px;
  background: #e2ddd8;
}

.about-text {
  font-size: 0.9rem;
  line-height: 1.8;
  color: #333;
}

/* ── Expertise badges ───────────────────────────────── */
.badge-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin-top: 0.9rem;
}
.badge {
  font-size: 0.62rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 0.22rem 0.58rem;
  border-radius: 2px;
  background: #e8f0fb;
  color: #1a3a70;
}

/* ── Audience cards ─────────────────────────────────── */
.audience-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}
.audience-card {
  border: 1px solid #e2ddd8;
  border-radius: 4px;
  padding: 1.1rem 1.1rem 1rem;
  background: #fff;
}
.audience-card:hover {
  background: #faf7f3;
}
.audience-title {
  font-size: 0.92rem;
  font-weight: 500;
  color: #141416;
  margin-bottom: 0.45rem;
}
.audience-text {
  font-size: 0.82rem;
  line-height: 1.7;
  color: #555;
}
.audience-link {
  display: inline-block;
  margin-top: 0.7rem;
  font-size: 0.78rem;
  font-weight: 500;
  color: #0d2b5e;
  text-decoration: none;
}
.audience-link:hover {
  color: #d4852a;
}

/* ── Publications list ──────────────────────────────── */
.pub-list {
  display: flex;
  flex-direction: column;
}
.pub-item {
  display: grid;
  grid-template-columns: 60px 1fr;
  gap: 0 1rem;
  padding: 0.9rem 0;
  border-bottom: 1px solid #eceae6;
}
.pub-item:last-child { border-bottom: none; }
.pub-year {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.72rem;
  color: #bbb;
  text-align: right;
  padding-top: 0.22rem;
}
.pub-title {
  font-size: 0.9rem;
  line-height: 1.5;
  margin: 0 0 0.2rem;
}
.pub-title a {
  color: #141416;
  text-decoration: none;
}
.pub-title a:hover { color: #d4852a; }
.pub-meta {
  font-size: 0.78rem;
  color: #666;
  line-height: 1.6;
}

.section-cta {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  margin-top: 0.9rem;
  font-size: 0.78rem;
  color: #0d2b5e;
  text-decoration: none;
  font-weight: 500;
}
.section-cta:hover { color: #d4852a; }

/* ── Quick links ────────────────────────────────────── */
.quick-links {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1px;
  background: #e2ddd8;
  border: 1px solid #e2ddd8;
  border-radius: 4px;
  overflow: hidden;
}
.quick-link {
  background: #fff;
  padding: 1rem;
  text-align: center;
  text-decoration: none;
  color: #141416;
}
.quick-link:hover {
  background: #faf7f3;
}
.quick-link-title {
  display: block;
  font-size: 0.82rem;
  font-weight: 500;
  color: #0d2b5e;
}
.quick-link-sub {
  display: block;
  margin-top: 0.25rem;
  font-size: 0.7rem;
  color: #888;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

@media (max-width: 700px) {
  .metrics-bar { grid-template-columns: repeat(3, 1fr); }
  .audience-grid { grid-template-columns: 1fr; }
  .quick-links { grid-template-columns: repeat(2, 1fr); }
  .pub-item { grid-template-columns: 1fr; }
  .pub-year { text-align: left; padding-bottom: 0.25rem; }
}
</style>

<div class="about-page">

<div class="hero">
  <div class="hero-title">Applied AI research with impact</div>
  <div class="hero-subtitle">
    Ph.D. candidate at <a href="https://www.upm.es/" target="_blank" rel="noopener">UPM</a> researching on applied Artificial Intelligence for personalized medicine.
  </div>

  <div class="hero-cta-row">
    <a class="hero-btn hero-btn-primary" href="../publications">View Publications</a>
    <a class="hero-btn hero-btn-secondary" href="../projects">View Projects</a>
    <a class="hero-btn hero-btn-secondary" href="../cv">View CV</a>
  </div>
</div>

<div class="logo-strip">
  <div class="logo-item"><a href="https://www.gaps.ssr.upm.es/" target="_blank" rel="noopener"><img src="/images/logo_gaps.png" alt="GAPS"></a></div>
  <div class="logo-item"><a href="https://www.ssr.upm.es/" target="_blank" rel="noopener"><img src="/images/logo_ssr.png" alt="SSR"></a></div>
  <div class="logo-item"><a href="https://www.etsit.upm.es/" target="_blank" rel="noopener"><img src="/images/logo_etsit.png" alt="ETSIT"></a></div>
  <div class="logo-item"><a href="https://www.upm.es/" target="_blank" rel="noopener"><img src="/images/logo_upm.png" alt="UPM"></a></div>
  <div class="logo-item logo-iptc"><a href="https://iptc.upm.es/" target="_blank" rel="noopener"><img src="/images/logo_iptc.png" alt="IPTC"></a></div>
</div>

<div class="metrics-bar">
  <div class="metric-item">
    <span class="metric-number">{{ all_pubs | size }}</span>
    <span class="metric-label">Publications</span>
  </div>
  <div class="metric-item">
    <span class="metric-number">{{ q1_pubs | size }}</span>
    <span class="metric-label">Q1 Journals</span>
  </div>
  <div class="metric-item">
    <span class="metric-number">{{ all_projects | size }}</span>
    <span class="metric-label">R&D Projects</span>
  </div>
  <div class="metric-item">
    <span class="metric-number">{{ metrics.citations }}</span>
    <span class="metric-label">Citations</span>
  </div>
  <div class="metric-item">
    <span class="metric-number">{{ metrics.h_index }}</span>
    <span class="metric-label">H-Index</span>
  </div>
</div>

<div class="about-section">
  <div class="about-section-header">
    <span class="about-section-title">Research Profile</span>
    <div class="about-section-line"></div>
  </div>
  <div class="about-text">
    My work focuses on combining machine learning, optimization, and signal processing to solve real-world problems. My research encompasses medical applications, autonomous navigation, cybersecurity, communications, industrial applications, and audio-related problems.
  </div>
  <div class="badge-row">
    <span class="badge">Healthcare AI</span>
    <span class="badge">Federated Learning</span>
    <span class="badge">Signal Processing</span>
    <span class="badge">Optimal Control</span>
    <span class="badge">Autonomous Navigation</span>
    <span class="badge">Applied AI</span>
  </div>
</div>

<div class="about-section">
  <div class="about-section-header">
    <span class="about-section-title">Collaborate / Join</span>
    <div class="about-section-line"></div>
  </div>

  <div class="audience-grid">
    <div class="audience-card">
      <div class="audience-title">For Students</div>
      <div class="audience-text">
        If you are a UPM student interested in applying AI, machine learning, optimization, or signal processing to your Bachelor's or Master's thesis, feel free to contact me. Topics may include healthcare AI, autonomous systems, communications, and data-driven industrial applications.
      </div>
      <a class="audience-link" href="../teaching">Teaching and supervision →</a>
    </div>

    <div class="audience-card">
      <div class="audience-title">For Industry & Institutions</div>
      <div class="audience-text">
        I collaborate with companies and institutions interested in applying AI to real-world challenges, especially in healthcare, autonomous systems, and industrial data analysis. I am open to joint R&amp;D, consulting, and collaborative research projects.
      </div>
      <a class="audience-link" href="../projects">Research projects →</a>
    </div>
  </div>
</div>

<div class="about-section">
  <div class="about-section-header">
    <span class="about-section-title">Latest Publications</span>
    <div class="about-section-line"></div>
  </div>

  <div class="pub-list">
    {% for pub in recent_pubs %}
    <div class="pub-item">
      <div class="pub-year">{{ pub.year }}</div>
      <div>
        <p class="pub-title">
          {% if pub.doi %}
          <a href="{{ pub.doi }}" target="_blank" rel="noopener">{{ pub.title }}</a>
          {% else %}
          {{ pub.title }}
          {% endif %}
        </p>
        <div class="pub-meta">
          {{ pub.authors }}<br>
          {% if pub.journal %}{{ pub.journal }}{% endif %}{% if pub.journal and pub.venue %} · {% endif %}{% if pub.venue %}{{ pub.venue }}{% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

  <a class="section-cta" href="../publications">Browse full publication list →</a>
</div>

{% assign media_items = site.data.media | default: empty %}
{% assign media_count = media_items | size %}

{% if media_count > 0 %}
<div class="about-section">
  <div class="about-section-header">
    <span class="about-section-title">In the Media</span>
    <div class="about-section-line"></div>
  </div>

  <div class="pub-list">
    {% assign sorted_media = media_items | sort: "year" | reverse %}
    {% for item in sorted_media %}
    <div class="pub-item">
      <div class="pub-year">{{ item.year }}</div>
      <div>
        <p class="pub-title">
          {% if item.url %}
          <a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.title }}</a>
          {% else %}
          {{ item.title }}
          {% endif %}
        </p>
        <div class="pub-meta">
          {{ item.outlet }}
          {% if item.kind %} · {{ item.kind }}{% endif %}
          {% if item.topic %} · {{ item.topic }}{% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
{% endif %}

<div class="about-section">
  <div class="about-section-header">
    <span class="about-section-title">Explore</span>
    <div class="about-section-line"></div>
  </div>

  <div class="quick-links">
    <a class="quick-link" href="../publications">
      <span class="quick-link-title">Publications</span>
      <span class="quick-link-sub">Research outputs</span>
    </a>
    <a class="quick-link" href="../projects">
      <span class="quick-link-title">Projects</span>
      <span class="quick-link-sub">Research & funding</span>
    </a>
    <a class="quick-link" href="../teaching">
      <span class="quick-link-title">Teaching</span>
      <span class="quick-link-sub">Courses & supervision</span>
    </a>
    <a class="quick-link" href="../cv">
      <span class="quick-link-title">CV</span>
      <span class="quick-link-sub">Full academic record</span>
    </a>
  </div>
</div>

</div>
