---
layout: page
title: Research
permalink: /research/
#description: Research themes in the Human Connection Lab.
nav: true
nav_order: 2
---

<style>
/*
 * Suppress the theme's own auto-rendered page title/
 * description above the white card — this page already has
 * its own kicker + title inside the card, so showing both
 * duplicated "Research" in two different type styles.
 */

.post-header {
  display: none;
}

.research-page {
  max-width: 1050px;
  margin: 2rem auto;
  background: var(--global-card-bg-color);
  border-radius: 16px;
  padding: 2.5rem 3rem;
}

@media (max-width: 700px) {
  .research-page {
    padding: 1.75rem;
  }
}

.research-kicker {
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.75rem;
  font-weight: 500;
  color: var(--global-theme-color);
  margin-bottom: 0.5rem;
}

.research-title {
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 2.4rem;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  font-weight: 700;
}

.research-intro {
  max-width: 760px;
  font-size: 1.02rem;
  line-height: 1.7;
  color: var(--global-text-color-light);
  margin-bottom: 3rem;
}

.research-intro a {
  text-decoration: underline;
}

.feature-section {
  display: grid;
  grid-template-columns: 320px 1fr;
  gap: 3rem;
  align-items: center;
  padding: 3rem 0;
  border-top: 1px solid var(--global-divider-color);
}

.feature-section.reverse {
  grid-template-columns: 1fr 320px;
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
  width: 100%;
  max-width: 320px;
  aspect-ratio: 3 / 2;
  border-radius: 14px;
  overflow: hidden;
  margin: 0 auto;
  background: #ffffff;
}

.feature-visual img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
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

@media (max-width: 850px) {
  .feature-section,
  .feature-section.reverse {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .feature-section.reverse .feature-visual {
    order: -1;
  }

  .feature-visual {
    max-width: 300px;
  }
}

/*
 * DARK-MODE-ONLY FIX
 * .feature-visual's background below is a hardcoded white,
 * chosen as a frame for illustrations in light mode. Light mode
 * is untouched; this rule only applies under
 * html[data-theme="dark"], swapping in the theme's dark card
 * color so the frame doesn't stay a bright white box.
 */

html[data-theme="dark"] .feature-visual {
  background: var(--global-card-bg-color);
}
</style>

<div class="research-page">

<div class="research-kicker">Human Connection Lab</div>

<h1 class="research-title">Research</h1>
<div class="title-rule"></div>

<div class="research-intro">
  <p>
    In the Human Connection Lab, we study how people connect and belong, and how they come to trust one another. We ask questions like who gets recognized, why societies have become increasingly lonely, and what stories we tell about connection.
  </p>

  <p>
    We study these questions using tools ranging from behavioral experiments and archival "big data" analysis, to computational text analysis.
  </p>
</div>

<section class="feature-section">
  <div class="feature-visual">
    <img src="{{ '/assets/img/img-theme-loneliness-white.jpg' | relative_url }}" alt="A lonely figure sitting alone on a small island in the rain">
  </div>

  <div class="feature-text">
    <h2>Why are so many of us feeling more disconnected?</h2>
    <p>
      We use "big data" archival analysis, behavioral data, and text analysis to investigate why loneliness is on the rise. This research examines loneliness and social isolation across individuals, communities, and cultures, asking who is most at risk and why. We study how social disconnection varies geographically, and how changing social norms and everyday conditions may shape the value people place on connection.
    </p>
  </div>
</section>

<section class="feature-section reverse">
  <div class="feature-text">
    <h2>How do the stories we tell shape whether we feel connected?</h2>
    <p>
      We study how cultural narratives about independence, self-protection, and belonging shape social life, and how social life reciprocally reflects shifting cultural values. This line of work looks at how people talk about withdrawal, connection, and belonging, using natural language processing and large-scale text data to trace how cultural messages may encourage or discourage social connection over time.
    </p>
  </div>

  <div class="feature-visual">
    <img src="{{ '/assets/img/img-theme-cultural-narrative-white.jpg' | relative_url }}" alt="An open book with speech bubbles, a heart, and a globe, representing stories and cultural connection">
  </div>
</section>

<section class="feature-section">
  <div class="feature-visual">
    <img src="{{ '/assets/img/img-theme-gender-disparities-white.jpg' | relative_url }}" alt="A balance scale weighing male and female symbols, with a raised hand and a speech bubble">
  </div>

  <div class="feature-text">
    <h2>Why do some voices get heard more than others, and how does gender play into it?</h2>
    <p>
      We study why certain people are more likely to be recognized, included, and heard in groups, and what that means for equity. This work also examines gender disparities in confidence, speaking time, recognition, and leadership emergence, asking why men and women sometimes experience group life differently and how everyday group interactions can amplify or reduce inequalities in voice and influence.
    </p>
  </div>
</section>

<section class="feature-section reverse">
  <div class="feature-text">
    <h2>What makes someone worth following?</h2>
    <p>
      We study the everyday behaviors, confidence, voice, and fairness, that shape who earns influence and trust. One line of research examines how leadership emerges through confidence, voice, dominance, prestige, and reputation, asking why some people are more likely to be heard and selected as leaders, and how different paths to influence shape how well a group functions.
    </p>
  </div>

  <div class="feature-visual">
    <img src="{{ '/assets/img/img-theme-hierarchy-egalitarian-white.jpg' | relative_url }}" alt="Chess king and pawn pieces beside a podium with a microphone and a rising bar chart">
  </div>
</section>

<div class="research-links">
  <a href="{{ '/publications/' | relative_url }}"><span class="link-underline-text">Full publication list</span> ↗</a>
  <a href="{{ '/lab/' | relative_url }}"><span class="link-underline-text">Meet the lab</span> ↗</a>
  <a href="{{ '/join-us/' | relative_url }}"><span class="link-underline-text">Join us</span> ↗</a>
  <a href="{{ '/contact/' | relative_url }}"><span class="link-underline-text">Contact us</span> ↗</a>
</div>

</div>
