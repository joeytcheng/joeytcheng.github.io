---
layout: page
permalink: /lab/
title: The Team
description: Meet the team.
nav: true
nav_order: 3
---

<style>
.people-page {
  max-width: 900px;
  margin: 2rem auto;
  background: var(--global-card-bg-color);
  border-radius: 16px;
  padding: 2.5rem 3rem;
}

@media (max-width: 700px) {
  .people-page {
    padding: 1.75rem;
  }
}

.people-kicker {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.75rem;
  color: var(--global-theme-color);
  margin-bottom: 0.5rem;
}

.people-title {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 1.5rem;
}

.people-banner {
  background: var(--global-theme-color);
  color: var(--global-bg-color);
  text-align: center;
  padding: 0.75rem;
  margin-bottom: 2rem;
  font-size: 0.95rem;
}

.people-banner a {
  color: var(--global-bg-color);
  text-decoration: underline;
  font-weight: 600;
}

.people-section {
  margin-top: 2.5rem;
  border-bottom: 1px solid var(--global-divider-color);
  padding-bottom: 1.5rem;
}

.people-section h2,
.people-grid-section h2 {
  text-transform: uppercase;
  font-size: 1.45rem;
  letter-spacing: 0.5px;
  margin-bottom: 1.5rem;
}

.person {
  display: flex;
  gap: 1.75rem;
  align-items: flex-start;
  margin-bottom: 2rem;
}

.person-photo {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  object-fit: cover;
  flex-shrink: 0;
}

.person-info {
  flex: 1;
}

.person-name-line {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  flex-wrap: wrap;
  margin-bottom: 0.15rem;
}

.person-name {
  font-weight: 700;
  text-transform: uppercase;
}

.person-icons-inline {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 1.05rem;
}

.person-icons-inline a {
  color: var(--icon-muted-color);
  text-decoration: none;
}

.person-icons-inline a:hover {
  color: var(--global-theme-color);
}

.person-role {
  font-style: italic;
  margin-bottom: 0.5rem;
}

.person p {
  margin-bottom: 0.75rem;
}

/* Grid sections */

.people-grid-section {
  margin-top: 2.5rem;
  border-bottom: 1px solid var(--global-divider-color);
  padding-bottom: 2rem;
}

.people-grid {
  display: grid;
  gap: 1.5rem;
}

.people-grid.three {
  grid-template-columns: repeat(3, 1fr);
}

.people-grid.five {
  grid-template-columns: repeat(5, 1fr);
}

.grid-person {
  text-align: center;
}

.grid-person-photo {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 0.75rem;
}

.grid-person-name {
  font-weight: 700;
  text-transform: uppercase;
  font-size: 0.95rem;
}

.grid-person-role {
  font-size: 0.9rem;
  font-style: italic;
}

.grid-person-topic {
  font-size: 0.9rem;
  font-style: normal;
}

/* Mobile-friendly layout */

@media (max-width: 800px) {
  .people-grid.five {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 600px) {
  .person {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .person-photo {
    width: 160px;
    height: 160px;
  }

  .person-name-line {
    justify-content: center;
  }

  .people-grid.three,
  .people-grid.five {
    grid-template-columns: repeat(2, 1fr);
  }

  .grid-person-photo {
    width: 110px;
    height: 110px;
  }
}

@media (max-width: 400px) {
  .people-grid.three,
  .people-grid.five {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="people-page">

<div class="people-kicker">Human Connection Lab</div>

<h1 class="people-title">The Team</h1>

<div class="people-banner">
  We are growing! To learn more, please <a href="{{ '/contact/' | relative_url }}">contact us</a>.
</div>

<section class="people-section">

<h2>Lab Director</h2>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/profile-cheng.jpg' | relative_url }}" alt="Joey T. Cheng">

  <div class="person-info">

    <div class="person-name-line">
      <div class="person-name">Joey T. Cheng</div>

      <div class="person-icons-inline">
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
    </div>

    <div class="person-role">Lab Director</div>

    <p>
      Joey studies social behavior, leadership, status, and social connection. Her research examines how people
      navigate groups, how leaders emerge, and why people are becoming more or less connected to one another.
    </p>

  </div>
</div>

</section>

<section class="people-section">

<h2>Graduate Students</h2>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/profile-too.jpg' | relative_url }}" alt="Miranda Too">

  <div class="person-info">

    <div class="person-name-line">
      <div class="person-name">Miranda Too</div>

      <div class="person-icons-inline">
        <a href="mailto:mtoo@yorku.ca" aria-label="Email">
          <i class="fas fa-envelope"></i>
        </a>

        <a href="http://mirandatoo.com/" target="_blank" rel="noopener noreferrer" aria-label="Website">
          <i class="fas fa-globe"></i>
        </a>
      </div>
    </div>

    <div class="person-role">PhD Student, Social-Personality Psychology</div>

    <p>
      Miranda studies humility, prestige, and reputation.
    </p>

  </div>
</div>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/profile-arshinoff.jpg' | relative_url }}" alt="Spencer Arshinoff">

  <div class="person-info">

    <div class="person-name-line">
      <div class="person-name">Spencer Arshinoff</div>

      <div class="person-icons-inline">
        <a href="mailto:sarshin@yorku.ca" aria-label="Email">
          <i class="fas fa-envelope"></i>
        </a>

        <a href="https://www.linkedin.com/in/spencerarshinoff/" target="_blank" rel="noopener noreferrer" aria-label="Website">
          <i class="fas fa-globe"></i>
        </a>
      </div>
    </div>

    <div class="person-role">PhD Student, Social-Personality Psychology</div>

    <p>
      Spencer studies attitudes toward work, cultural change, social values, and temporal analysis.
    </p>

  </div>
</div>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/profile-lisophie.jpg' | relative_url }}" alt="Sophie Li">

  <div class="person-info">

    <div class="person-name-line">
      <div class="person-name">Sophie Li</div>

      <div class="person-icons-inline">
        <a href="mailto:sophie96@yorku.ca" aria-label="Email">
          <i class="fas fa-envelope"></i>
        </a>

        <a href="https://jysophieli.weebly.com/" target="_blank" rel="noopener noreferrer" aria-label="Website">
          <i class="fas fa-globe"></i>
        </a>
      </div>
    </div>

    <div class="person-role">PhD Student, Social-Personality Psychology</div>

    <p>
      Sophie studies conflict resolution, political apologies, and natural language processing.
    </p>

  </div>
</div>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/profile-torres.jpg' | relative_url }}" alt="Adrian Torres">

  <div class="person-info">

    <div class="person-name-line">
      <div class="person-name">Adrian Torres</div>

      <div class="person-icons-inline">
        <a href="mailto:apt98@yorku.ca" aria-label="Email">
          <i class="fas fa-envelope"></i>
        </a>

        <a href="https://maggietoplak.com/lab-members/" target="_blank" rel="noopener noreferrer" aria-label="Website">
          <i class="fas fa-globe"></i>
        </a>
      </div>
    </div>

    <div class="person-role">PhD Student, Clinical-Developmental Psychology</div>

    <p>
      Adrian studies performance, voice, and confidence.
    </p>

  </div>
</div>

</section>

<section class="people-grid-section">

<h2>Undergraduate Researchers</h2>

<div class="people-grid three">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-martelt.jpg' | relative_url }}" alt="Tatijanna Martel">
    <div class="grid-person-name">Tatijanna Martel</div>
    <div class="grid-person-role">Independent Research Project</div>
    <div class="grid-person-topic">Loneliness &amp; Social Isolation</div>
  </div>

</div>

</section>

<section class="people-grid-section">

<h2>Graduate Lab Alumni</h2>

<div class="people-grid three">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-drisdelle.jpg' | relative_url }}" alt="Emily Drisdelle">
    <div class="grid-person-name">Emily Drisdelle</div>
    <div class="grid-person-role">MA Alumna</div>
  </div>

<div class="grid-person">
  <img class="grid-person-photo" src="{{ '/assets/img/profile-arshad.jpg' | relative_url }}" alt="Memoona Arshad">
  <div class="grid-person-name">
    <a href="https://www.linkedin.com/in/memoona-arshad-017630238/" target="_blank" rel="noopener noreferrer">
      Memoona Arshad
    </a>
  </div>
  <div class="grid-person-topic">Program Evaluation Lead, Jack.org</div>
</div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-vogt.jpg' | relative_url }}" alt="Randi Vogt">
    <div class="grid-person-name">Randi Vogt</div>
    <div class="grid-person-role">Graduate Alumna</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-chenfx.jpg' | relative_url }}" alt="Fan Xuan Chen">
    <div class="grid-person-name">Fan Xuan Chen</div>
    <div class="grid-person-role">MA Alumna</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-watanabe.jpg' | relative_url }}" alt="Shoko Watanabe">
    <div class="grid-person-name">Shoko Watanabe</div>
    <div class="grid-person-role">Graduate Alumna</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-wuyuejun.jpg' | relative_url }}" alt="Yue Jun Wu">
    <div class="grid-person-name">Yue Jun Wu</div>
    <div class="grid-person-role">Graduate Alumna</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-liamy.jpg' | relative_url }}" alt="Amy Li">
    <div class="grid-person-name">Amy Li</div>
    <div class="grid-person-role">Graduate Alumna</div>
  </div>

</div>


</section>

<section class="people-grid-section">

<h2>Former Visiting Researchers</h2>

<div class="people-grid three">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-leckelt.jpg' | relative_url }}" alt="Marius Leckelt">
    <div class="grid-person-name">Marius Leckelt</div>
    <div class="grid-person-role">Graduate Alumnus</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-redhead.jpg' | relative_url }}" alt="Daniel Redhead">
    <div class="grid-person-name">Daniel Redhead</div>
    <div class="grid-person-role">Graduate Alumnus</div>
  </div>
  
</div>

</section>

<section class="people-grid-section">

<h2>Undergraduate Lab Alumni (selected)</h2>

<div class="people-grid five">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-aiyub.jpg' | relative_url }}" alt="Aliya Aiyub">
    <div class="grid-person-name">Aliya Aiyub</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-ikram.jpg' | relative_url }}" alt="Yumna Ikram">
    <div class="grid-person-name">Yumna Ikram</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-padala.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Akhila Padala</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-wangmilton.jpg' | relative_url }}" alt="Milton Wang">
    <div class="grid-person-name">Milton Wang</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-helm.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Eric Helm</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-clifford.jpg' | relative_url }}" alt="Florence Clifford">
    <div class="grid-person-name">Florence Clifford</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-zhangyiwei.jpg' | relative_url }}" alt="Yiwei Zhang">
    <div class="grid-person-name">Yiwei Zhang</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

</div>

</section>

</div>