---
layout: page
title:
permalink: /
nav: false
---

<style>
/*
 * The page title is intentionally blank on this page, so the
 * theme's auto-rendered header wrapper should already be empty
 * — hidden defensively anyway, for consistency with the rest
 * of the site and in case it renders any residual spacing.
 */

.post-header {
  display: none;
}

.landing-page {
  max-width: 1350px;
  margin: 0 auto;
}

.landing-hero {
  padding: 4rem 1rem 5rem;
  display: grid;
  grid-template-columns: 2.6fr 1fr;
  gap: 3rem;
  align-items: center;
  margin: 1rem 0 2rem;
}

.landing-illustration svg {
  width: 100%;
  height: auto;
  max-width: 750px;
}

.landing-headline {
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 2.6rem;
  line-height: 1.25;
  font-weight: 700;
  color: var(--global-text-color);
  margin-bottom: 1.1rem;
}

.landing-headline-accent {
  color: var(--global-theme-color);
}

.landing-intro {
  font-size: 1rem;
  line-height: 1.6;
  color: var(--global-text-color-light);
  margin-bottom: 1.75rem;
}

.landing-readmore-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.landing-readmore {
  display: inline-block;
  font-size: 0.85rem;
  font-weight: 400;
  letter-spacing: 0.06em;
  color: var(--global-theme-color);
  text-decoration: none;
}

.landing-readmore .link-underline-text {
  text-decoration: underline;
  color: var(--global-theme-color);
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

.landing-text-reveal {
  opacity: 0;
  animation: landing-text-in 0.9s ease-out forwards;
  animation-delay: 2.6s;
}

@keyframes landing-text-in {
  from {
    opacity: 0;
    transform: translateY(14px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 800px) {
  .landing-hero {
    grid-template-columns: 1fr;
    padding: 2rem;
  }

  .landing-headline {
    font-size: 2rem;
  }
}
</style>

<div class="landing-page">

<section class="landing-hero">

  <div class="landing-illustration">
    <svg viewBox="20 65 260 240" role="img" aria-label="Illustration of a network of connected people">
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

  <div class="landing-text-reveal">
    <h1 class="landing-headline">What creates <span class="landing-headline-accent">human connections</span>, and what breaks them apart?</h1>

    <p class="landing-intro">
      At the <strong>Human Connection Lab</strong>, we study the tension between our need for connection and the modern conditions — busy institutions, shifting cultural narratives, digital life — that make forming connections harder.
    </p>

    <div class="landing-readmore-group">
      <a class="landing-readmore" href="{{ '/research/' | relative_url }}"><span class="link-underline-text">Our research</span> ↗</a>
      <a class="landing-readmore" href="{{ '/bio/' | relative_url }}"><span class="link-underline-text">Lab director Joey&nbsp;Cheng</span> ↗</a>
    </div>
  </div>

</section>

</div>
