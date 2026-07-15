---
layout: page
title: Director Bio
permalink: /bio/
nav: true
nav_order: 1
---

<style>
.about-custom {
  max-width: 1200px;
  margin: 0 auto;
}

.about-label {
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.85rem;
  color: var(--global-theme-color);
  margin-bottom: 2.5rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.about-label::after {
  content: "";
  width: 60px;
  height: 1px;
  background: var(--global-theme-color);
  display: inline-block;
}

.about-layout {
  display: grid;
  grid-template-columns: 250px 1fr;
  gap: 3.5rem;
  align-items: start;
}

.about-sidebar img {
  width: 230px;
  height: 230px;
  border-radius: 50%;
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
  color: var(--global-text-color);
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

.about-main h1 {
  font-size: 2.5rem;
  line-height: 1.15;
  margin-bottom: 1.75rem;
  font-weight: 500;
}

.about-main h1 em {
  color: var(--global-theme-color);
  font-style: italic;
}

.about-main p {
  font-size: 1rem;
  line-height: 1.8;
  margin-bottom: 1.35rem;
}

.about-main a {
  text-decoration: underline;
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
    width: 220px;
    height: 220px;
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

<div class="about-label">About</div>

<div class="about-layout">

  <aside class="about-sidebar">

    <img src="{{ '/assets/img/profile-cheng.jpg' | relative_url }}" alt="Joey T. Cheng">

    <div class="about-socials">
      <a href="mailto:your-email@yorku.ca" aria-label="Email">
        <i class="fas fa-envelope"></i>
      </a>

      <a href="{{ '/cv/' | relative_url }}" aria-label="CV">
        <i class="ai ai-cv"></i>
      </a>

      <a href="https://scholar.google.com/" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar">
        <i class="ai ai-google-scholar"></i>
      </a>

      <a href="https://github.com/" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
        <i class="fab fa-github"></i>
      </a>

      <a href="https://osf.io/" target="_blank" rel="noopener noreferrer" aria-label="OSF">
        <i class="ai ai-osf"></i>
      </a>

      <a href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
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
      <p>Human Connection Lab Director</p>
      <p>Area Head, Social-Personality Psychology Unit</p>
    </div>

    <div class="about-card">
      <div class="about-card-title">Editorial Roles</div>
      <p>Associate Editor</p>
      <p>Editorial Board Member</p>
    </div>

    <div class="about-card">
      <div class="about-card-title">Education</div>
      <p>PhD, University of British Columbia</p>
      <p>BSc, University of Toronto</p>
    </div>

  </aside>

  <main class="about-main">

    <h1>
      I study <em>human connection</em> and the social forces that bring people together or pull them apart.
    </h1>

    <p>
      I am a social psychologist interested in how people navigate social life. My research examines how people gain influence in groups, how leaders emerge, and why some people become more connected to others while others become socially isolated.
    </p>

    <p>
      One major focus of my work is leadership and social status. I study the psychological and behavioral processes that shape influence, including confidence, voice, dominance, prestige, and fairness preferences. Much of this work asks why some people are more likely than others to be heard, recognized, and selected as leaders.
    </p>

    <p>
      My newer research examines loneliness and social isolation. I am interested in how social disconnection varies across people, places, and cultures, and how contemporary narratives about independence, self-protection, and withdrawal may shape the value people place on social connection.
    </p>

    <p>
      I am an Associate Professor in the <a href="https://www.yorku.ca/health/psychology/" target="_blank" rel="noopener noreferrer">Department of Psychology at York University</a>, where I direct the Human Connection Lab.
    </p>

    <p>
      My work has appeared in journals including <em>Journal of Experimental Psychology: General</em>, <em>Journal of Personality and Social Psychology</em>, <em>Psychological Science</em>, and other outlets in social, personality, and organizational psychology.
    </p>

    <p>
      In the Human Connection Lab, my students, collaborators, and I study topics including leadership, gender disparities in groups, prestige and dominance, social connection, loneliness, cultural change, and natural language processing approaches to social behavior.
    </p>

    <p>
      My academic journey: I earned my PhD (Social-Personality Psychology, with a minor in Quantitative Methods) at the University of British Columbia in 2013, then chased my curiosity about status and leadership south for a stint as a Visiting Scholar and Postdoctoral Fellow at UC Berkeley's Haas School of Business. These days I'm at York University, where I've been since 2019 — first as an Assistant Professor and, since 2023, as an Associate Professor in the Department of Psychology, and since 2022, the York Research Chair in Leadership, Collaboration, and Teams — proof that studying how people work together eventually convinces someone to let you lead a few things yourself.
    </p>

    <p>
      What keeps me in research is curiosity. I love the process of chasing a question I don't yet understand, picking up a new technical skill or an entirely new way of thinking about an old problem, and using what I learn to say something true about how people connect, lead, and belong. I care about doing this work carefully and honestly, and about building it together with people who care as much about getting it right as I do.
    </p>

    <p>
      Here are the <a href="https://joeytcheng.github.io/teaching/">courses I’ve taught</a>.
    </p>

    <a class="about-pill" href="https://joeytcheng.github.io/research/">
      Human Connection Lab Research
    </a>

  </main>

</div>

</div>