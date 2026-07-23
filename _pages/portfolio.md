---
layout: archive
title: "Code"
permalink: /code/
author_profile: true
---

<style>
.code-page * { box-sizing: border-box; }
.code-page {
  font-family: 'IBM Plex Sans', sans-serif;
  font-weight: 300;
  color: #141416;
  max-width: 860px;
}

/* ── Section headers ── */
.code-section { margin: 2.2rem 0 1rem; }
.code-section-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.1rem;
}
.code-section-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.05rem;
  font-weight: 600;
  color: #0d2b5e;
  white-space: nowrap;
}
.code-section-line { flex: 1; height: 1px; background: #e2ddd8; }

/* ── Repo cards ── */
.code-list { display: flex; flex-direction: column; }

.code-card {
  display: grid;
  grid-template-columns: 90px 1fr;
  gap: 0 1.2rem;
  padding: 1rem 0;
  border-bottom: 1px solid #eceae6;
}
.code-card:last-child { border-bottom: none; }

.code-tag {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.66rem;
  color: #bbb;
  padding-top: 0.22rem;
  text-align: right;
  letter-spacing: 0.02em;
  line-height: 1.5;
  text-transform: uppercase;
}

.code-title {
  font-size: 0.93rem;
  font-weight: 400;
  line-height: 1.45;
  margin: 0 0 0.2rem;
}
.code-title a { color: #141416; text-decoration: none; }
.code-title a:hover { color: #d4852a; }

.code-sub {
  font-size: 0.78rem;
  color: #666;
  line-height: 1.6;
  margin: 0.1rem 0;
}

.code-detail {
  font-size: 0.75rem;
  color: #999;
  font-style: italic;
  margin-top: 0.2rem;
}

.code-items {
  margin: 0.4rem 0 0 0;
  padding-left: 1.1rem;
  font-size: 0.78rem;
  color: #555;
  line-height: 1.75;
}

/* ── Badges ── */
.badge-row { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 0.5rem; }
.badge {
  font-size: 0.62rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 0.18rem 0.55rem;
  border-radius: 2px;
}
.badge-teaching  { background: #fdf0e8; color: #7a3d14; }
.badge-research  { background: #e8f0fb; color: #1a3a70; }

/* ── GitHub link ── */
.code-link {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  margin-top: 0.55rem;
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.04em;
  color: #0d2b5e;
  text-decoration: none;
  text-transform: uppercase;
}
.code-link:hover { color: #d4852a; text-decoration: underline; text-underline-offset: 2px; }

@media (max-width: 640px) {
  .code-card { grid-template-columns: 1fr; }
  .code-tag  { text-align: left; padding-bottom: 0.2rem; }
}
</style>

<div class="code-page">

<div class="code-page">

<!-- ─────────────────────────────────────────────────────────────────────── -->
<!-- Teaching Codes and Contributions                                      -->
<!-- ─────────────────────────────────────────────────────────────────────── -->

<div class="code-section">
  <div class="code-section-header">
    <span class="code-section-title">Teaching Codes and Contributions</span>
    <div class="code-section-line"></div>
  </div>

  <div class="code-list">

    <!-- PASD contribution -->
    <div class="code-card">
      <div class="code-tag">PASD</div>

      <div>
        <p class="code-title">
          <a href="https://github.com/jparras/dgm_classes/tree/main/videos"
             target="_blank"
             rel="noopener">
            Deep Generative Models — Video Materials
          </a>
        </p>

        <p class="code-sub">
          Contribution to the audiovisual teaching materials for the
          Procesado Avanzado de Señales y Datos course.
        </p>

        <p class="code-detail">
          Educational resources on deep generative models.
        </p>

        <div class="badge-row">
          <span class="badge badge-teaching">Teaching Contribution</span>
        </div>

        <a class="code-link"
           href="https://github.com/jparras/dgm_classes/tree/main/videos"
           target="_blank"
           rel="noopener">

          <svg width="12" height="12" viewBox="0 0 24 24"
               fill="none" stroke="currentColor" stroke-width="2">
            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>
          </svg>

          View contribution
        </a>
      </div>
    </div>


    <!-- Application Projects -->
    <div class="code-card">
      <div class="code-tag">APPR</div>

      <div>
        <p class="code-title">
          <a href="https://github.com/AlbaGarridoLopezz/Application-Projects-MUTSC"
             target="_blank"
             rel="noopener">
            Application Projects — MUTSC
          </a>
        </p>

        <p class="code-sub">
          Teaching materials and practical resources for the Application
          Projects course in the Master's Degree in Signal Theory and
          Communications.
        </p>

        <div class="badge-row">
          <span class="badge badge-teaching">Teaching</span>
        </div>

        <a class="code-link"
           href="https://github.com/AlbaGarridoLopezz/Application-Projects-MUTSC"
           target="_blank"
           rel="noopener">

          <svg width="12" height="12" viewBox="0 0 24 24"
               fill="none" stroke="currentColor" stroke-width="2">
            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>
          </svg>

          View on GitHub
        </a>
      </div>
    </div>

  </div>
</div>


<!-- ─────────────────────────────────────────────────────────────────────── -->
<!-- Research Codes                                                         -->
<!-- ─────────────────────────────────────────────────────────────────────── -->

<div class="code-section">
  <div class="code-section-header">
    <span class="code-section-title">Research Codes</span>
    <div class="code-section-line"></div>
  </div>

  <div class="code-list">

    <!-- SAMVAE -->
    <div class="code-card">
      <div class="code-tag">SAMVAE</div>

      <div>
        <p class="code-title">
          <a href="https://github.com/AlbaGarridoLopezz/SAMVAE"
             target="_blank"
             rel="noopener">
            SAMVAE
          </a>
        </p>

        <p class="code-sub">
          Open-source implementation of a multimodal variational autoencoder
          for survival analysis with competing risks.
        </p>

        <p class="code-detail">
          Code associated with the article
          “Deep Survival Analysis in Multimodal Medical Data:
          A Parametric and Probabilistic Approach with Competing Risks.”
        </p>

        <div class="badge-row">
          <span class="badge badge-research">Research</span>
          <span class="badge badge-research">Open Source</span>
        </div>

        <a class="code-link"
           href="https://github.com/AlbaGarridoLopezz/SAMVAE"
           target="_blank"
           rel="noopener">

          <svg width="12" height="12" viewBox="0 0 24 24"
               fill="none" stroke="currentColor" stroke-width="2">
            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>
          </svg>

          View on GitHub
        </a>
      </div>
    </div>


    <!-- Jensen-Shannon estimators -->
    <div class="code-card">
      <div class="code-tag">JSD</div>

      <div>
        <p class="code-title">
          <a href="URL_DEL_REPOSITORIO_JS"
             target="_blank"
             rel="noopener">
            Jensen–Shannon Divergence Estimators
          </a>
        </p>

        <p class="code-sub">
          Open-source package for the implementation and evaluation of
          Jensen–Shannon divergence estimators for synthetic-data validation.
        </p>

        <p class="code-detail">
          Code associated with the preprint
          “Not All Jensen-Shannon Divergence Estimators Are Equal.”
        </p>

        <div class="badge-row">
          <span class="badge badge-research">Research</span>
          <span class="badge badge-research">Open Source</span>
        </div>

        <a class="code-link"
           href="URL_DEL_REPOSITORIO_JS"
           target="_blank"
           rel="noopener">

          <svg width="12" height="12" viewBox="0 0 24 24"
               fill="none" stroke="currentColor" stroke-width="2">
            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>
          </svg>

          View on GitHub
        </a>
      </div>
    </div>

  </div>
</div>

</div><!-- /.code-page --> 