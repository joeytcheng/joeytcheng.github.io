---
layout: page
title:
permalink: /
nav: false
---

<style>
.landing-page {
  max-width: 1350px;
  margin: 0 auto;
}

.landing-hero {
  background: var(--global-card-bg-color);
  border-radius: 12px;
  padding: 2.5rem;
  display: grid;
  grid-template-columns: 2.6fr 1fr;
  gap: 2rem;
  align-items: center;
  margin: 2.5rem 0 3rem;
}

.landing-illustration svg {
  width: 100%;
  height: auto;
  max-width: 750px;
}

.landing-headline {
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 2rem;
  line-height: 1.3;
  font-weight: 700;
  color: var(--global-text-color);
  margin-bottom: 1rem;
}

.landing-intro {
  font-size: 1rem;
  line-height: 1.7;
  margin-bottom: 1.25rem;
}

.landing-readmore {
  display: inline-block;
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  color: var(--global-theme-color);
  text-decoration: none;
}

.landing-readmore:hover {
  text-decoration: underline;
}

.ln {
  stroke-dasharray: 300;
  stroke-dashoffset: 300;
  animation: landing-draw 0.6s ease-out forwards;
}

.nd {
  opacity: 0;
  transform-origin: center;
  transform-box: fill-box;
  animation: landing-pop 0.5s ease-out forwards;
}

.dash {
  animation: landing-fadein 0.8s ease-out forwards;
}

@keyframes landing-draw {
  to { stroke-dashoffset: 0; }
}

@keyframes landing-pop {
  0% { opacity: 0; transform: scale(0.3); }
  100% { opacity: 1; transform: scale(1); }
}

@keyframes landing-fadein {
  to { opacity: 0.5; }
}

@media (max-width: 800px) {
  .landing-hero {
    grid-template-columns: 1fr;
    padding: 2rem;
  }

  .landing-headline {
    font-size: 1.6rem;
  }
}
</style>

<div class="landing-page">

<section class="landing-hero">

  <div class="landing-illustration">
    <svg viewBox="0 0 300 300" role="img" aria-label="Illustration of a network of connected people">
      <g fill="none" stroke="var(--global-theme-color)" stroke-width="1.5" stroke-linecap="round">
        <line class="ln" style="animation-delay:.1s" x1="150" y1="90" x2="90" y2="140" />
        <line class="ln" style="animation-delay:.1s" x1="150" y1="90" x2="210" y2="140" />
        <line class="ln" style="animation-delay:.5s" x1="90" y1="140" x2="60" y2="200" />
        <line class="ln" style="animation-delay:.5s" x1="90" y1="140" x2="130" y2="200" />
        <line class="ln" style="animation-delay:.5s" x1="210" y1="140" x2="170" y2="200" />
        <line class="ln" style="animation-delay:.5s" x1="210" y1="140" x2="240" y2="200" />
        <line class="ln" style="animation-delay:.9s" x1="130" y1="200" x2="170" y2="200" />
        <line class="ln" style="animation-delay:.9s" x1="60" y1="200" x2="95" y2="250" />
        <line class="ln" style="animation-delay:.9s" x1="130" y1="200" x2="95" y2="250" />
        <line class="ln" style="animation-delay:.9s" x1="130" y1="200" x2="150" y2="260" />
        <line class="ln" style="animation-delay:.9s" x1="170" y1="200" x2="150" y2="260" />
        <line class="ln" style="animation-delay:.9s" x1="170" y1="200" x2="205" y2="250" />
        <line class="ln" style="animation-delay:.9s" x1="240" y1="200" x2="205" y2="250" />
        <line class="dash" style="animation-delay:1.5s" x1="90" y1="140" x2="210" y2="140" stroke-dasharray="2 5" opacity="0" />
        <line class="dash" style="animation-delay:1.6s" x1="60" y1="200" x2="240" y2="200" stroke-dasharray="2 5" opacity="0" />
        <line class="dash" style="animation-delay:1.7s" x1="95" y1="250" x2="205" y2="250" stroke-dasharray="2 5" opacity="0" />
        <path class="dash" style="animation-delay:1.8s" d="M40,270 C90,290 210,290 260,270" stroke-width="1" stroke-dasharray="1 5" opacity="0" />

        <circle class="nd" style="animation-delay:0s" cx="150" cy="90" r="16" />
        <circle class="nd" style="animation-delay:.4s" cx="90" cy="140" r="14" />
        <circle class="nd" style="animation-delay:.4s" cx="210" cy="140" r="14" />
        <circle class="nd" style="animation-delay:.8s" cx="60" cy="200" r="12" />
        <circle class="nd" style="animation-delay:.8s" cx="130" cy="200" r="13" />
        <circle class="nd" style="animation-delay:.8s" cx="170" cy="200" r="13" />
        <circle class="nd" style="animation-delay:.8s" cx="240" cy="200" r="12" />
        <circle class="nd" style="animation-delay:1.2s" cx="95" cy="250" r="10" />
        <circle class="nd" style="animation-delay:1.2s" cx="150" cy="260" r="11" />
        <circle class="nd" style="animation-delay:1.2s" cx="205" cy="250" r="10" />
      </g>
    </svg>
  </div>

  <div>
    <h1 class="landing-headline">What creates human connections, and what breaks them apart?</h1>

    <p class="landing-intro">
      At the <strong>Human Connection Lab</strong>, we study the tension between our need for connection and the modern conditions — busy institutions, shifting cultural narratives, digital life — that make forming connections harder.
    </p>

    <a class="landing-readmore" href="{{ '/research/' | relative_url }}">More on our research &rarr;</a>
  </div>

</section>

</div>
