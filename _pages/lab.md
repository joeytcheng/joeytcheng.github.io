---
layout: page
permalink: /lab/
title: The Team
description: Meet the team.
nav: true
nav_order: 4
---

<style>
/*
 * Suppress the theme's own auto-rendered page title/
 * description above the white card — this page already has
 * its own kicker + title inside the card, so showing both
 * duplicated "The Team" in two different type styles.
 */

.post-header {
  display: none;
}

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
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.75rem;
  font-weight: 500;
  color: var(--global-theme-color);
  margin-bottom: 0.5rem;
}

.people-title {
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 2.4rem;
  line-height: 1.1;
  font-weight: 700;
  margin-bottom: 1.5rem;
}

.people-banner {
  background: var(--global-theme-color);
  color: #ffffff;
  text-align: center;
  padding: 0.75rem;
  margin-bottom: 2rem;
  font-size: 0.95rem;
}

.people-banner-pill {
  display: inline-block;
  background: rgba(255, 255, 255, 0.15);
  color: #ffffff !important;
  font-size: 0.68rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 0.2rem 0.65rem;
  border-radius: 999px;
  margin-right: 0.6rem;
  vertical-align: middle;
}

.people-banner a {
  color: #ffffff;
  text-decoration: none;
}

.people-banner-link-text {
  text-decoration: underline;
  color: #ffffff !important;
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
<div class="title-rule"></div>

<div class="people-banner">
  <span class="people-banner-pill">Now hiring</span>
  <a href="{{ '/join-us/' | relative_url }}"><span class="people-banner-link-text">Join us</span> ↗</a>
</div>

<section class="people-section">

<h2>Lab Director</h2>

<div class="person">
  <img class="person-photo" src="{{ '/assets/img/profile-cheng.jpg' | relative_url }}" alt="Joey T. Cheng">

  <div class="person-info">

    <div class="person-name-line">
      <div class="person-name">Joey T. Cheng</div>

      <div class="person-icons-inline">
        <a href="mailto:chengjt@yorku.ca" aria-label="Email">
          <i class="fas fa-envelope"></i>
        </a>

        <a href="https://scholar.google.com/citations?user=lweBpmIAAAAJ&hl=en" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar">
          <i class="ai ai-google-scholar"></i>
        </a>

        <a href="https://github.com/joeytcheng" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
          <i class="fab fa-github"></i>
        </a>

        <a href="https://osf.io/gvqfm/" target="_blank" rel="noopener noreferrer" aria-label="OSF">
          <i class="ai ai-osf"></i>
        </a>

        <a href="https://www.linkedin.com/in/joeytcheng/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
          <i class="fab fa-linkedin"></i>
        </a>
      </div>
    </div>

    <div class="person-role">Lab Director</div>

    <p>
      Joey is a behavioral scientist and social psychologist studying how people navigate social connection — both the connections we seek out, and the more complicated ones shaped by power and status. Her work spans two threads: the confidence, voice, dominance, prestige, and egalitarian preferences that shape who is heard, respected, and trusted to lead; and, more recently, how and why loneliness and social disconnection vary across people, places, and cultures.
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
      Miranda studies humility, prestige, and reputation — asking how modest, other-focused behavior shapes the way people are seen and valued within their groups. She's interested in when humility earns genuine respect and prestige, and when it goes unnoticed or gets taken advantage of. Her work approaches the lab's broader question of what makes someone worth following from a different angle than confidence or dominance.
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
      Spencer studies how attitudes toward work have shifted alongside broader cultural change, using large-scale text and survey data to trace evolving social values over time. His work traces how narratives about ambition, career, and time itself change across decades, and what that reveals about shifting priorities. This connects to the lab's interest in how the stories a culture tells shape everyday behavior and belonging.
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
      Sophie studies conflict resolution and political apologies, using natural language processing to analyze how leaders and institutions communicate accountability after wrongdoing. Her work asks what makes an apology land as sincere rather than hollow, and how language choices shape whether trust can be repaired. This ties into the lab's broader interest in how the stories we tell shape social repair and connection.
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
      Adrian studies how knowledge of true ability — our own and others' — shapes who earns status in a group. He finds that revealing relative performance strengthens the link between ability and how much someone speaks, which in turn boosts peer-perceived prestige; when performance stays hidden, that link disappears. The work asks whether making competence visible can produce a more meritocratic distribution of status, rewarding real ability rather than just confidence or volume.
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
    <div class="grid-person-name">
      <a href="https://www.linkedin.com/in/emilydrisdelle/" target="_blank" rel="noopener noreferrer">
        Emily Drisdelle
      </a>
    </div>
    <div class="grid-person-topic">Researcher &amp; Analyst</div>
  </div>

<div class="grid-person">
  <img class="grid-person-photo" src="{{ '/assets/img/profile-arshad.jpg' | relative_url }}" alt="Memoona Arshad">
  <div class="grid-person-name">
    <a href="https://www.linkedin.com/in/memoona-arshad-017630238/" target="_blank" rel="noopener noreferrer">
      Memoona Arshad
    </a>
  </div>
  <div class="grid-person-topic">Program Evaluation Lead<br>Jack.org</div>
</div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-vogt.jpg' | relative_url }}" alt="Randi Vogt">
    <div class="grid-person-name">
      <a href="https://www.geisinger.edu/gchs/research/about-gchs-research/find-an-investigator/2023/03/03/14/01/randi-vogt" target="_blank" rel="noopener noreferrer">
        Randi Vogt
      </a>
    </div>
    <div class="grid-person-topic">Postdoctoral Fellow<br>Geisinger Research Institute</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-chenfx.jpg' | relative_url }}" alt="Fan Xuan Chen">
    <div class="grid-person-name">
      <a href="https://scholar.google.com/citations?user=Lr3gBXQAAAAJ&hl=en" target="_blank" rel="noopener noreferrer">
        Fan Xuan Chen
      </a>
    </div>
    <div class="grid-person-topic">AI Model Evaluation Lead<br>Turing.com</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-watanabe.jpg' | relative_url }}" alt="Shoko Watanabe">
    <div class="grid-person-name">
      <a href="https://www.sed.tohoku.ac.jp/laboratory/detail---id-80.html" target="_blank" rel="noopener noreferrer">
        Shoko Watanabe
      </a>
    </div>
    <div class="grid-person-topic">Specially Appointed Assistant Professor<br>Tohoku University, Japan</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-wuyuejun.jpg' | relative_url }}" alt="Yue Jun Wu">
    <div class="grid-person-name">Yue Jun Wu</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-liamy.jpg' | relative_url }}" alt="Amy Li">
    <div class="grid-person-name">Amy Li</div>
  </div>

</div>


</section>

<section class="people-grid-section">

<h2>Former Visiting Researchers</h2>

<div class="people-grid three">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-leckelt.jpg' | relative_url }}" alt="Marius Leckelt">
    <div class="grid-person-name">
      <a href="https://www.linkedin.com/in/mariusleckelt/" target="_blank" rel="noopener noreferrer">
        Marius Leckelt
      </a>
    </div>
    <div class="grid-person-topic">Data Scientist &amp; Machine Learning Engineer<br>Bain &amp; Company, Switzerland</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-redhead.jpg' | relative_url }}" alt="Daniel Redhead">
    <div class="grid-person-name">
      <a href="https://www.rug.nl/staff/d.j.redhead/" target="_blank" rel="noopener noreferrer">
        Daniel Redhead
      </a>
    </div>
    <div class="grid-person-topic">Assistant Professor<br>University of Groningen, Netherlands</div>
  </div>
  
</div>

</section>

<section class="people-grid-section">

<h2>Undergraduate Lab Alumni (selected)</h2>

<div class="people-grid five">

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-aiyub.jpg' | relative_url }}" alt="Aliya Aiyub">
    <div class="grid-person-name">
      <a href="https://www.psychologytoday.com/ca/therapists/simcoe-county-psychotherapy-alliston-on/1796066" target="_blank" rel="noopener noreferrer">
        Aliya Aiyub
      </a>
    </div>
    <div class="grid-person-topic">Psychotherapist</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-ikram.jpg' | relative_url }}" alt="Yumna Ikram">
    <div class="grid-person-name">Yumna Ikram</div>
    <div class="grid-person-topic">Registered Social Worker</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-padala.jpg' | relative_url }}" alt="Akhila Padala">
    <div class="grid-person-name">Akhila Padala</div>
    <div class="grid-person-topic">Master of Social Work Student</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-wangmilton.jpg' | relative_url }}" alt="Milton Wang">
    <div class="grid-person-name">
      <a href="https://www.linkedin.com/in/milton-wang-767188124/" target="_blank" rel="noopener noreferrer">
        Milton Wang
      </a>
    </div>
    <div class="grid-person-topic">HR Specialist<br>U.S. Department of Veterans Affairs</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-helm.jpg' | relative_url }}" alt="Eric Helm">
    <div class="grid-person-name">
      <a href="https://www.linkedin.com/in/eric-helm-844562125/" target="_blank" rel="noopener noreferrer">
        Eric Helm
      </a>
    </div>
    <div class="grid-person-topic">Data Scientist<br>Google</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-clifford.jpg' | relative_url }}" alt="Florence Clifford">
    <div class="grid-person-name">
      <a href="https://www.linkedin.com/in/florence-clifford/" target="_blank" rel="noopener noreferrer">
        Florence Clifford
      </a>
    </div>
    <div class="grid-person-topic">Business Systems and Insights Lead<br>Watson Board Advisors</div>
  </div>

  <div class="grid-person">
    <img class="grid-person-photo" src="{{ '/assets/img/profile-zhangyiwei.jpg' | relative_url }}" alt="Yiwei Zhang">
    <div class="grid-person-name">
      <a href="https://www.linkedin.com/in/yiwei-zhang-2701687a/" target="_blank" rel="noopener noreferrer">
        Yiwei Zhang
      </a>
    </div>
    <div class="grid-person-topic">Data Scientist<br>McKinsey &amp; Company</div>
  </div>

</div>

</section>

</div>