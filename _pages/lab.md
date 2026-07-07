---
layout: page
permalink: /lab/
title: Human Connection Lab
description: Current and past lab members.
nav: true
nav_order: 3
---

<style>
.people-page {
  max-width: 900px;
  margin: 0 auto;
}

.people-title {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 1.5rem;
}

.people-banner {
  background: #426f9f;
  color: white;
  text-align: center;
  padding: 0.75rem;
  margin-bottom: 2rem;
  font-size: 0.95rem;
}

.people-banner a {
  color: white;
  text-decoration: underline;
  font-weight: 600;
}

.people-section {
  margin-top: 2.5rem;
  border-bottom: 2px solid #426f9f;
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

.person-name {
  font-weight: 700;
  text-transform: uppercase;
  margin-bottom: 0.15rem;
}

.person-role {
  font-style: italic;
  margin-bottom: 0.5rem;
}

.person-links {
  font-size: 0.9rem;
  margin-bottom: 0.75rem;
}

.person-links a {
  text-decoration: underline;
}

.person p {
  margin-bottom: 0.75rem;
}

/* Grid sections */

.people-grid-section {
  margin-top: 2.5rem;
  border-bottom: 2px solid #426f9f;
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

<h1 class="people-title">The Team</h1>

<div class="people-banner">
  We are growing! To learn more, please <a href="{{ '/contact/' | relative_url }}">contact</a> us.
</div>

<section class="people-section">

<h2>Lab Director</h2>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Joey T. Cheng">

  <div class="person-info">
    <div class="person-name">Joey T. Cheng</div>
    <div class="person-role">Lab Director</div>

    <div class="person-links">
      <a href="{{ '/cv/' | relative_url }}">CV</a> |
      <a href="mailto:your-email@yorku.ca">Email</a> |
      <a href="https://scholar.google.com/">Google Scholar</a> |
      <a href="https://osf.io/">OSF</a>
    </div>

    <p>
      Joey studies social behavior, leadership, status, and social connection. Her research examines how people
      navigate groups, how leaders emerge, and why people are becoming more or less connected to one another.
    </p>
  </div>
</div>

</section>

<section class="people-section">

<h2>Current Graduate Students</h2>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Miranda Too">

  <div class="person-info">
    <div class="person-name">Miranda Too</div>
    <div class="person-role">PhD Student, Social-Personality Psychology</div>

    <div class="person-links">
      <a href="mailto:student-email@yorku.ca">Email</a> |
      <a href="https://example.com">Website</a>
    </div>

    <p>
      Miranda studies humility, prestige, and reputation.
    </p>
  </div>
</div>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Spencer Arshinoff">

  <div class="person-info">
    <div class="person-name">Spencer Arshinoff</div>
    <div class="person-role">PhD Student, Social-Personality Psychology</div>

    <div class="person-links">
      <a href="mailto:student-email@yorku.ca">Email</a> |
      <a href="https://example.com">Website</a>
    </div>

    <p>
      Spencer studies attitudes toward work, cultural change, social values, and temporal analysis.
    </p>
  </div>
</div>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Sophie Li">

  <div class="person-info">
    <div class="person-name">Sophie Li</div>
    <div class="person-role">PhD Student, Social-Personality Psychology</div>

    <div class="person-links">
      <a href="mailto:student-email@yorku.ca">Email</a> |
      <a href="https://example.com">Website</a>
    </div>

    <p>
      Sophie studies conflict resolution, political apologies, and natural language processing.
    </p>
  </div>
</div>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Adrian Torres">

  <div class="person-info">
    <div class="person-name">Adrian Torres</div>
    <div class="person-role">PhD Student, Clinical-Developmental Psychology</div>

    <div class="person-links">
      <a href="mailto:student-email@yorku.ca">Email</a> |
      <a href="https://example.com">Website</a>
    </div>

    <p>
      Adrian studies performance, voice, and confidence.
    </p>
  </div>
</div>

</section>

<section class="people-grid-section">

<h2>Current Undergraduate Researchers</h2>

<div class="people-grid three">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Tatijanna Martel">
    <div class="grid-person-name">Tatijanna Martel</div>
    <div class="grid-person-role">Undergraduate Researcher</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Researcher</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Researcher</div>
  </div>

</div>

</section>

<section class="people-grid-section">

<h2>Graduate Lab Alumni</h2>

<div class="people-grid three">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Emily Drisdelle">
    <div class="grid-person-name">Emily Drisdelle</div>
    <div class="grid-person-role">MA Alumna</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Memoona Arshad">
    <div class="grid-person-name">Memoona Arshad</div>
    <div class="grid-person-role">Graduate Alumna</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Graduate Alum</div>
  </div>

</div>

</section>

<section class="people-grid-section">

<h2>Undergraduate Lab Alumni</h2>

<div class="people-grid five">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/cheng-profile.jpg' | relative_url }}" alt="Student Name">
    <div class="grid-person-name">Student Name</div>
    <div class="grid-person-role">Undergraduate Alum</div>
  </div>

</div>

</section>

</div>



### Current Lab Members

- **Miranda Too** (PhD Student, Social-Personality Psychology)<br>
  humility, prestige, reputation

- **Spencer Arshinoff** (PhD Student, Social-Personality Psychology)<br>
  attitudes towards work, cultural change, social values, temporal analysis

- **Sophie Li** (PhD Student, Social-Personality Psychology)<br>
  conflict resolution, political apologies, natural language processing

- **Adrian Torres** (PhD Student, Clinical-Developmental Psychology)<br>
  performance, voice, confidence

- **Tatijanna Martel** (Undergraduate, Independent Research Project)<br>
  social connection, loneliness, cross-national similarities and differences

### Lab Alumni

- **Emily Drisdelle** (MA in Social-Personality Psychology, York University)<br>
  gender disparities in voice and leadership

- **Memoona Arshad** (MA in Social-Personality Psychology, York University)<br>
  socio-economic status, barriers to influence

- **Randi Vogt** (MA in Social-Personality Psychology, University of Illinois at Urbana-Champaign)<br>
  overconfidence, persistence

- **Fan Xuan Chen** (MA in Social-Personality Psychology, University of Illinois at Urbana-Champaign)<br>
  dominance, punishment, leadership

- **Shoko Watanabe** (PhD in Social-Personality Psychology, University of Illinois at Urbana-Champaign)<br>
  trust, reputation, reciprocity

- **Daniel Redhead** (PhD in Psychology, University of Essex)<br>
  social networks, dominance, prestige
