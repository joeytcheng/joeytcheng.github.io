---
layout: page
title:
permalink: /
nav: false
---

<style>
.landing-page {
  max-width: 1050px;
  margin: 0 auto;
}

.landing-hero {
  padding: 3.5rem 0 3rem;
}

.landing-badge {
  display: inline-block;
  background: var(--global-theme-color);
  color: var(--global-bg-color);
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  padding: 0.35rem 0.75rem;
  border-radius: 4px;
  margin-bottom: 1.25rem;
}

.landing-title {
  font-size: 2.6rem;
  line-height: 1.15;
  font-weight: 500;
  margin-bottom: 1.25rem;
}

.landing-intro {
  font-size: 1.02rem;
  line-height: 1.8;
  max-width: 620px;
  margin-bottom: 1.25rem;
}

.landing-director {
  font-size: 0.95rem;
  line-height: 1.7;
  color: var(--global-text-color-light);
  max-width: 620px;
  margin-bottom: 1.75rem;
}

.landing-actions {
  display: flex;
  gap: 0.9rem;
  flex-wrap: wrap;
}

.landing-link {
  color: var(--global-theme-color);
  font-size: 0.95rem;
  text-decoration: none;
}

.landing-link:hover {
  text-decoration: underline;
  text-underline-offset: 0.2rem;
}

.landing-questions {
  background: var(--global-theme-color);
  color: var(--global-bg-color);
  padding: 2.75rem 2rem 3.25rem;
  border-radius: 12px;
  margin-bottom: 3rem;
}

.questions-header {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 0.5rem;
}

.questions-header h2 {
  font-size: 1.4rem;
  font-weight: 500;
  margin: 0;
}

.questions-link {
  font-size: 0.85rem;
  color: var(--global-bg-color);
  text-decoration: underline;
  white-space: nowrap;
}

.questions-link:hover {
  color: var(--global-bg-color);
}

.questions-intro {
  font-size: 0.95rem;
  line-height: 1.7;
  max-width: 620px;
  opacity: 0.9;
  margin-bottom: 2rem;
}

.questions-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.25rem;
}

.question-card {
  background: var(--global-bg-color);
  color: var(--global-text-color);
  border-radius: 10px;
  padding: 1.5rem;
}

.question-icon {
  font-size: 2.5rem;
  color: var(--global-theme-color);
  margin-bottom: 1rem;
}

.question-title {
  font-size: 1.05rem;
  font-weight: 500;
  margin-bottom: 0.5rem;
}

.question-body {
  font-size: 0.9rem;
  line-height: 1.6;
}

.landing-footer {
  background: var(--global-theme-color);
  color: var(--global-bg-color);
  padding: 2.5rem 2rem;
  border-radius: 12px;
  margin-bottom: 2rem;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}

.footer-heading {
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  margin-bottom: 1rem;
}

.footer-line {
  font-size: 0.9rem;
  line-height: 1.9;
}

.footer-line a {
  color: var(--global-bg-color);
  text-decoration: underline;
}

@media (max-width: 700px) {
  .landing-title {
    font-size: 2rem;
  }

  .questions-grid {
    grid-template-columns: 1fr;
  }

  .footer-grid {
    grid-template-columns: 1fr;
    gap: 1.75rem;
  }
}
</style>

<div class="landing-page">

<section class="landing-hero">

  <div class="landing-badge">York University</div>

  <h1 class="landing-title">Human Connection Lab</h1>

  <p class="landing-intro">
    Welcome to the <strong>Human Connection Lab</strong> at York University. We study how people connect, lead, and belong in groups, organizations, and society, and how social forces bring people together or pull them apart.
  </p>

  <p class="landing-director">
    Directed by Joey T. Cheng, Associate Professor of Psychology, York University.
  </p>

  <div class="landing-actions">
    <a class="landing-link" href="{{ '/bio/' | relative_url }}">Lab Director Bio ↗</a>
    <a class="landing-link" href="{{ '/lab/' | relative_url }}">Meet the lab ↗</a>
  </div>

</section>

<section class="landing-questions">

  <div class="questions-header">
    <h2>Research questions</h2>
    <a class="questions-link" href="{{ '/research/' | relative_url }}">More on our research &rarr;</a>
  </div>

  <p class="questions-intro">
    A brief preview of the questions that organize our work.
  </p>

  <div class="questions-grid">

    <div class="question-card">
      <div class="question-icon"><i class="fas fa-map-location-dot"></i></div>
      <div class="question-title">Why are so many of us feeling more disconnected?</div>
      <div class="question-body">We use surveys, behavioral data, and text analysis to measure loneliness and well-being across people, places, and cultures.</div>
    </div>

    <div class="question-card">
      <div class="question-icon"><i class="fas fa-network-wired"></i></div>
      <div class="question-title">How do the stories we tell shape whether we feel connected?</div>
      <div class="question-body">We study how cultural narratives about independence, self-protection, and belonging shape social life.</div>
    </div>

    <div class="question-card">
      <div class="question-icon"><i class="fas fa-comments"></i></div>
      <div class="question-title">Why do some voices get heard more than others?</div>
      <div class="question-body">We study why certain people are more likely to be recognized, included, and heard in groups, and what that means for equity.</div>
    </div>

    <div class="question-card">
      <div class="question-icon"><i class="fas fa-users"></i></div>
      <div class="question-title">What makes someone worth following?</div>
      <div class="question-body">We study the everyday behaviors, confidence, voice, and fairness, that shape who earns influence and trust.</div>
    </div>

  </div>

</section>

<section class="landing-footer">

  <div class="footer-grid">

    <div>
      <div class="footer-heading">Contact info</div>
      <div class="footer-line">Email | <a href="mailto:chengjt@yorku.ca">chengjt@yorku.ca</a></div>
      <div class="footer-line"><a href="{{ '/contact/' | relative_url }}">Contact page &rarr;</a></div>
    </div>

    <div>
      <div class="footer-heading">Join the team</div>
      <div class="footer-line">If you're interested in joining, you can find out more <a href="{{ '/contact/' | relative_url }}">here</a>.</div>
    </div>

  </div>

</section>

</div>
