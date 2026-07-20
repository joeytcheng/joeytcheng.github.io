---
layout: page
permalink: /contact/
title: Contact
description: Get in touch!
nav: true
nav_order: 6
---

<div class="contact-page">

  <p class="contact-eyebrow">Human Connection Lab</p>

  <h1 class="contact-title">Contact</h1>
  <div class="title-rule"></div>

  <p class="contact-intro">
    We're always happy to hear from prospective students, collaborators, and press — please get in touch.
  </p>

  <div class="contact-grid">

    <section class="contact-item">
      <p class="contact-label">EMAIL</p>

      <h2 class="contact-item-title">
        <a href="mailto:chengjt@yorku.ca">
          <span class="link-underline-text">chengjt@yorku.ca</span> <i class="fas fa-envelope" aria-hidden="true"></i>
        </a>
      </h2>

      <p class="contact-description">
        Best for questions about research, collaboration, or other
        academic matters.
      </p>

      <p class="contact-link">
        <a href="#">
          <span class="link-underline-text">York faculty website</span> ↗
        </a>
        <br>
        <a
          href="https://www.yorku.ca/health/psychology/"
          target="_blank"
          rel="noopener noreferrer"
          style="display: inline-block; margin-top: 0.5rem;">
          <span class="link-underline-text">Department website</span> ↗
        </a>
      </p>
    </section>

    <section class="contact-item">
      <p class="contact-label">MEDIA AND SPEAKING</p>

      <h2 class="contact-item-title">Interviews and Events</h2>

      <p class="contact-description">
        For media interviews, research commentary, invited talks, or other
        requests, please email me with the topic, format, and
        proposed timeline.
      </p>

      <p class="contact-link">
        <a href="mailto:chengjt@yorku.ca?subject=Media%20or%20Speaking%20Inquiry">
          <span class="link-underline-text">Send an inquiry</span> ↗
        </a>
      </p>
    </section>

    <section class="contact-item">
      <p class="contact-label">ACTIVELY RECRUITING</p>

      <h2 class="contact-item-title">Join the Lab</h2>

      <p class="contact-description">
        Interested in graduate study, postdoctoral positions, visiting
        scholar opportunities, or undergraduate research in the lab?
        Please reach out—we are hiring!
      </p>

      <p class="contact-link">
        <a href="{{ '/join-us/' | relative_url }}">
          <span class="link-underline-text">See the Join us page</span> ↗
        </a>
        <br>
        <a
          href="https://docs.google.com/forms/d/e/1FAIpQLScqWzKCojb5APpJ9pIF8_Rl01LVSMZ_BwrwAF5tNjEqCnhYcg/viewform?usp=header"
          target="_blank"
          rel="noopener noreferrer"
          style="display: inline-block; margin-top: 0.5rem;">
          <span class="link-underline-text">Submit undergrad lab application</span> ↗
        </a>
      </p>
    </section>

    <section class="contact-item contact-item-location">
      <p class="contact-label">VISIT THE LAB</p>

      <h2 class="contact-item-title">Human Connection Lab</h2>

      <p class="contact-description">
        Lab Director: Joey Cheng
        <a href="mailto:chengjt@yorku.ca" aria-label="Email Joey T. Cheng">
          <i class="fas fa-envelope"></i>
        </a>
        <br>
        Department of Psychology<br>
        Behavioural Sciences Building (BSB)<br>
        4700 Keele Street<br>
        Toronto, Ontario<br>
        Canada&nbsp;&nbsp;M3J 1P3
      </p>

      <div class="contact-location-map">
        <iframe
          src="https://www.google.com/maps?q=Behavioural+Sciences+Building+York+University+4700+Keele+Street+Toronto+ON+M3J+1P3&output=embed"
          width="100%"
          height="100%"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          title="Map showing the Human Connection Lab location at York University">
        </iframe>
      </div>
    </section>

  </div>

</div>

<style>
  /*
   * Suppress the theme's own auto-rendered page title/
   * description above the white card — replaced by a matching
   * eyebrow + title block inside the card, the same treatment
   * used across the rest of the site.
   */

  .post-header {
    display: none;
  }

  .contact-page {
    width: 100%;
    max-width: 1100px;
    margin: 2rem auto;
    background: var(--global-card-bg-color);
    border-radius: 16px;
    padding: 2.5rem 3rem;
    box-sizing: border-box;
  }

  @media (max-width: 700px) {
    .contact-page {
      padding: 1.75rem;
    }
  }

  .contact-eyebrow {
    margin: 0 0 0.5rem;
    color: var(--global-theme-color);
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.15em;
    text-transform: uppercase;
  }

  .contact-title {
    font-family: Georgia, 'Times New Roman', serif;
    font-size: 2.4rem;
    line-height: 1.1;
    margin: 0 0 1.25rem;
    font-weight: 700;
  }

  .contact-intro {
    max-width: 760px;
    margin: 0 0 3.5rem;
    font-size: 1.02rem;
    line-height: 1.7;
    color: var(--global-text-color-light);
  }

  .contact-intro a {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .contact-intro a:hover {
    text-decoration: underline;
    text-underline-offset: 0.2rem;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    column-gap: 5rem;
    row-gap: 4.5rem;
  }

  .contact-item {
    min-width: 0;
  }

  .contact-label {
    margin: 0 0 1.15rem;
    color: var(--global-text-color-light);
    font-family: monospace;
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .contact-item-title {
    margin: 0 0 0.6rem;
    font-size: 1.15rem;
    font-weight: 600;
    line-height: 1.4;
  }

  .contact-item-title a {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .contact-item-title a .link-underline-text {
    text-decoration: underline;
    text-underline-offset: 0.15rem;
    color: var(--global-theme-color);
  }

  .contact-description {
    max-width: 510px;
    margin: 0;
    color: var(--global-text-color-light);
    line-height: 1.65;
  }

  .contact-link {
    margin: 1.1rem 0 0;
  }

  .contact-description a {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .contact-link a {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .link-underline-text {
    text-decoration: underline;
    text-underline-offset: 0.2rem;
    color: var(--global-theme-color);
  }

  .contact-item-location .contact-description {
    line-height: 1.6;
  }

  .contact-item-location .contact-description a {
    color: var(--global-theme-color);
    margin-left: 0.3rem;
    text-decoration: none;
  }

  .contact-location-map {
    width: 100%;
    aspect-ratio: 16 / 9;
    border-radius: 8px;
    overflow: hidden;
    border: 1px solid var(--global-divider-color);
    margin-top: 0.9rem;
  }

  .contact-location-map iframe {
    width: 100%;
    height: 100%;
    display: block;
  }

  @media (max-width: 768px) {
    .contact-intro {
      margin-bottom: 2.75rem;
    }

    .contact-grid {
      grid-template-columns: 1fr;
      row-gap: 3rem;
    }
  }

  @media (max-width: 576px) {
    .contact-item-title {
      font-size: 1.08rem;
    }
  }
</style>
