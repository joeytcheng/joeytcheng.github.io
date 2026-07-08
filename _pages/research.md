---
layout: page
title: Research
permalink: /research/
description: Research themes in the Human Connection Lab.
nav: true
nav_order: 2
---

<style>
.research-page {
  max-width: 1050px;
  margin: 0 auto;
}

.research-kicker {
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.75rem;
  color: var(--global-theme-color);
  margin-bottom: 0.5rem;
}

.research-title {
  font-size: 2.8rem;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  font-weight: 500;
}

.research-intro {
  max-width: 760px;
  font-size: 1.02rem;
  line-height: 1.8;
  margin-bottom: 3rem;
}

.research-intro a {
  text-decoration: underline;
}

.theme-list {
  border-top: 1px solid var(--global-divider-color);
  margin-bottom: 3.5rem;
}

.theme-card {
  display: grid;
  grid-template-columns: 135px 55px 1fr;
  gap: 1.5rem;
  align-items: center;
  padding: 1.6rem 1.2rem;
  border-bottom: 1px solid var(--global-divider-color);
  background: var(--global-card-bg-color);
}

.theme-visual {
  width: 115px;
  height: 115px;
  border: 1.5px solid var(--global-theme-color);
  border-radius: 20px;
  color: var(--global-theme-color);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.25rem;
  justify-self: start;
}

.theme-visual.circle {
  border-radius: 50%;
}

.theme-visual.soft {
  border-radius: 35px;
}

.theme-visual.no-border {
  border: none;
  font-size: 3rem;
}

.theme-number {
  color: var(--global-theme-color);
  font-size: 0.8rem;
  letter-spacing: 0.08em;
  align-self: start;
  padding-top: 0.4rem;
}

.theme-text h2 {
  font-size: 1.45rem;
  margin-bottom: 0.75rem;
  font-weight: 500;
}

.theme-text p {
  line-height: 1.7;
  margin-bottom: 0;
}

.feature-section {
  display: grid;
  grid-template-columns: 220px 1fr;
  gap: 3rem;
  align-items: center;
  padding: 3rem 0;
  border-top: 1px solid var(--global-divider-color);
}

.feature-section.reverse {
  grid-template-columns: 1fr 220px;
}

.feature-text h2 {
  font-size: 1.55rem;
  color: var(--global-theme-color);
  margin-bottom: 1rem;
  font-weight: 500;
}

.feature-text p {
  line-height: 1.8;
  margin-bottom: 0;
}

.feature-visual {
  width: 180px;
  height: 180px;
  border: 2px solid var(--global-theme-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--global-theme-color);
  font-size: 3rem;
  margin: 0 auto;
}

.feature-visual.square {
  border-radius: 18px;
}

.feature-visual.no-border {
  border: none;
  font-size: 4rem;
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

.research-links a:hover {
  text-decoration: underline;
}

@media (max-width: 850px) {
  .research-title {
    font-size: 2.2rem;
  }

  .theme-card {
    grid-template-columns: 95px 45px 1fr;
    gap: 1rem;
  }

  .theme-visual {
    width: 85px;
    height: 85px;
    font-size: 1.9rem;
  }

  .feature-section,
  .feature-section.reverse {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .feature-section.reverse .feature-visual {
    order: -1;
  }

  .feature-visual {
    width: 150px;
    height: 150px;
    font-size: 2.5rem;
  }
}

@media (max-width: 600px) {
  .theme-card {
    grid-template-columns: 1fr;
    gap: 0.75rem;
  }

  .theme-number {
    padding-top: 0;
  }

  .theme-visual {
    width: 100px;
    height: 100px;
  }
}
</style>

<div class="research-page">

<div class="research-kicker">Human Connection Lab</div>

<h1 class="research-title">Research</h1>

<div class="research-intro">
  <p>
    In the Human Connection Lab, we study how people connect, compete, lead, withdraw, and find their place in social life. Our work brings together social psychology, personality psychology, organizational psychology, cultural psychology, and computational methods to understand how people navigate groups and relationships.
  </p>

  <p>
    Across projects, we ask how social environments shape who is heard, who gains influence, who feels connected, and who becomes socially isolated. We use experiments, surveys, behavioral data, cross-cultural datasets, and natural language processing to study these questions.
  </p>
</div>

<div class="theme-list">

  <div class="theme-card">
    <div class="theme-visual circle">
      <i class="fas fa-users"></i>
    </div>

    <div class="theme-number">01</div>

    <div class="theme-text">
      <h2>Leadership, Status, and Social Influence</h2>
      <p>
        How do people gain influence in groups? One line of research examines how leadership emerges through confidence, voice, dominance, prestige, and reputation. We study why some people are more likely to be heard and selected as leaders, and how different paths to influence shape group functioning.
      </p>
    </div>
  </div>

  <div class="theme-card">
    <div class="theme-visual soft">
      <i class="fas fa-comments"></i>
    </div>

    <div class="theme-number">02</div>

    <div class="theme-text">
      <h2>Gender Disparities in Groups</h2>
      <p>
        Why do men and women sometimes experience group life differently? This work examines gender disparities in confidence, speaking time, recognition, and leadership emergence. We are especially interested in how group interaction patterns can amplify or reduce inequalities in voice and influence.
      </p>
    </div>
  </div>

  <div class="theme-card">
    <div class="theme-visual">
      <i class="fas fa-map-location-dot"></i>
    </div>

    <div class="theme-number">03</div>

    <div class="theme-text">
      <h2>Loneliness and Social Isolation</h2>
      <p>
        Why are people becoming more socially disconnected, and who is most at risk? This research examines loneliness and social isolation across individuals, communities, and cultures. We study how social disconnection varies geographically and how changing social norms may shape the value people place on connection.
      </p>
    </div>
  </div>

  <div class="theme-card">
    <div class="theme-visual no-border">
      <i class="fas fa-network-wired"></i>
    </div>

    <div class="theme-number">04</div>

    <div class="theme-text">
      <h2>Culture, Narratives, and Social Connection</h2>
      <p>
        How do cultural narratives shape social life? This line of work studies how people talk about independence, self-protection, withdrawal, connection, and belonging. Using natural language processing and large-scale text data, we examine how cultural messages may encourage or discourage social connection.
      </p>
    </div>
  </div>

</div>

<section class="feature-section">
  <div class="feature-visual no-border">
    <i class="fas fa-users"></i>
  </div>

  <div class="feature-text">
    <h2>Understanding how people navigate groups</h2>
    <p>
      Much of our work begins with the small-group settings where people speak, listen, compete, cooperate, and form impressions of one another. We study how these everyday behaviors shape broader outcomes, including leadership, influence, recognition, and belonging.
    </p>
  </div>
</section>

<section class="feature-section reverse">
  <div class="feature-text">
    <h2>Studying loneliness as both personal and social</h2>
    <p>
      Loneliness is often experienced as a private feeling, but it is also shaped by social structures, cultural expectations, and the environments people live in. Our research examines loneliness and isolation as outcomes of both individual experiences and broader social conditions.
    </p>
  </div>

  <div class="feature-visual square">
    <i class="fas fa-map-location-dot"></i>
  </div>
</section>

<section class="feature-section">
  <div class="feature-visual">
    <i class="fas fa-comments"></i>
  </div>

  <div class="feature-text">
    <h2>Using language to understand cultural change</h2>
    <p>
      Social life is shaped not only by what people do, but also by the stories they tell about what is healthy, admirable, risky, or worthwhile. We use computational approaches to study narratives about social connection, independence, isolation, and self-protection.
    </p>
  </div>
</section>

<section class="feature-section reverse">
  <div class="feature-text">
    <h2>Building a lab around human connection</h2>
    <p>
      The Human Connection Lab brings together students and collaborators interested in leadership, gender, social status, loneliness, culture, and computational social science. Across these areas, our broader goal is to understand the social forces that bring people together or pull them apart.
    </p>
  </div>

  <div class="feature-visual no-border">
    <i class="fas fa-network-wired"></i>
  </div>
</section>

<div class="research-links">
  <a href="{{ '/publications/' | relative_url }}">Full publication list →</a>
  <a href="{{ '/lab/' | relative_url }}">Meet the lab →</a>
  <a href="{{ '/contact/' | relative_url }}">Contact us →</a>
</div>

</div>



# The Human Connection Lab

Research on leadership, belonging, and the social psychology of human connection.

Directed by Joey T. Cheng at York University, the lab studies how people connect, lead, and belong in groups, organizations, and society.

Our work examines leadership, social influence, teamwork, prestige, loneliness, social isolation, and the cultural forces shaping modern social life.



## Research

### 01 Leadership & Influence
How people earn respect, gain influence, and shape group life.

### 02 Belonging & Loneliness
Why people feel connected, isolated, included, or unseen.

### 03 Teams & Collaboration
How groups coordinate, share voice, and work together effectively.

### 04 Culture & Modern Social Life
How cultural norms shape connection, independence, status, and well-being.