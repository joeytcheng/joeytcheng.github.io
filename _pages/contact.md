---
layout: page
permalink: /contact/
title: Contact
description: Get in touch!
nav: true
nav_order: 5
---


<style>
.contact-page {
  max-width: 900px;
  margin: 0 auto;
}

.contact-intro {
  font-size: 1rem;
  line-height: 1.7;
  margin-bottom: 3rem;
}

.faq-section {
  margin-top: 3rem;
}

.faq-title {
  font-size: 2rem;
  color: var(--global-theme-color);
  margin-bottom: 1.25rem;
}

.faq-item {
  border-top: 1px solid var(--global-divider-color);
  padding: 1rem 0;
}

.faq-item:last-child {
  border-bottom: 1px solid var(--global-divider-color);
}

.faq-question {
  cursor: pointer;
  font-weight: 700;
  font-size: 1.05rem;
  list-style: none;
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.faq-question::-webkit-details-marker {
  display: none;
}

.faq-question::before {
  content: "⌄";
  color: var(--global-theme-color);
  font-size: 1.25rem;
  transform: rotate(-90deg);
  transition: transform 0.2s ease;
}

.faq-item[open] .faq-question::before {
  transform: rotate(0deg);
}

.faq-answer {
  margin-top: 0.75rem;
  margin-left: 2rem;
  font-size: 0.95rem;
  line-height: 1.7;
}

.faq-answer p {
  margin-bottom: 0.75rem;
}

.faq-answer a {
  text-decoration: underline;
}

@media (max-width: 600px) {
  .faq-title {
    font-size: 1.7rem;
  }

  .faq-question {
    font-size: 1rem;
  }

  .faq-answer {
    margin-left: 1.75rem;
  }
}
</style>

<div class="contact-page">

<div class="contact-intro">

<p>
  For research-related inquiries, prospective student questions, media requests, or other matters, please contact me by email.
</p>

<p>
  Email: <a href="mailto:your-email@yorku.ca">your-email@yorku.ca</a>
</p>

</div>

<section class="faq-section">

<h2 class="faq-title">Frequently Asked Questions</h2>

<details class="faq-item">
  <summary class="faq-question">Are you accepting graduate students?</summary>
  <div class="faq-answer">
    <p>
      I review applications from students whose interests fit closely with the Human Connection Lab’s research areas, including leadership, status, gender disparities in groups, loneliness, social isolation, culture, and computational approaches to social behavior.
    </p>
  </div>
</details>

<details class="faq-item">
  <summary class="faq-question">What kinds of research projects do students work on?</summary>
  <div class="faq-answer">
    <p>
      Students in the lab work on projects related to leadership, social influence, prestige and dominance, gender disparities in groups, loneliness, social isolation, and cultural narratives about social connection.
    </p>
  </div>
</details>

<details class="faq-item">
  <summary class="faq-question">Can undergraduate students join the lab?</summary>
  <div class="faq-answer">
    <p>
      Yes. Undergraduate students may become involved through independent research projects, thesis projects, volunteer research assistant positions, or other research opportunities when available.
    </p>
  </div>
</details>

<details class="faq-item">
  <summary class="faq-question">What should I include when contacting you about research opportunities?</summary>
  <div class="faq-answer">
    <p>
      Please briefly describe your research interests, relevant experience, and why the Human Connection Lab seems like a good fit. It is also helpful to include a CV or resume and, for prospective graduate students, a short description of possible research questions you would like to pursue.
    </p>
  </div>
</details>

<details class="faq-item">
  <summary class="faq-question">Do I need prior experience with statistics or programming?</summary>
  <div class="faq-answer">
    <p>
      Prior experience is helpful but not always required. Many projects involve quantitative methods, experiments, survey research, or computational tools, so students should be interested in developing those skills over time.
    </p>
  </div>
</details>

<details class="faq-item">
  <summary class="faq-question">Where is the lab located?</summary>
  <div class="faq-answer">
    <p>
      The Human Connection Lab is based in the Department of Psychology at York University in Toronto, Ontario.
    </p>
  </div>
</details>

<details class="faq-item">
  <summary class="faq-question">Who should contact you for media or speaking inquiries?</summary>
  <div class="faq-answer">
    <p>
      Please contact me by email with a brief description of the request, the topic, the timeline, and any relevant details about the audience or outlet.
    </p>
  </div>
</details>

</section>

</div>

