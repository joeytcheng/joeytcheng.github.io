---
layout: page
title: Lab Director
permalink: /bio/
nav: true
nav_order: 1
---

<style>
/*
 * Suppress the theme's own auto-rendered page title above the
 * white card — the eyebrow, name, and mission-statement heading
 * already inside the card form a complete header on their own.
 */

.post-header {
  display: none;
}

.about-custom {
  max-width: 1200px;
  margin: 2rem auto;
  background: var(--global-card-bg-color);
  border-radius: 16px;
  padding: 2.5rem 3rem;
}

@media (max-width: 700px) {
  .about-custom {
    padding: 1.75rem;
  }
}

.about-kicker {
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.75rem;
  font-weight: 500;
  color: var(--global-theme-color);
  margin-bottom: 0.5rem;
}

.about-title {
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 2.4rem;
  line-height: 1.1;
  font-weight: 700;
  margin-bottom: 2rem;
}

.about-layout {
  display: grid;
  grid-template-columns: 250px 1fr;
  gap: 3.5rem;
  align-items: start;
}

.about-sidebar img {
  width: 100%;
  max-width: 230px;
  height: auto;
  aspect-ratio: 3 / 4;
  border-radius: 16px;
  object-fit: cover;
  margin-bottom: 1rem;
}

.about-socials {
  margin: 0 0 1.5rem 0;
  display: flex;
  gap: 0.75rem;
  font-size: 1.3rem;
  justify-content: center;
  max-width: 230px;
}

.about-socials a {
  color: var(--icon-muted-color);
  text-decoration: none;
}

.about-socials a:hover {
  color: var(--global-theme-color);
}

.about-card {
  background: var(--global-card-bg-color);
  border-left: 1px solid var(--global-theme-color);
  padding: 1rem 1.25rem;
  margin-bottom: 1rem;
}

.about-card-title {
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.75rem;
  color: var(--global-theme-color);
  margin-bottom: 0.65rem;
}

.about-card p {
  margin-bottom: 0.35rem;
  line-height: 1.45;
}

.about-card a {
  color: var(--global-text-color);
  text-decoration: underline;
}

.about-eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.75rem;
  font-weight: 600;
  color: var(--global-theme-color);
  margin-bottom: 1rem;
}

.about-name-link {
  display: block;
  color: var(--global-theme-color);
  font-weight: 700;
  font-size: 2.4rem;
  font-family: Georgia, 'Times New Roman', serif;
  text-decoration: none;
  line-height: 1.1;
}

.about-divider {
  width: 40px;
  height: 2px;
  background: var(--global-theme-color);
  border: none;
  margin: 1.25rem 0;
}

.about-main h1 {
  font-size: 1.7rem;
  line-height: 1.4;
  font-style: italic;
  font-weight: 400;
  font-family: Georgia, 'Times New Roman', serif;
  margin-top: 1.5rem;
  margin-bottom: 1.75rem;
  max-width: 620px;
  border-left: 3px solid var(--global-theme-color);
  padding-left: 20px;
}

.about-quote-accent {
  color: var(--global-theme-color);
}

.about-main p {
  font-size: 1rem;
  line-height: 1.8;
  margin-bottom: 1.35rem;
}

.about-main a {
  text-decoration: underline;
}

.research-links {
  border-top: 1px solid var(--global-divider-color);
  padding-top: 1.25rem;
  margin-top: 2rem;
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  font-size: 0.9rem;
}

.research-links a {
  color: var(--global-theme-color);
  text-decoration: none;
}

.research-links .link-underline-text {
  text-decoration: underline;
  text-underline-offset: 0.2rem;
  color: var(--global-theme-color);
}

.about-pill {
  display: inline-block;
  border: 1px solid var(--global-theme-color);
  color: var(--global-theme-color);
  border-radius: 999px;
  padding: 0.45rem 0.9rem;
  font-size: 0.85rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-top: 0.75rem;
  text-decoration: none;
}

.about-pill:hover {
  color: var(--global-bg-color);
  background: var(--global-theme-color);
  text-decoration: none;
}

@media (max-width: 800px) {
  .about-layout {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .about-sidebar img {
    width: 100%;
    max-width: 220px;
    height: auto;
    aspect-ratio: 3 / 4;
  }

  .about-socials {
    max-width: 220px;
  }

  .about-main h1 {
    font-size: 2rem;
  }
}
</style>

<div class="about-custom">

<div class="about-kicker">Human Connection Lab</div>
<h1 class="about-title">Lab Director</h1>
<div class="title-rule"></div>

<div class="about-layout">

  <aside class="about-sidebar">

    <img src="{{ '/assets/img/profile-cheng.jpg' | relative_url }}" alt="Joey T. Cheng">

    <div class="about-socials">
      <a href="mailto:chengjt@yorku.ca" aria-label="Email">
        <i class="fas fa-envelope"></i>
      </a>

      <a href="https://scholar.google.com/citations?user=lweBpmIAAAAJ&hl=en" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar">
        <i class="ai ai-google-scholar"></i>
      </a>

      <a href="https://www.linkedin.com/in/joeytcheng/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
        <i class="fab fa-linkedin"></i>
      </a>
    </div>

    <div class="about-card">
      <div class="about-card-title">Affiliation</div>
      <p><a href="https://www.yorku.ca/health/psychology/" target="_blank" rel="noopener noreferrer">Department of Psychology</a></p>
      <p>York University</p>
    </div>

    <div class="about-card">
      <div class="about-card-title">Research Focus</div>
      <p>Social Connection · Loneliness · Leadership · Status · Groups · Culture</p>
    </div>

    <div class="about-card">
      <div class="about-card-title">Roles</div>
      <p>Associate Professor</p>
      <p>York Research Chair in Leadership, Collaboration, & Teams</p>
      <p>Lab Director, Human Connection Lab</p>
      <p>Area Head, Social-Personality Psychology Unit</p>
    </div>

    <div class="about-card">
      <div class="about-card-title">Education</div>
      <p>Postdoc, University of California, Berkeley</p>
      <p>PhD, University of British Columbia</p>
      <p>BSc, University of Toronto</p>
    </div>

  </aside>

  <main class="about-main">

    <div class="about-eyebrow">Associate Professor &middot; Department of Psychology<br>York University</div>

    <div class="about-name-link">Joey T. Cheng</div>

    <h1>
      I study <span class="about-quote-accent">human connection</span> — what brings people together, and what drives them apart.
    </h1>

    <p>
      I am an Associate Professor of Psychology and York Research Chair at York University, where I direct the <a href="{{ '/lab/' | relative_url }}">Human Connection Lab</a>. I completed my undergraduate degree at the University of Toronto in 2007, and my doctoral degree at the University of British Columbia in 2013. I then spent the next six years in the United States — first as a Postdoctoral Fellow at University of California, Berkeley's Haas School of Business, then as faculty at the University of California, Irvine and the University of Illinois at Urbana-Champaign. I returned home to Toronto and York University in 2019.
    </p>

    <p>
      I am a behavioral scientist and social psychologist interested in how people navigate social connection — both the connections we seek out, and the more complicated ones shaped by power and status. My research asks how people gain influence in groups, how leaders emerge, and why some people grow more connected to others while others grow isolated.
    </p>

    <p>
      My work spans two threads. One examines the tensions that make collaboration work — and sometimes make it hard — the confidence, voice, dominance, prestige, and egalitarian preferences that shape who is heard, respected, and trusted to lead. The other, newer thread examines loneliness and social isolation: how disconnection varies across people, places, and cultures, and how narratives about independence and self-protection shape the value we place on connection.
    </p>

    <p>
      What I love about research is the process of chasing a question I don't yet understand — picking up a new method or data analytic skill, or an entirely new way of thinking about an old problem — and using what I learn to say something about how people connect, collaborate, and belong. I care about exploring these questions, and about building this work together with people who care as much about getting it right as I do.
    </p>

    <div class="research-links">
      <a href="{{ '/publications/' | relative_url }}"><span class="link-underline-text">Publications</span> ↗</a>
      <a href="{{ '/lab/' | relative_url }}"><span class="link-underline-text">Meet the lab</span> ↗</a>
      <a href="{{ '/join-us/' | relative_url }}"><span class="link-underline-text">Join us</span> ↗</a>
      <a href="{{ '/contact/' | relative_url }}"><span class="link-underline-text">Contact us</span> ↗</a>
    </div>

  </main>

</div>

</div>
