---
layout: page
permalink: /publications/
title: Publications
description: Articles and book chapters by year of publication
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<style>
  /* =========================================================
     PUBLICATIONS PAGE
     ========================================================= */

  /*
   * Suppress the theme's own auto-rendered page title/
   * description above the white card — replaced by a matching
   * kicker + title + description block inside the card, the
   * same treatment used on Research and The Team.
   */

  .post-header {
    display: none;
  }

  .publications-page {
    max-width: 900px;
    margin: 2rem auto;
    background: var(--global-card-bg-color);
    border-radius: 16px;
    padding: 2.5rem 3rem;
  }

  @media (max-width: 700px) {
    .publications-page {
      padding: 1.75rem;
    }
  }

  .publications-kicker {
    text-transform: uppercase;
    letter-spacing: 0.15em;
    font-size: 0.75rem;
    font-weight: 500;
    color: var(--global-theme-color);
    margin-bottom: 0.5rem;
  }

  .publications-title {
    font-family: Georgia, 'Times New Roman', serif;
    font-size: 2.4rem;
    line-height: 1.1;
    margin-bottom: 1.5rem;
    font-weight: 700;
  }

  .publications-description {
    max-width: 700px;
    font-size: 1.02rem;
    line-height: 1.7;
    color: var(--global-text-color-light);
    margin-bottom: 1.75rem;
  }

  .publications {
    margin-top: 1.5rem;
  }

  /* =========================================================
     TOOLBAR (SEARCH + TOPIC FILTER, TOP OF PAGE)
     ========================================================= */

  .publications-toolbar {
    margin-bottom: 1.75rem;
  }

  .publications-toolbar #pub-search-wrapper {
    position: relative;
    margin-bottom: 1rem;
    max-width: 320px;
    margin-left: auto;
  }

  .pub-search-icon {
    position: absolute;
    left: 0.75rem;
    top: 50%;
    transform: translateY(-50%);
    color: var(--global-text-color-light);
    font-size: 0.8rem;
    pointer-events: none;
  }

  .publications-toolbar #pub-search-wrapper input {
    width: 100%;
    box-sizing: border-box;
    padding: 0.55rem 0.75rem 0.55rem 2rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 8px;
    background: var(--global-card-bg-color);
    color: var(--global-text-color);
    font-size: 0.85rem;
  }

  .topic-filter-label {
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--global-text-color-light);
    margin-bottom: 0.6rem;
  }

  .topic-filter-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .topic-filter-item {
    display: inline-block;
    margin: 0;
    padding: 0.4rem 0.85rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 999px;
    background: transparent;
    color: var(--global-text-color);
    font-size: 0.82rem;
    line-height: 1.3;
    cursor: pointer;
  }

  .topic-filter-item:hover {
    border-color: var(--global-theme-color);
    color: var(--global-theme-color);
  }

  .topic-filter-item.active {
    background: var(--global-theme-color);
    border-color: var(--global-theme-color);
    color: #ffffff;
    font-weight: 600;
  }

  .topic-filter-item.active:hover {
    color: #ffffff;
  }

  /*
   * Hide al-folio's year headings.
   * JavaScript copies each year above the corresponding titles.
   */

  .publications h2.bibliography {
    display: none !important;
  }

  /* Remove default bibliography numbering */

  .publications ol.bibliography {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  /* Individual publication entry */

  .publications ol.bibliography > li {
    position: relative;
    display: grid;
    grid-template-columns: 64px minmax(0, 1fr);
    column-gap: 1.25rem;
    align-items: start;
    margin: 0;
    padding: 1.7rem 0 2rem;
    border-bottom: 1px solid var(--global-divider-color);
  }

  /*
   * Grid items default to min-width: auto, which lets long
   * unwrapped content (e.g. a raw BibTeX line) force the
   * column wider than the page. min-width: 0 lets it wrap
   * and stay contained instead.
   */

  .pub-content-col {
    min-width: 0;
  }

  @media (max-width: 480px) {
    .publications ol.bibliography > li {
      display: block;
    }
  }

  .publications ol.bibliography > li:first-child {
    padding-top: 0.5rem;
  }

  .publications ol.bibliography > li .row {
    margin: 0;
  }

  /*
   * Hide the abbreviation and preview columns.
   */

  .publications .abbr,
  .publications .preview {
    display: none !important;
  }

  /*
   * Allow publication content to use the full page width.
   */

  .publications .row > div,
  .publications .col-sm-8,
  .publications .col-sm-9,
  .publications .col-sm-10,
  .publications .col-sm-11,
  .publications .col-md-8,
  .publications .col-md-9,
  .publications .col-md-10,
  .publications .col-md-11 {
    width: 100%;
    max-width: 100%;
    flex: 0 0 100%;
    padding-right: 0;
    padding-left: 0;
  }

  /* =========================================================
     YEAR ABOVE THE TITLE
     ========================================================= */

  .publication-year-above-title {
    display: block;
    margin: 0;
    padding-top: 0.15rem;
    color: var(--global-text-color-light);
    font-size: 1rem;
    font-weight: 400;
    font-style: italic;
    line-height: 1.25;
  }

  @media (max-width: 480px) {
    .publication-year-above-title {
      margin-bottom: 0.3rem;
    }
  }

  /*
   * Hide any other year elements generated inside an entry.
   */

  .publications .year,
  .publications .year-label,
  .publications .year-badge,
  .publications .publication-year {
    display: none !important;
  }

  /*
   * Do not hide the new year placed above the title.
   */

  .publications .publication-year-above-title {
    display: block !important;
  }

  /* =========================================================
     PUBLICATION TITLE
     ========================================================= */

  .publications .title {
    margin: 0 0 0.45rem;
    color: var(--global-theme-color);
    font-size: 1.2rem;
    font-weight: 500;
    line-height: 1.45;
  }

  /* =========================================================
     AUTHORS
     ========================================================= */

  /*
   * Author names use the same light color as the journal line.
   */

  .publications .author {
    margin: 0 0 0.2rem;
    color: var(--global-text-color-light);
    font-size: 1rem;
    line-height: 1.55;
  }

  .publications .author a,
  .publications .author span,
  .publications .author em,
  .publications .author strong {
    color: var(--global-text-color-light);
  }

  /*
   * Keep your highlighted name slightly heavier while
   * retaining the same light color.
   */

  .publications .author em,
  .publications .author strong {
    font-weight: 600;
  }

  /*
   * Reveal any author elements hidden by al-folio.
   */

  .publications .author .more-authors,
  .publications .author .more-authors.hidden,
  .publications .author span.hidden,
  .publications .author .hidden-authors,
  .publications .author .hidden-authors.hidden,
  .publications .author [data-more-authors] {
    display: inline !important;
    visibility: visible !important;
    opacity: 1 !important;
  }

  /*
   * Hide author-expansion controls because all authors
   * should be visible immediately.
   */

  .publications .author .more-authors-click,
  .publications .author .more-authors-button,
  .publications .author button,
  .publications .author [role="button"],
  .publications .author a.more-authors {
    display: none !important;
  }

  /* =========================================================
     JOURNAL, BOOK, VOLUME, ISSUE, AND PAGES
     ========================================================= */

  /*
   * The publication year is removed from this line by the
   * JavaScript below.
   */

  .publications .periodical {
    margin: 0 0 0.8rem;
    color: var(--global-text-color-light);
    font-size: 1rem;
    line-height: 1.5;
  }

  .publications .periodical em,
  .publications .periodical a,
  .publications .periodical span {
    color: var(--global-text-color-light);
  }

  /*
   * Hide a year if al-folio puts it in a dedicated element
   * within the journal line.
   */

  .publications .periodical .year,
  .publications .periodical .publication-year {
    display: none !important;
  }

  /*
   * Publication type badge (e.g. Journal article, Book
   * chapter, Edited book) appended after the paper title.
   */

  .pub-type-badge {
    display: inline-block;
    margin-left: 0.55rem;
    padding: 0.15rem 0.5rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 4px;
    color: var(--global-text-color-light);
    font-size: 0.66rem;
    font-style: normal;
    font-weight: 600;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    vertical-align: middle;
  }

  /* =========================================================
     HIGHLIGHTS BOX (toggled by the "Highlights" button)
     ========================================================= */

  .publications div.abstract,
  .publications .publication-overview {
    box-sizing: border-box;
    width: 100%;
    max-width: 100%;
    margin: 0.85rem 0;
    overflow: hidden;

    background: #F3E9EE;
    border-radius: 8px;

    color: var(--global-text-color-light);

    font-family: inherit;
    font-size: 0.82rem;
    font-weight: 400;
    line-height: 1.5;
  }

  .pub-highlights-header {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 0.6rem 1rem;
    border-bottom: 1px solid rgba(107, 58, 93, 0.15);
  }

  .pub-highlights-header i {
    font-size: 0.68rem;
    color: var(--global-theme-color);
  }

  .pub-highlights-header span {
    color: var(--global-theme-color);
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 0.07em;
    text-transform: uppercase;
  }

  .pub-highlights-list {
    list-style: none;
    margin: 0;
    padding: 0.9rem 1rem;
  }

  .pub-highlights-list li {
    position: relative;
    padding-left: 1.15rem;
    margin-bottom: 0.05rem;
    line-height: 1.25;
    color: inherit;
  }

  .pub-highlights-list li:last-child {
    margin-bottom: 0;
  }

  .pub-highlights-list li::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0.6em;
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #C79FB2;
  }

  /*
   * The first bullet is the rhetorical hook rather than a
   * finding, so it is set apart with bold weight rather than
   * italics — emphasis through weight rather than a second
   * hue, so it doesn't compete with the plum accent already
   * used for the header and bullet markers.
   */

  .pub-highlights-hook {
    font-weight: 600;
  }

  /* =========================================================
     PUBLICATION BUTTONS
     ========================================================= */

  .publications .links {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 1rem;
    margin-top: 0.75rem;
  }

  /*
   * One-off extra links (see EXTRA_LINKS in the script below),
   * e.g. a second supplemental document that doesn't fit the
   * standard PDF/Supplement/URL/Site button row.
   */

  .publications .pub-extra-links {
    margin: 0.35rem 0 0;
    font-size: 0.82rem;
    color: var(--global-text-color-light);
  }

  .publications .pub-extra-links a {
    color: var(--global-theme-color);
    text-decoration: underline;
    text-underline-offset: 0.15rem;
  }

  /*
   * PDF, URL, and Site links render as plain icon-plus-label
   * links (no button box), matching a minimal citation-list
   * style.
   */

  .publications .links a.btn,
  .publications .links button.btn {
    display: inline-flex !important;
    align-items: center;
    gap: 0.4rem;

    width: auto !important;
    min-height: 0 !important;
    margin: 0 !important;
    padding: 0 !important;

    border: none !important;
    border-radius: 0 !important;
    background: transparent !important;
    box-shadow: none !important;

    color: var(--icon-muted-color) !important;
    font-family: inherit !important;
    font-size: 0.85rem !important;
    font-weight: 500 !important;
    line-height: 1.3 !important;
    text-transform: none !important;

    cursor: pointer;

    transition: color 0.2s ease;
  }

  .publications .links a.btn:hover,
  .publications .links a.btn:focus,
  .publications .links button.btn:hover,
  .publications .links button.btn:focus {
    color: var(--global-theme-color) !important;
    background: transparent !important;
    border: none !important;
    text-decoration: underline;
    outline: none;
  }

  .publications .links a.btn i,
  .publications .links button.btn i {
    font-size: 0.82rem;
  }

  /*
   * Chevron indicator on the dropdown-toggle buttons
   * (Highlights, Cite APA, Cite BibTeX), drawn with borders
   * rather than a font glyph so it renders identically across
   * browsers. Rotates in place to point up when open, rather
   * than swapping to a different character.
   */

  .pub-highlights-toggle-icon {
    display: inline-block;
    width: 6px;
    height: 6px;
    margin-left: 0.25rem;
    border-right: 2px solid currentColor;
    border-bottom: 2px solid currentColor;
    transform: rotate(45deg);
    transition: transform 0.2s ease;
  }

  .pub-highlights-toggle-icon.is-open {
    transform: rotate(225deg);
  }

  /*
   * Force the icon and label text to always match the
   * button's own color, overriding any leftover color rule
   * the theme applies to a specific child element.
   */

  .publications .links a.btn *,
  .publications .links button.btn * {
    color: inherit !important;
  }


  /* =========================================================
     CITE: APA BOX AND BIBTEX BOX
     ========================================================= */

  .pub-cite-box {
    box-sizing: border-box;
    width: 100%;
    max-width: 100%;
    margin-top: 0.85rem;
    overflow: hidden;

    background: #F3E9EE;
    border-radius: 8px;

    color: var(--global-text-color);
    font-size: 0.82rem;
    line-height: 1.65;
  }

  /*
   * Header row: label on the left, Copy button on the right,
   * both in normal document flow. This replaces an earlier
   * absolutely-positioned Copy button, which could overlap
   * long unbroken citation text (e.g. a DOI URL) on some
   * entries.
   */

  .pub-cite-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 0.75rem;
    padding: 0.55rem 0.9rem;
    border-bottom: 1px solid rgba(107, 58, 93, 0.15);
  }

  .pub-cite-label-group {
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .pub-cite-label-group i {
    font-size: 0.68rem;
    color: var(--global-theme-color);
  }

  .pub-cite-label {
    color: var(--global-theme-color);
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 0.07em;
    text-transform: uppercase;
  }

  .pub-cite-body {
    padding: 0.75rem 0.9rem;
  }

  /*
   * The BibTeX body now holds plain text (its original
   * <pre>/<code> syntax highlighting is stripped out in JS),
   * so it only needs wrapping rules here — no font-family
   * override, and no padding/background/border reset, both of
   * which were previously applied to .pub-cite-body itself
   * instead of only its old nested <pre>/<code> children. That
   * mistake was overriding the shared .pub-cite-body padding
   * above and forcing a monospace font, which is why the
   * BibTeX box looked cramped and used a different font than
   * the APA and Highlights boxes.
   */

  .pub-cite-bibtex .pub-cite-body {
    white-space: pre-wrap;
    word-break: break-word;
    overflow-wrap: anywhere;
    max-width: 100%;
  }

  .pub-cite-apa .pub-cite-text {
    font-family: inherit;
    overflow-wrap: anywhere;
    word-break: break-word;
  }

  .pub-cite-copy {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    flex-shrink: 0;

    padding: 0.25rem 0.65rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 5px;

    background: var(--global-card-bg-color);
    color: var(--global-text-color-light);
    font-family: var(--global-font-family, inherit);
    font-size: 0.72rem;
    font-weight: 500;

    cursor: pointer;
    transition: border-color 0.2s ease, color 0.2s ease;
  }

  .pub-cite-copy i {
    font-size: 0.7rem;
  }

  .pub-cite-copy:hover,
  .pub-cite-copy:focus {
    border-color: var(--global-theme-color);
    color: var(--global-theme-color);
    outline: none;
  }

  /* =========================================================
     READING LIST
     ========================================================= */

  .reading-list-section {
    margin-top: 3.5rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--global-divider-color);
  }

  .reading-list-section h2 {
    margin-bottom: 1rem;
    font-size: 1.45rem;
    font-weight: 500;
  }

  /* =========================================================
     MOBILE
     ========================================================= */

  @media (max-width: 576px) {
    .publications ol.bibliography > li {
      padding: 1.4rem 0 1.6rem;
    }

    .publication-year-above-title {
      margin-bottom: 0.3rem;
      font-size: 0.95rem;
    }

    .publications .title {
      font-size: 1.08rem;
    }

    .publications .author,
    .publications .periodical {
      font-size: 0.95rem;
    }

    .publications div.abstract,
    .publications .publication-overview {
      margin-top: 0.85rem;
      font-size: 0.8rem;
      line-height: 1.45;
    }

    .pub-highlights-list {
      padding: 0.8rem 0.9rem;
    }
  }

  /*
   * DARK-MODE-ONLY FIX
   * The Highlights box background below is a hardcoded light
   * pink, chosen for light mode. Its text already switches to a
   * light color in dark mode via var(--global-text-color-light),
   * which would be unreadable against that same light pink — so
   * this box needs a dark-mode-specific background. Light mode
   * is untouched; this rule only applies under
   * html[data-theme="dark"].
   */

  html[data-theme="dark"] .publications div.abstract,
  html[data-theme="dark"] .publications .publication-overview {
    background: #3A2732;
  }

  /*
   * DARK-MODE-ONLY FIX
   * .pub-cite-box (the Cite APA / Cite BibTeX dropdowns) has a
   * hardcoded light-pink background below, chosen for light
   * mode. Its text uses var(--global-text-color), which already
   * switches to a light color in dark mode — unreadable against
   * that same light-pink background. Light mode is untouched;
   * this rule only applies under html[data-theme="dark"].
   */

  html[data-theme="dark"] .pub-cite-box {
    background: #3A2732;
  }

  /* =========================================================
     CLOSING LINKS BAR
     ========================================================= */

  .publications-links {
    margin-top: 1.5rem;
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    align-items: center;
    font-size: 0.9rem;
  }

  .publications-links a {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .publications-links .link-underline-text {
    text-decoration: underline;
    text-underline-offset: 0.2rem;
    color: var(--global-theme-color);
  }

  .publications-links .back-to-top {
    margin-left: auto;
  }
</style>

<div class="publications-page" id="top">

<div class="publications-kicker">Human Connection Lab</div>

<h1 class="publications-title">Publications</h1>
<div class="title-rule"></div>

<div class="publications-toolbar">

  <!-- Bibliography search feature (custom, client-side) -->

  <div class="pub-search-box" id="pub-search-wrapper">
    <i class="fas fa-magnifying-glass pub-search-icon" aria-hidden="true"></i>
    <input
      type="text"
      id="pub-search-input"
      placeholder="Search publications..."
      aria-label="Search publications" />
  </div>

  <div class="topic-filter-label">Filter by topic</div>

  <div class="topic-filter-row" id="topic-filter-box">
    <button type="button" class="topic-filter-item active" data-topic="all">All topics</button>
    <button type="button" class="topic-filter-item" data-topic="culture">Culture &amp; norms</button>
    <button type="button" class="topic-filter-item" data-topic="status-hierarchy">Hierarchy &amp; egalitarianism</button>
    <button type="button" class="topic-filter-item" data-topic="dominance-prestige">Status &amp; respect</button>
    <button type="button" class="topic-filter-item" data-topic="gender">Gender disparities</button>
    <button type="button" class="topic-filter-item" data-topic="leadership">Leadership &amp; collaboration</button>
    <button type="button" class="topic-filter-item" data-topic="personality">Personality &amp; individual differences</button>
    <button type="button" class="topic-filter-item" data-topic="pride-emotion">Emotion &amp; identity</button>
    <button type="button" class="topic-filter-item" data-topic="social-connection">Social connection</button>
    <button type="button" class="topic-filter-item" data-topic="well-being">Well-being</button>
  </div>

</div>

<div class="publications">

{% bibliography %}

</div>

<div class="publications-links">
  <a href="{{ '/research/' | relative_url }}"><span class="link-underline-text">Research overview</span> ↗</a>
  <a href="{{ '/bio/' | relative_url }}"><span class="link-underline-text">Lab director bio</span> ↗</a>
  <a href="{{ '/lab/' | relative_url }}"><span class="link-underline-text">Meet the lab</span> ↗</a>
  <a href="{{ '/contact/' | relative_url }}"><span class="link-underline-text">Contact us</span> ↗</a>
  <a href="#top" class="back-to-top"><span class="link-underline-text">Back to top</span> ↑</a>
</div>

</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const publicationsContainer =
      document.querySelector(".publications");

    if (!publicationsContainer) {
      return;
    }

    /* =======================================================
       PLACE THE YEAR ABOVE EACH PUBLICATION TITLE
       =======================================================
       Walk every year heading and publication entry in a
       single document-order pass, rather than matching each
       heading to its following <ol> via nextElementSibling.
       The sibling-walk approach silently skipped restructuring
       for any group whose markup didn't exactly match a plain
       "<h2><ol>" pair (e.g. a non-numeric year grouping such
       as "in press"), which left that entry's original
       children to fall directly into the raw two-column CSS
       grid unwrapped — squeezing the title into the narrow
       64px year column. querySelectorAll always returns nodes
       in document order regardless of selector order, so this
       single pass tracks "the most recent year heading seen so
       far" and applies it to every entry that follows,
       independent of how the headings and lists are nested.
       ======================================================= */

    const yearHeadingsAndEntries =
      publicationsContainer.querySelectorAll(
        "h2.bibliography, ol.bibliography > li"
      );

    let currentYearText = "";

    yearHeadingsAndEntries.forEach(function (node) {
      /*
       * A single malformed or unexpectedly-structured entry
       * should not be able to throw and silently abort this
       * loop for every entry that follows it. Catch per-node
       * so one bad entry just stays unrestructured instead of
       * breaking the whole page.
       */

      try {
        processYearHeadingOrEntry(node);
      } catch (error) {
        console.error(
          "Publications: failed to place year for an entry",
          node,
          error
        );
      }
    });

    function processYearHeadingOrEntry(node) {
      if (node.matches("h2.bibliography")) {
        const headingText = node.textContent.trim();

        /*
         * Most headings are a plain four-digit year. Some
         * entries (e.g. "in press") have a non-numeric year
         * value instead — use the heading text as-is in that
         * case so it still appears above the title.
         */

        const yearMatch =
          headingText.match(/\b(?:19|20)\d{2}\b/);

        currentYearText =
          yearMatch
            ? yearMatch[0]
            : headingText
              ? headingText.charAt(0).toUpperCase() +
                headingText.slice(1)
              : "";

        return;
      }

      const publication = node;

      /*
       * Avoid restructuring the same entry more than once.
       */

      if (
        publication.querySelector(
          ".publication-year-above-title"
        )
      ) {
        return;
      }

      const title =
        publication.querySelector(".title");

      if (!title) {
        return;
      }

      /*
       * Move all of the entry's existing content into a
       * wrapper column, then place the year as a sibling
       * column to its left (grid-template-columns on the
       * <li> handles the two-column layout).
       */

      const contentColumn =
        document.createElement("div");

      contentColumn.className = "pub-content-col";

      while (publication.firstChild) {
        contentColumn.appendChild(
          publication.firstChild
        );
      }

      const yearElement =
        document.createElement("div");

      yearElement.className =
        "publication-year-above-title";

      yearElement.textContent = currentYearText;

      publication.appendChild(yearElement);
      publication.appendChild(contentColumn);
    }

    const publicationItems =
      publicationsContainer.querySelectorAll(
        "ol.bibliography > li"
      );

    /*
     * jekyll-scholar puts the citation key on an inner element
     * (the "Entry bib key" div), not on the <li> itself — the
     * <li> has no id of its own. TOPIC_MAP and PUB_TYPE_MAP are
     * keyed by citation key, so every lookup needs to go through
     * this helper rather than reading publication.id directly.
     */

    function getPublicationKey(publication) {
      const keyElement = publication.querySelector("[id]");
      return keyElement ? keyElement.id : "";
    }

    /* =======================================================
       HIGHLIGHTS HELPER
       =======================================================
       Bib entries may separate bullet points with " || " (see
       the header comment in papers.bib). When that delimiter
       isn't present, fall back to splitting the existing prose
       on sentence boundaries, so every entry still renders as
       a bulleted list even before its overview is hand-edited
       into the " || "-delimited format.
       ======================================================= */

    function splitIntoHighlightBullets(text) {
      const trimmedText = text.trim();

      const delimitedParts = trimmedText
        .split(/\s*\|\|\s*/)
        .map(function (part) {
          return part.trim();
        })
        .filter(function (part) {
          return part.length > 0;
        });

      if (delimitedParts.length > 1) {
        return delimitedParts;
      }

      const sentenceMatches = trimmedText.match(
        /[^.!?]+[.!?]+(?:\s+|$)/g
      );

      if (sentenceMatches && sentenceMatches.length > 1) {
        return sentenceMatches.map(function (sentence) {
          return sentence.trim();
        });
      }

      return [trimmedText];
    }

    /* =======================================================
       CITE HELPERS
       ======================================================= */

    function escapeHtml(text) {
      return text
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;");
    }

    /*
     * al_folio_core's own bib.liquid layout never renders
     * volume, number (issue), or pages anywhere on the page —
     * its ".periodical" div is built only from the journal/
     * booktitle name plus month/year (confirmed against the
     * gem's _layouts/bib.liquid source). Those fields DO still
     * exist in papers.bib and DO appear in the raw BibTeX block
     * (entry.bibtex dumps every field verbatim), so this reads
     * them back out of that hidden block's raw text — the only
     * place on the page they still survive — to reconstruct a
     * proper "Volume(Issue), pages" segment for both the visible
     * journal line and the Cite APA box.
     */

    function extractBibField(rawBibtexText, fieldName) {
      const pattern = new RegExp(
        "^\\s*" + fieldName + "\\s*=\\s*\\{([^}]*)\\}",
        "im"
      );

      const match = rawBibtexText.match(pattern);

      return match ? match[1].trim() : null;
    }

    function formatPageRange(pages) {
      return pages.replace(/\s*--\s*/g, "–");
    }

    function buildVolumeIssuePages(volume, number, pages, asHtml) {
      let segment = "";

      if (volume) {
        segment +=
          ", " +
          (asHtml
            ? "<em>" + escapeHtml(volume) + "</em>"
            : volume);

        if (number) {
          segment +=
            "(" +
            (asHtml ? escapeHtml(number) : number) +
            ")";
        }
      }

      if (pages) {
        const formattedPages = formatPageRange(pages);

        segment +=
          ", " +
          (asHtml
            ? escapeHtml(formattedPages)
            : formattedPages);
      }

      return segment;
    }

    function buildApaCitation(
      publication,
      doiHref,
      volume,
      number,
      pages
    ) {
      const titleEl =
        publication.querySelector(".title");

      const authorEl =
        publication.querySelector(".author");

      const periodicalEl =
        publication.querySelector(".periodical");

      const yearEl = publication.querySelector(
        ".publication-year-above-title"
      );

      if (
        !titleEl ||
        !authorEl ||
        !periodicalEl ||
        !yearEl
      ) {
        return null;
      }

      const authorsText = authorEl.textContent
        .trim()
        .replace(/\s+/g, " ");

      const titleText = titleEl.textContent
        .trim()
        .replace(/\s+/g, " ");

      const yearText = yearEl.textContent.trim();

      /*
       * Plain-text version (for clipboard copy): identical to
       * before, built from periodicalEl's textContent.
       */

      const periodicalText = periodicalEl.textContent
        .trim()
        .replace(/\s+/g, " ")
        .replace(/[.,;]+$/, "");

      /*
       * HTML version (for on-screen display): built from
       * periodicalEl's innerHTML instead of textContent, so the
       * <em> tag the theme already wraps around the journal/
       * book title (see ".periodical em" above) survives into
       * the citation box, giving APA-correct italics instead of
       * flattening everything to plain text.
       */

      const periodicalHTML = periodicalEl.innerHTML
        .trim()
        .replace(/\s+/g, " ")
        .replace(/[.,;]+\s*$/, "");

      const volIssuePagesText = buildVolumeIssuePages(
        volume,
        number,
        pages,
        false
      );

      const volIssuePagesHTML = buildVolumeIssuePages(
        volume,
        number,
        pages,
        true
      );

      const citationText =
        authorsText +
        " (" +
        yearText +
        "). " +
        titleText +
        ". " +
        periodicalText +
        volIssuePagesText +
        "." +
        (doiHref ? " " + doiHref : "");

      const citationHTML =
        escapeHtml(authorsText) +
        " (" +
        escapeHtml(yearText) +
        "). " +
        escapeHtml(titleText) +
        ". " +
        periodicalHTML +
        volIssuePagesHTML +
        "." +
        (doiHref
          ? " " + escapeHtml(doiHref)
          : "");

      return {
        text: citationText,
        html: citationHTML
      };
    }

    /* =======================================================
       DROPDOWN COORDINATION
       =======================================================
       Highlights, Cite APA, and Cite BibTeX each toggle their
       own box, but only one should be open per entry at a
       time — otherwise they stack on top of each other. Each
       button's click handler closes every registered dropdown
       for that entry, then opens its own box only if it wasn't
       already the one showing (so opening a different dropdown
       never requires first closing whichever one is open).
       ======================================================= */

    function closeDropdownEntry(entry) {
      entry.box.classList.remove("hidden");

      entry.box.style.setProperty(
        "display",
        "none",
        "important"
      );

      const toggleIcon = entry.button.querySelector(
        ".pub-highlights-toggle-icon"
      );

      if (toggleIcon) {
        toggleIcon.classList.remove("is-open");
      }
    }

    function openDropdownEntry(entry) {
      entry.box.classList.remove("hidden");

      entry.box.style.setProperty(
        "display",
        "block",
        "important"
      );

      const toggleIcon = entry.button.querySelector(
        ".pub-highlights-toggle-icon"
      );

      if (toggleIcon) {
        toggleIcon.classList.add("is-open");
      }
    }

    function sanitizeClonedTrigger(button) {
      /*
       * Cloning a native toggle button (cloneNode) copies its
       * HTML attributes, including any framework "hook"
       * attributes (e.g. Bootstrap's data-toggle/data-target,
       * or an href used for collapse behavior). Those hooks
       * are read by a document-level delegated listener, so
       * even though cloning strips element-specific JS
       * listeners, the clone can still trigger the theme's own
       * native toggle behavior on click, in addition to our
       * own handler. Stripping every data-, aria-, href, and
       * onclick attribute removes those hooks so only our own
       * click handler runs.
       */

      const attributesToRemove = [];

      Array.prototype.forEach.call(
        button.attributes,
        function (attr) {
          const name = attr.name;

          if (
            name === "href" ||
            name === "onclick" ||
            name.indexOf("data-") === 0 ||
            name.indexOf("aria-") === 0
          ) {
            attributesToRemove.push(name);
          }
        }
      );

      attributesToRemove.forEach(function (name) {
        button.removeAttribute(name);
      });

      if (!button.hasAttribute("tabindex")) {
        button.setAttribute("tabindex", "0");
      }

      if (!button.hasAttribute("role")) {
        button.setAttribute("role", "button");
      }
    }

    function flashCopied(buttonEl) {
      /*
       * Copy buttons now contain an icon plus a label span.
       * Swap only the label text so the icon is not wiped out.
       */

      const labelEl = buttonEl.querySelector("span");
      const targetEl = labelEl || buttonEl;

      const originalLabel = targetEl.textContent;

      targetEl.textContent = "Copied";

      setTimeout(function () {
        targetEl.textContent = originalLabel;
      }, 1500);
    }

    function copyPublicationText(text, buttonEl, html) {
      /*
       * navigator.clipboard.writeText() only ever puts plain
       * text on the clipboard, so a pasted APA citation always
       * lost its italics even though the on-screen box showed
       * them correctly — copying by hand (select + Ctrl/Cmd-C)
       * worked because that's a native browser copy, which
       * carries the rendered HTML along with it. When an HTML
       * version is supplied, write both a text/plain and a
       * text/html clipboard entry via the Clipboard API so a
       * paste into Word/Docs/Gmail etc. keeps the italics, while
       * a paste into a plain-text field still just gets text.
       */

      if (
        html &&
        navigator.clipboard &&
        navigator.clipboard.write &&
        typeof ClipboardItem !== "undefined"
      ) {
        const item = new ClipboardItem({
          "text/plain": new Blob(
            [text],
            { type: "text/plain" }
          ),
          "text/html": new Blob(
            [html],
            { type: "text/html" }
          )
        });

        navigator.clipboard
          .write([item])
          .then(function () {
            flashCopied(buttonEl);
          })
          .catch(function () {
            copyPlainText(text, buttonEl);
          });

        return;
      }

      copyPlainText(text, buttonEl);
    }

    function copyPlainText(text, buttonEl) {
      if (
        navigator.clipboard &&
        navigator.clipboard.writeText
      ) {
        navigator.clipboard
          .writeText(text)
          .then(function () {
            flashCopied(buttonEl);
          })
          .catch(function () {
            fallbackCopyText(text, buttonEl);
          });

        return;
      }

      fallbackCopyText(text, buttonEl);
    }

    function fallbackCopyText(text, buttonEl) {
      const textarea =
        document.createElement("textarea");

      textarea.value = text;
      textarea.style.position = "fixed";
      textarea.style.opacity = "0";

      document.body.appendChild(textarea);
      textarea.focus();
      textarea.select();

      try {
        document.execCommand("copy");
        flashCopied(buttonEl);
      } catch (error) {
        /*
         * Copying silently fails in unsupported browsers;
         * the text remains visible for manual selection.
         */
      }

      document.body.removeChild(textarea);
    }

    /* =======================================================
       APA-FORMATTED AUTHOR LINES
       =======================================================
       One pre-formatted "Last, I. I., & Last, I. I." string per
       citation key, built from each entry's own bib author (or,
       for the one edited volume, editor) field. Used below to
       replace the theme's own "Initials Last, ... and Initials
       Last" author-line rendering, which is not APA style.
       ======================================================= */

    const AUTHOR_MAP = {
      LiChengBensonInPress: "Li, Z., Cheng, J. T., & Benson, A. J.",
      kuper2026culturaldifferencesinthepers: "Kuper, N., Gardiner, G., Baranski, E., Funder, D. C., Rauthmann, J. F., Yeung, V. W. L., & International Situations Project",
      chmielowiceszymanski2026howdifferentformsofsocialran: "Chmielowice-Szymanski, N. S., Cheng, J. T., Millett, M. A., Cillessen, A. H. N., et al.",
      laustsen2025crossculturalevidencethatint: "Laustsen, L., Sheng, X., Ahmad, M. G., Al-Shawaf, L., Banai, B., Banai, I. P., et al.",
      li2024powermotivespersonalitycorre: "Li, Z., Lynch, J., Sun, T., Rizkyana, Q., Cheng, J. T., & Benson, A. J.",
      cheng2024prestigebasedleadershipoffer: "Cheng, J. T.",
      baranski2024personalityandconception: "Baranski, E., Gardiner, G., Shaman, N., Shagan, J., Lee, D., International Situations Project, Funder, D. C., et al.",
      cheng2023dominanceandprestigeinlead: "Cheng, J. T.",
      cheng2023sexandgendereffectsonpowerst: "Cheng, J. T., Hemelrijk, C. K., Hentschel, T., Huchard, E., Kappeler, P. M., et al.",
      cheng2023eyegazeandvisualattentionasa: "Cheng, J. T., Gerpott, F. H., Benson, A. J., Bucker, B., Foulsham, T., Lansu, T. A. M., et al.",
      forby2023readingtheroom: "Forby, L., Anderson, N. C., Cheng, J. T., Foulsham, T., Karstadt, B., Dawson, J., et al.",
      gardiner2023theeconomicwellbeingofnation: "Gardiner, G., Lee, D. I., Baranski, E., Funder, D. C., Beramendi, M., Bastian, B., et al.",
      cheng2022whentoughnessbegetsrespect: "Cheng, J. T., Dhaliwal, N. A., & Too, M. A.",
      mcclanahan2022twowaystostayatthetop: "McClanahan, K. J., Maner, J. K., & Cheng, J. T.",
      chen2022thevigilanteidentityandorgan: "Chen, F. X., Graso, M., Aquino, K., Lin, L., Cheng, J. T., DeCelles, K., & Vadera, A. K.",
      zeng2022dominanceinhumans: "Zeng, T. C., Cheng, J. T., & Henrich, J.",
      chen2021harshbutexpedient: "Chen, F. X., Zhang, X., Laustsen, L., & Cheng, J. T.",
      cheng2021dominanceisnecessarytoexplai: "Cheng, J. T., Tracy, J. L., & Henrich, J.",
      baranski2021internationaloptimism: "Baranski, E., Sweeny, K., Gardiner, G., International Situations Project, et al.",
      baranski2021whointheworldistrying: "Baranski, E., Sweeny, K., Gardiner, G., Funder, D. C., et al.",
      redhead2021takingchargeandsteppingin: "Redhead, D., Dhaliwal, N., & Cheng, J. T.",
      aung2021lowfundamentalandformantfreq: "Aung, T., Goetz, S., Adams, J., McKenna, C., Hess, C., Roytman, S., Cheng, J. T., et al.",
      redhead2021statuscompetitionandpeerrela: "Redhead, D., Cheng, J. T., & O'Gorman, R.",
      redhead2021individualsthatimposecosts: "Redhead, D., Cheng, J. T., & O'Gorman, R.",
      cheng2021thesocialtransmissionofoverc: "Cheng, J. T., Anderson, C., Tenney, E. R., Brion, S., Moore, D. A., & Logg, J. M.",
      cheng2020overconfidenceiscontagious: "Cheng, J. T., Tenney, E. R., Moore, D. A., & Logg, J. M.",
      cheng2018forceandpersuasionhowdowe: "Cheng, J. T.",
      gardiner2019towardsmeaningfulcompariso: "Gardiner, G., Sauerberger, K., International Situations Project, Funder, D. C., et al.",
      redhead2021higherstatusingroup: "Redhead, D., Cheng, J. T., & O'Gorman, R.",
      lee2020situationalexperiencearoundt: "Lee, D. I., Gardiner, G., Baranski, E., International Situations Project, et al.",
      vankleef2020powerstatusandhierarchy: "van Kleef, G. A., & Cheng, J. T.",
      cheng2020dominanceprestigeandtheroleo: "Cheng, J. T.",
      cheng2020whysocialstatusisessentialbu: "Cheng, J. T., & Tracy, J. L.",
      vogt2020childhoodgrowthinmathandread: "Vogt, R. L., Cheng, J. T., & Briley, D. A.",
      cheng2020theneurobiologyofhumansocial: "Cheng, J. T., & Kornienko, O.",
      tracy2020theevolutionofprideandsocial: "Tracy, J. L., Mercadante, E., Witkower, Z., & Cheng, J. T.",
      witkower2020twosignalsofsocialrank: "Witkower, Z., Tracy, J. L., Cheng, J. T., & Henrich, J.",
      cheng2014jobmarketmemoir: "Cheng, J. T.",
      gardiner2019assessingpersonalityacross13: "Gardiner, G., Guillaume, E., Stauner, N., Bae, J., Han, G., Moon, J., Bronin, I., et al.",
      gardiner2020happinessaroundtheworld: "Gardiner, G., Lee, D., Baranski, E., Funder, D., International Situations Project, et al.",
      redhead2019onthedynamicsofsocialhierarc: "Redhead, D. J., Cheng, J. T., Driver, C., Foulsham, T., & O'Gorman, R.",
      cheng2018prestigeinalargescalesocialg: "Cheng, J. T., Kornienko, O., & Granger, D. A.",
      weidman2018thepsychologicalstructureofh: "Weidman, A. C., Cheng, J. T., & Tracy, J. L.",
      baranski2017comparisonsofdailybehaviorac: "Baranski, E. N., Gardiner, G., Guillaume, E., Aveyard, M., Bastian, B., Bronin, I., et al.",
      guillaume2016theworldat7: "Guillaume, E., Baranski, E., Todd, E., Bastian, B., Bronin, I., Ivanova, C., et al.",
      cheng2016listenfollowme: "Cheng, J. T., Tracy, J. L., Ho, S., & Henrich, J.",
      weidman2015isshetheonepersonalityjudgme: "Weidman, A. C., Cheng, J. T., Chisholm, C., & Tracy, J. L.",
      shi2015crossculturalevidenceforthet: "Shi, Y., Chung, J. M., Cheng, J. T., Tracy, J. L., Robins, R. W., Chen, X., & Zheng, Y.",
      anderson2014thepsychologyofsocialstatus: "Anderson, C., Cheng, J. T., & Tracy, J. L. (Eds.)",
      cheng2014theassessmentofsocialstatus: "Cheng, J. T., Weidman, A. C., & Tracy, J. L.",
      cheng2014towardaunifiedscienceofhiera: "Cheng, J. T., & Tracy, J. L.",
      tracy2014pride: "Tracy, J. L., Weidman, A. C., Cheng, J. T., & Martens, J. P.",
      cheng2013arenarcissistshardyorvulnera: "Cheng, J. T., Tracy, J. L., & Miller, G. E.",
      cheng2013theimpactofwealthonprestigea: "Cheng, J. T., & Tracy, J. L.",
      cheng2013twowaystothetop: "Cheng, J. T., Tracy, J. L., Foulsham, T., Kingstone, A., & Henrich, J.",
      feinberg2012gossipasaneffectiveandlowcos: "Feinberg, M., Cheng, J. T., & Willer, R.",
      tracy2012theemotionaldynamicsofnarcis: "Tracy, J. L., Cheng, J. T., Martens, J. P., & Robins, R. W.",
      foulsham2010gazeallocationinadynamicsitu: "Foulsham, T., Cheng, J. T., Tracy, J. L., Henrich, J., & Kingstone, A.",
      shariff2010furtherthoughtsontheevolutio: "Shariff, A. F., Tracy, J. L., Cheng, J. T., & Henrich, J.",
      cheng2010pridepersonalityandtheevolut: "Cheng, J. T., Tracy, J. L., & Henrich, J.",
      shariff2010naturalismandthetaleoftwofac: "Shariff, A. F., Tracy, J. L., & Cheng, J. T.",
      tracy2010anaturalistsviewofpride: "Tracy, J. L., Shariff, A. F., & Cheng, J. T.",
      tracy2009authenticandhubristicpride: "Tracy, J. L., Cheng, J. T., Robins, R. W., & Trzesniewski, K. H.",
    };

    publicationItems.forEach(function (publication) {
      /*
       * As above: a single entry that fails to process (e.g.
       * an unexpected markup shape for one bib entry) should
       * not throw and silently abort processing for every
       * publication that follows it in document order.
       */

      try {
        processPublicationEntry(publication);
      } catch (error) {
        console.error(
          "Publications: failed to process an entry",
          getPublicationKey(publication),
          error
        );
      }
    });

    function processPublicationEntry(publication) {
      /* =====================================================
         DISPLAY ALL AUTHORS
         ===================================================== */

      const authorContainer =
        publication.querySelector(".author");

      if (authorContainer) {
        const potentiallyHiddenAuthors =
          authorContainer.querySelectorAll(
            [
              ".more-authors",
              ".more-authors.hidden",
              ".hidden-authors",
              ".hidden-authors.hidden",
              "span.hidden",
              "[data-more-authors]"
            ].join(", ")
          );

        potentiallyHiddenAuthors.forEach(function (element) {
          element.classList.remove("hidden");
          element.removeAttribute("hidden");
          element.removeAttribute("aria-hidden");

          element.style.display = "inline";
          element.style.visibility = "visible";
          element.style.opacity = "1";
        });

        /*
         * Remove buttons and links used only to expand the
         * shortened author list.
         */

        const authorControls =
          authorContainer.querySelectorAll(
            [
              "button",
              '[role="button"]',
              ".more-authors-click",
              ".more-authors-button",
              "a.more-authors"
            ].join(", ")
          );

        authorControls.forEach(function (control) {
          control.remove();
        });

        /*
         * Some al-folio versions use a clickable text element
         * instead of a conventional button.
         */

        const authorElements =
          authorContainer.querySelectorAll(
            "span, a"
          );

        authorElements.forEach(function (element) {
          const label =
            element.textContent
              .trim()
              .toLowerCase();

          const isExpansionControl =
            label === "more authors" ||
            label === "show more" ||
            label === "expand" ||
            label === "..." ||
            label === "…" ||
            label.includes("more author");

          if (isExpansionControl) {
            element.remove();
          }
        });

        /*
         * Fallback: some al-folio versions hide the remaining
         * authors with a class name we haven't accounted for
         * above. Force-show anything still computed as hidden
         * inside the author line so lists don't trail off with
         * a dangling "and".
         */

        const stillHiddenAuthorNodes =
          authorContainer.querySelectorAll("*");

        stillHiddenAuthorNodes.forEach(function (element) {
          const computedStyle =
            window.getComputedStyle(element);

          if (
            computedStyle.display === "none" ||
            computedStyle.visibility === "hidden"
          ) {
            element.style.display = "inline";
            element.style.visibility = "visible";
            element.style.opacity = "1";
          }
        });

        /*
         * APA-FORMAT THE AUTHOR LINE
         * The theme's own author-line markup renders names as
         * "Initials Last, Initials Last, and Initials Last" —
         * not proper APA style. AUTHOR_MAP holds a pre-formatted
         * "Last, I. I., & Last, I. I." string per citation key
         * (built from each entry's own bib author/editor field),
         * which fully replaces the rendered text below. If a key
         * is missing from the map, the theme's own rendering is
         * left untouched rather than breaking the entry.
         */

        const entryKeyForAuthors = getPublicationKey(publication);
        const apaAuthors = AUTHOR_MAP[entryKeyForAuthors];

        if (apaAuthors) {
          authorContainer.textContent = apaAuthors;
        }
      }

      /* =====================================================
         REMOVE THE YEAR FROM THE JOURNAL LINE
         ===================================================== */

      const periodical =
        publication.querySelector(".periodical");

      if (periodical) {
        /*
         * First remove dedicated year elements that may be
         * nested inside the journal line.
         */

        const nestedYearElements =
          periodical.querySelectorAll(
            [
              ".year",
              ".year-label",
              ".year-badge",
              ".publication-year"
            ].join(", ")
          );

        nestedYearElements.forEach(function (element) {
          element.remove();
        });

        /*
         * The year is often plain text rather than a separate
         * HTML element. Walk backward through the text nodes
         * and remove a trailing four-digit publication year.
         *
         * Examples removed:
         *
         * Journal Name, 2024
         * Journal Name (2024)
         * Journal Name. 2024
         * Journal Name 2024
         */

        const textWalker =
          document.createTreeWalker(
            periodical,
            NodeFilter.SHOW_TEXT
          );

        const textNodes = [];
        let currentNode;

        while (
          (currentNode = textWalker.nextNode())
        ) {
          textNodes.push(currentNode);
        }

        for (
          let index = textNodes.length - 1;
          index >= 0;
          index -= 1
        ) {
          const textNode = textNodes[index];

          if (!textNode.nodeValue.trim()) {
            continue;
          }

          const originalText =
            textNode.nodeValue;

          const revisedText =
            originalText.replace(
              /(?:\s*[,.;]\s*|\s+)\(?(?:(?:19|20)\d{2}|in press)\)?[.,;]?\s*$/i,
              ""
            );

          if (revisedText !== originalText) {
            textNode.nodeValue = revisedText;
            break;
          }
        }

        /*
         * Clean up punctuation or whitespace left behind after
         * removing the year.
         */

        periodical.innerHTML =
          periodical.innerHTML
            .replace(
              /\s+([,.;:])/g,
              "$1"
            )
            .replace(
              /[,;]\s*$/,
              ""
            )
            .trim();
      }

      /* =====================================================
         REMOVE ANY OTHER YEAR BADGES
         ===================================================== */

      const separateYearElements =
        publication.querySelectorAll(
          [
            ".year",
            ".year-label",
            ".year-badge",
            ".publication-year"
          ].join(", ")
        );

      separateYearElements.forEach(function (yearElement) {
        if (
          !yearElement.classList.contains(
            "publication-year-above-title"
          )
        ) {
          yearElement.remove();
        }
      });

      /*
       * Registered as each of Highlights, Cite APA, and Cite
       * BibTeX is built below, so every button's click handler
       * can close the other two before opening its own —
       * keeping only one dropdown open per entry at a time.
       */

      const dropdownControls = [];

      /* =====================================================
         HIGHLIGHTS: BUILD THE BULLET LIST
         =====================================================
         The overview box is no longer permanently shown, nor
         rendered as plain paragraphs — it toggles open via a
         "Highlights" button, first in the button row, and its
         content is rebuilt as a bulleted list with a header
         row, using the same take-over-the-toggle approach as
         the Cite buttons below.
         ===================================================== */

      const overviewContent =
        publication.querySelector(
          "div.abstract"
        );

      if (overviewContent) {
        overviewContent.classList.add(
          "publication-overview"
        );

        /*
         * The theme's own "hidden" class applies its own
         * max-height/overflow collapse independent of the
         * display property — that's why the box still
         * rendered as a near-zero-height sliver even once
         * display was forced to "block". Removing the class
         * entirely hands full control of visibility to our
         * own inline display toggle.
         */

        overviewContent.classList.remove(
          "hidden"
        );

        overviewContent.style.setProperty(
          "display",
          "none",
          "important"
        );

        const highlightsText =
          overviewContent.textContent.trim();

        if (highlightsText) {
          const bullets = splitIntoHighlightBullets(
            highlightsText
          );

          while (overviewContent.firstChild) {
            overviewContent.removeChild(
              overviewContent.firstChild
            );
          }

          const highlightsHeader =
            document.createElement("div");

          highlightsHeader.className =
            "pub-highlights-header";

          highlightsHeader.innerHTML =
            '<i class="fas fa-star" aria-hidden="true"></i><span>Highlights</span>';

          const highlightsList =
            document.createElement("ul");

          highlightsList.className =
            "pub-highlights-list";

          bullets.forEach(function (
            bulletText,
            bulletIndex
          ) {
            const bulletItem =
              document.createElement("li");

            if (bulletIndex === 0) {
              bulletItem.className =
                "pub-highlights-hook";
            }

            bulletItem.textContent = bulletText;

            highlightsList.appendChild(
              bulletItem
            );
          });

          overviewContent.appendChild(
            highlightsHeader
          );
          overviewContent.appendChild(
            highlightsList
          );
        }
      }

      /* =====================================================
         RELABEL, ICON, AND REORDER PUBLICATION BUTTONS
         ===================================================== */

      const publicationButtons =
        publication.querySelectorAll(
          ".links a.btn, .links button.btn"
        );

      const BUTTON_ICONS = {
        pdf: "fas fa-file-lines",
        url: "fas fa-arrow-up-right-from-square",
        site: "fas fa-globe",
        supp: "fas fa-paperclip"
      };

      const BUTTON_LABELS = {
        pdf: "PDF",
        url: "URL",
        site: "Site",
        supp: "Supplement"
      };

      const BUTTON_ARIA = {
        pdf: "Download PDF",
        url: "Open publication URL",
        site: "Visit site",
        supp: "Download supplemental materials"
      };

      let citeTriggerButton = null;
      let overviewTriggerButton = null;

      publicationButtons.forEach(function (button) {
        const originalLabel =
          button.textContent
            .trim()
            .toLowerCase();

        /*
         * jekyll-scholar also auto-renders a separate "DOI"
         * button from the doi field. Since it links to the
         * same place as the URL button below, drop it here
         * to avoid two redundant link buttons.
         */

        if (
          originalLabel === "doi" ||
          button.classList.contains("doi")
        ) {
          button.remove();
          return;
        }

        /*
         * The "Cite" toggle (rendered as "Bib" by default)
         * is handled separately below, not as a link button.
         */

        if (
          originalLabel === "bib" ||
          originalLabel === "bibtex" ||
          button.classList.contains("bibtex")
        ) {
          citeTriggerButton = button;
          return;
        }

        /*
         * The "Overview" toggle (rendered as "Abstract" by
         * default) is also handled separately below.
         */

        if (
          originalLabel === "abstract" ||
          originalLabel === "overview" ||
          button.classList.contains("abstract")
        ) {
          overviewTriggerButton = button;
          return;
        }

        let buttonType = null;

        if (
          originalLabel === "pdf" ||
          button.classList.contains("pdf")
        ) {
          buttonType = "pdf";
        } else if (
          originalLabel === "html" ||
          button.classList.contains("html") ||
          button.getAttribute("data-type") === "html"
        ) {
          buttonType = "url";
        } else if (
          originalLabel === "website" ||
          button.classList.contains("website")
        ) {
          buttonType = "site";
        } else if (
          originalLabel === "code" ||
          button.classList.contains("code")
        ) {
          /*
           * The "code" field is repurposed for supplemental
           * materials (this bibliography has no software/code
           * entries), rendered as "Supp" below.
           */

          buttonType = "supp";
        }

        if (!buttonType) {
          return;
        }

        button.setAttribute(
          "data-btn-type",
          buttonType
        );

        /*
         * PDF, Supplement, URL, and Site all lead away from the
         * publications list to an external document or page.
         * Opening them in a new tab preserves the visitor's
         * search/topic-filter state on this page, matching the
         * target="_blank" convention already used for outbound
         * links elsewhere on the site (Contact, Join the Lab).
         */

        if (button.tagName === "A") {
          button.setAttribute("target", "_blank");
          button.setAttribute("rel", "noopener noreferrer");
        }

        button.innerHTML =
          '<i class="' +
          BUTTON_ICONS[buttonType] +
          '" aria-hidden="true"></i><span>' +
          BUTTON_LABELS[buttonType] +
          "</span>";

        button.setAttribute(
          "aria-label",
          BUTTON_ARIA[buttonType]
        );
      });

      const linksContainer =
        publication.querySelector(".links");

      /* =====================================================
         OVERVIEW: BUILD THE TOGGLE BUTTON
         =====================================================
         Same take-over-the-toggle approach as Cite below:
         clone the native abstract-toggle button to strip its
         old listener, relabel it, and wire our own click
         handler.
         ===================================================== */

      if (overviewTriggerButton && overviewContent) {
        const freshOverviewButton =
          overviewTriggerButton.cloneNode(true);

        sanitizeClonedTrigger(freshOverviewButton);

        freshOverviewButton.classList.remove(
          "abstract"
        );
        freshOverviewButton.classList.add(
          "pub-cite-trigger"
        );

        freshOverviewButton.innerHTML =
          '<i class="fas fa-star" aria-hidden="true"></i><span>Highlights</span><span class="pub-highlights-toggle-icon" aria-hidden="true"></span>';

        freshOverviewButton.setAttribute(
          "data-btn-type",
          "highlights"
        );
        freshOverviewButton.setAttribute(
          "aria-label",
          "Show highlights"
        );

        overviewTriggerButton.replaceWith(
          freshOverviewButton
        );

        /*
         * Use setProperty with "important" priority rather than
         * a plain assignment. A plain inline style loses to an
         * external stylesheet rule that also uses !important
         * (e.g. a leftover Bootstrap ".collapse" rule the
         * theme may still apply to this element) — setting our
         * own priority to "important" guarantees this toggle
         * always wins, the same fix already applied to the
         * Cite boxes below.
         */

        const highlightsDropdownEntry = {
          box: overviewContent,
          button: freshOverviewButton
        };

        dropdownControls.push(
          highlightsDropdownEntry
        );

        freshOverviewButton.addEventListener(
          "click",
          function (event) {
            event.preventDefault();

            const showing =
              overviewContent.style.display !== "none";

            dropdownControls.forEach(
              closeDropdownEntry
            );

            if (!showing) {
              openDropdownEntry(
                highlightsDropdownEntry
              );
            }
          }
        );
      }

      /* =====================================================
         CITE: BUILD THE APA BOX AND STYLE THE BIBTEX BOX
         =====================================================
         jekyll-scholar renders a "Bib" toggle and a hidden
         BibTeX block for each entry. Rather than guess at the
         theme's own show/hide mechanism (which turned out to
         leave both boxes visible on load), we take over the
         toggle entirely: force both boxes hidden up front, and
         wire our own click handlers on two cloned buttons —
         "Cite APA" and "Cite BibTeX" — each of which shows
         only its own box, independently of the other.
         ===================================================== */

      const bibtexEl =
        publication.querySelector("div.bibtex");

      if (bibtexEl) {
        bibtexEl.classList.add(
          "pub-cite-box",
          "pub-cite-bibtex"
        );

        bibtexEl.style.display = "none";

        /*
         * Extract the plain text of the theme's original
         * bibtex content (discarding its syntax-highlighting
         * markup), then build a header row above a plain-text
         * body with a label and a Copy button that always sits
         * in normal flow — never overlapping the citation text
         * below, regardless of its length. Using plain text
         * instead of the original <pre>/<code> markup also
         * avoids some browsers' automatic "copy code block"
         * icon, which otherwise appears when hovering over
         * syntax-highlighted code but not over plain text.
         */

        /*
         * jekyll-scholar's {{ entry.bibtex }} dumps every field
         * exactly as parsed from papers.bib — including fields
         * that only exist to drive this site's own buttons
         * (bibtex_show, pdf, code, html), never real BibTeX
         * fields. Left in, a citation someone copies into
         * Zotero/BibDesk/JabRef would carry a local filename or
         * this site's own toggle flag. Strip those specific
         * field lines only; every genuine bibliographic field
         * (author, title, journal, volume, pages, doi, year,
         * publisher, isbn, abstract, etc.) is left untouched.
         */

        const bibtexRawText =
          bibtexEl.textContent.trim();

        const bibtexPlainText = bibtexRawText
          .split("\n")
          .filter(function (line) {
            return !/^\s*(bibtex_show|pdf|code|html)\s*=\s*\{/i.test(
              line
            );
          })
          .join("\n");

        const entryVolume = extractBibField(
          bibtexRawText,
          "volume"
        );

        const entryNumber = extractBibField(
          bibtexRawText,
          "number"
        );

        const entryPages = extractBibField(
          bibtexRawText,
          "pages"
        );

        while (bibtexEl.firstChild) {
          bibtexEl.removeChild(
            bibtexEl.firstChild
          );
        }

        const bibtexBody =
          document.createElement("div");

        bibtexBody.className = "pub-cite-body";
        bibtexBody.textContent = bibtexPlainText;

        /*
         * Force wrapping via inline styles on the body wrapper
         * and every descendant it contains (whatever markup the
         * theme happens to use inside .bibtex, e.g. a raw text
         * node, or a <pre>/<code> pair). An inline style set
         * with "important" priority always wins over any
         * external stylesheet, even one that also uses
         * !important, so this can't be silently overridden by
         * unknown gem-owned CSS the way a plain class rule can.
         */

        [bibtexBody]
          .concat(
            Array.prototype.slice.call(
              bibtexBody.querySelectorAll("*")
            )
          )
          .forEach(function (el) {
            el.style.setProperty(
              "white-space",
              "pre-wrap",
              "important"
            );
            el.style.setProperty(
              "word-break",
              "break-word",
              "important"
            );
            el.style.setProperty(
              "overflow-wrap",
              "anywhere",
              "important"
            );
            el.style.setProperty(
              "max-width",
              "100%",
              "important"
            );
            el.style.setProperty(
              "box-sizing",
              "border-box",
              "important"
            );
          });

        const bibtexHeader =
          document.createElement("div");

        bibtexHeader.className = "pub-cite-header";

        const bibtexLabel =
          document.createElement("span");

        bibtexLabel.className = "pub-cite-label";
        bibtexLabel.textContent = "BibTeX";

        const bibtexLabelIcon =
          document.createElement("i");

        bibtexLabelIcon.className = "fas fa-code";
        bibtexLabelIcon.setAttribute(
          "aria-hidden",
          "true"
        );

        const bibtexLabelGroup =
          document.createElement("span");

        bibtexLabelGroup.className =
          "pub-cite-label-group";

        bibtexLabelGroup.appendChild(
          bibtexLabelIcon
        );
        bibtexLabelGroup.appendChild(bibtexLabel);

        const bibtexCopyBtn =
          document.createElement("button");

        bibtexCopyBtn.type = "button";
        bibtexCopyBtn.className = "pub-cite-copy";
        bibtexCopyBtn.innerHTML =
          '<i class="fas fa-copy" aria-hidden="true"></i><span>Copy</span>';

        bibtexCopyBtn.addEventListener(
          "click",
          function (event) {
            event.stopPropagation();

            const text =
              bibtexBody.textContent.trim();

            copyPublicationText(
              text,
              bibtexCopyBtn
            );
          }
        );

        bibtexHeader.appendChild(bibtexLabelGroup);
        bibtexHeader.appendChild(bibtexCopyBtn);

        bibtexEl.appendChild(bibtexHeader);
        bibtexEl.appendChild(bibtexBody);

        const doiButton =
          linksContainer
            ? linksContainer.querySelector(
                '[data-btn-type="url"]'
              )
            : null;

        const doiHref =
          doiButton
            ? doiButton.getAttribute("href")
            : null;

        const apaCitation = buildApaCitation(
          publication,
          doiHref,
          entryVolume,
          entryNumber,
          entryPages
        );

        /*
         * The visible journal line under each title is
         * intentionally left as just the journal/book name — no
         * volume, issue, or pages there. Those get added only to
         * the Cite APA box (via buildApaCitation above) and are
         * already present verbatim in the Cite BibTeX box.
         */

        let apaBox = null;

        if (apaCitation) {
          apaBox = document.createElement("div");

          apaBox.className =
            "pub-cite-box pub-cite-apa";

          apaBox.style.display = "none";

          const apaHeader =
            document.createElement("div");

          apaHeader.className = "pub-cite-header";

          const apaLabel =
            document.createElement("span");

          apaLabel.className = "pub-cite-label";
          apaLabel.textContent = "APA citation";

          const apaLabelIcon =
            document.createElement("i");

          apaLabelIcon.className =
            "fas fa-quote-right";
          apaLabelIcon.setAttribute(
            "aria-hidden",
            "true"
          );

          const apaLabelGroup =
            document.createElement("span");

          apaLabelGroup.className =
            "pub-cite-label-group";

          apaLabelGroup.appendChild(apaLabelIcon);
          apaLabelGroup.appendChild(apaLabel);

          const apaCopyBtn =
            document.createElement("button");

          apaCopyBtn.type = "button";
          apaCopyBtn.className = "pub-cite-copy";
          apaCopyBtn.innerHTML =
            '<i class="fas fa-copy" aria-hidden="true"></i><span>Copy</span>';

          apaCopyBtn.addEventListener(
            "click",
            function (event) {
              event.stopPropagation();

              copyPublicationText(
                apaCitation.text,
                apaCopyBtn,
                apaCitation.html
              );
            }
          );

          apaHeader.appendChild(apaLabelGroup);
          apaHeader.appendChild(apaCopyBtn);

          const apaBody =
            document.createElement("div");

          apaBody.className = "pub-cite-body";

          const apaTextEl =
            document.createElement("div");

          apaTextEl.className = "pub-cite-text";
          apaTextEl.innerHTML = apaCitation.html;

          apaBody.appendChild(apaTextEl);

          apaBox.appendChild(apaHeader);
          apaBox.appendChild(apaBody);

          bibtexEl.insertAdjacentElement(
            "beforebegin",
            apaBox
          );
        }

        if (citeTriggerButton) {
          /*
           * Clone-and-replace strips any click handler the
           * theme already attached, so only our own toggles
           * run. Two independent buttons are built from the
           * single native toggle: one shows only the APA box,
           * the other shows only the BibTeX box.
           */

          let citeApaButton = null;

          if (apaBox) {
            citeApaButton =
              citeTriggerButton.cloneNode(true);

            sanitizeClonedTrigger(citeApaButton);

            citeApaButton.innerHTML =
              '<i class="fas fa-quote-right" aria-hidden="true"></i><span>Cite APA</span><span class="pub-highlights-toggle-icon" aria-hidden="true"></span>';
            citeApaButton.classList.add(
              "pub-cite-trigger"
            );
            citeApaButton.setAttribute(
              "data-btn-type",
              "cite-apa"
            );
            citeApaButton.setAttribute(
              "aria-label",
              "Show APA citation"
            );

            const citeApaDropdownEntry = {
              box: apaBox,
              button: citeApaButton
            };

            dropdownControls.push(
              citeApaDropdownEntry
            );

            citeApaButton.addEventListener(
              "click",
              function (event) {
                event.preventDefault();

                const showing =
                  apaBox.style.display !== "none";

                dropdownControls.forEach(
                  closeDropdownEntry
                );

                if (!showing) {
                  openDropdownEntry(
                    citeApaDropdownEntry
                  );
                }
              }
            );
          }

          const citeBibtexButton =
            citeTriggerButton.cloneNode(true);

          sanitizeClonedTrigger(citeBibtexButton);

          citeBibtexButton.innerHTML =
            '<i class="fas fa-code" aria-hidden="true"></i><span>Cite BibTeX</span><span class="pub-highlights-toggle-icon" aria-hidden="true"></span>';
          citeBibtexButton.classList.add(
            "pub-cite-trigger"
          );
          citeBibtexButton.setAttribute(
            "data-btn-type",
            "cite-bibtex"
          );
          citeBibtexButton.setAttribute(
            "aria-label",
            "Show BibTeX citation"
          );

          const citeBibtexDropdownEntry = {
            box: bibtexEl,
            button: citeBibtexButton
          };

          dropdownControls.push(
            citeBibtexDropdownEntry
          );

          citeBibtexButton.addEventListener(
            "click",
            function (event) {
              event.preventDefault();

              const showing =
                bibtexEl.style.display !== "none";

              dropdownControls.forEach(
                closeDropdownEntry
              );

              if (!showing) {
                openDropdownEntry(
                  citeBibtexDropdownEntry
                );
              }
            }
          );

          if (citeApaButton) {
            citeTriggerButton.replaceWith(
              citeApaButton
            );

            citeApaButton.insertAdjacentElement(
              "afterend",
              citeBibtexButton
            );
          } else {
            citeTriggerButton.replaceWith(
              citeBibtexButton
            );
          }
        }
      }

      /*
       * Final button order, left to right: Highlights, PDF,
       * Supp, URL, Cite APA, Cite BibTeX, Site. Any type not
       * present for this entry is simply skipped.
       */

      if (linksContainer) {
        [
          "highlights",
          "pdf",
          "supp",
          "url",
          "cite-apa",
          "cite-bibtex",
          "site"
        ].forEach(function (buttonType) {
          const button = linksContainer.querySelector(
            '[data-btn-type="' + buttonType + '"]'
          );

          if (button) {
            linksContainer.appendChild(button);
          }
        });
      }

      /*
       * ENTRY-SPECIFIC EXTRA LINKS
       * A small escape hatch for one-off supplementary links that
       * don't fit the site's four standard bib fields (pdf, html,
       * code, website) — used here for a second supplemental
       * document on the PNAS "Dominance is necessary..." reply.
       */

      const EXTRA_LINKS = {
        cheng2021dominanceisnecessarytoexplai: [
          {
            text: "Further exposition of 3 concerns",
            href: "/assets/pdf/cheng2021dominanceisnecessarytoexplai-exposition.pdf"
          }
        ]
      };

      const entryKey = getPublicationKey(publication);
      const extraLinks = EXTRA_LINKS[entryKey];

      if (extraLinks && extraLinks.length && linksContainer) {
        const extraLinksRow = document.createElement("p");
        extraLinksRow.className = "pub-extra-links";

        extraLinks.forEach(function (link, index) {
          const a = document.createElement("a");
          a.href = link.href;
          a.textContent = link.text;
          extraLinksRow.appendChild(a);

          if (index < extraLinks.length - 1) {
            extraLinksRow.appendChild(
              document.createTextNode(" · ")
            );
          }
        });

        linksContainer.insertAdjacentElement(
          "afterend",
          extraLinksRow
        );
      }
    }

    /* =======================================================
       TOPIC FILTER
       =======================================================
       Each publication is tagged below by its citation key
       (the id jekyll-scholar assigns to each entry). If a key
       is missing from this map, that entry stays visible
       under every filter rather than disappearing.
       ======================================================= */

    const TOPIC_MAP = {
      LiChengBensonInPress: ["leadership", "dominance-prestige", "well-being"],
      kuper2026culturaldifferencesinthepers: ["culture", "personality"],
      chmielowiceszymanski2026howdifferentformsofsocialran: ["status-hierarchy"],
      laustsen2025crossculturalevidencethatint: ["leadership", "culture", "dominance-prestige"],
      li2024powermotivespersonalitycorre: ["leadership", "personality"],
      cheng2024prestigebasedleadershipoffer: ["leadership", "gender", "dominance-prestige"],
      baranski2024personalityandconception: ["culture", "personality"],
      cheng2023dominanceandprestigeinlead: ["leadership", "dominance-prestige"],
      cheng2023sexandgendereffectsonpowerst: ["gender", "status-hierarchy", "dominance-prestige"],
      cheng2023eyegazeandvisualattentionasa: ["leadership"],
      forby2023readingtheroom: ["social-connection"],
      gardiner2023theeconomicwellbeingofnation: ["culture", "well-being"],
      cheng2022whentoughnessbegetsrespect: ["dominance-prestige", "status-hierarchy"],
      mcclanahan2022twowaystostayatthetop: ["dominance-prestige", "status-hierarchy"],
      chen2022thevigilanteidentityandorgan: ["status-hierarchy"],
      zeng2022dominanceinhumans: ["dominance-prestige"],
      chen2021harshbutexpedient: ["leadership", "dominance-prestige"],
      cheng2021dominanceisnecessarytoexplai: ["dominance-prestige", "status-hierarchy"],
      baranski2021internationaloptimism: ["culture", "personality", "well-being"],
      baranski2021whointheworldistrying: ["personality", "culture"],
      gardiner2020happinessaroundtheworld: ["culture", "well-being"],
      cheng2020overconfidenceiscontagious: ["personality"],
      redhead2021takingchargeandsteppingin: ["dominance-prestige", "status-hierarchy"],
      aung2021lowfundamentalandformantfreq: ["dominance-prestige"],
      redhead2021statuscompetitionandpeerrela: ["status-hierarchy", "social-connection"],
      redhead2021individualsthatimposecosts: ["dominance-prestige"],
      cheng2021thesocialtransmissionofoverc: ["personality"],
      cheng2018forceandpersuasionhowdowe: ["dominance-prestige", "leadership"],
      gardiner2019towardsmeaningfulcompariso: ["culture", "personality"],
      redhead2021higherstatusingroup: ["status-hierarchy"],
      lee2020situationalexperiencearoundt: ["culture"],
      vankleef2020powerstatusandhierarchy: ["status-hierarchy", "leadership"],
      cheng2020dominanceprestigeandtheroleo: ["dominance-prestige", "status-hierarchy"],
      cheng2020whysocialstatusisessentialbu: ["leadership", "status-hierarchy"],
      vogt2020childhoodgrowthinmathandread: ["personality"],
      cheng2020theneurobiologyofhumansocial: ["personality", "social-connection"],
      tracy2020theevolutionofprideandsocial: ["pride-emotion", "status-hierarchy"],
      witkower2020twosignalsofsocialrank: ["dominance-prestige", "status-hierarchy"],
      gardiner2019assessingpersonalityacross13: ["culture", "personality"],
      cheng2014jobmarketmemoir: ["leadership"],
      redhead2019onthedynamicsofsocialhierarc: ["status-hierarchy", "dominance-prestige"],
      cheng2018prestigeinalargescalesocialg: ["dominance-prestige"],
      weidman2018thepsychologicalstructureofh: ["personality"],
      baranski2017comparisonsofdailybehaviorac: ["culture"],
      guillaume2016theworldat7: ["culture"],
      cheng2016listenfollowme: ["dominance-prestige", "status-hierarchy"],
      weidman2015isshetheonepersonalityjudgme: ["personality"],
      shi2015crossculturalevidenceforthet: ["pride-emotion", "culture"],
      anderson2014thepsychologyofsocialstatus: ["status-hierarchy"],
      cheng2014theassessmentofsocialstatus: ["status-hierarchy"],
      cheng2014towardaunifiedscienceofhiera: ["dominance-prestige", "status-hierarchy"],
      tracy2014pride: ["pride-emotion"],
      cheng2013arenarcissistshardyorvulnera: ["personality"],
      cheng2013theimpactofwealthonprestigea: ["dominance-prestige", "status-hierarchy"],
      cheng2013twowaystothetop: ["dominance-prestige", "status-hierarchy"],
      feinberg2012gossipasaneffectiveandlowcos: ["status-hierarchy"],
      tracy2012theemotionaldynamicsofnarcis: ["personality", "pride-emotion"],
      foulsham2010gazeallocationinadynamicsitu: ["status-hierarchy"],
      shariff2010furtherthoughtsontheevolutio: ["pride-emotion"],
      cheng2010pridepersonalityandtheevolut: ["pride-emotion", "personality", "status-hierarchy"],
      shariff2010naturalismandthetaleoftwofac: ["pride-emotion"],
      tracy2010anaturalistsviewofpride: ["pride-emotion"],
      tracy2009authenticandhubristicpride: ["pride-emotion", "personality"]
    };

    publicationItems.forEach(function (publication) {
      const key = getPublicationKey(publication);
      const topics = TOPIC_MAP[key];

      if (topics) {
        publication.setAttribute(
          "data-topics",
          topics.join(" ")
        );
      }
    });

    /* =======================================================
       PUBLICATION TYPE BADGE
       ======================================================= */

    const PUB_TYPE_MAP = {
      LiChengBensonInPress: "Journal article",
      kuper2026culturaldifferencesinthepers: "Journal article",
      chmielowiceszymanski2026howdifferentformsofsocialran: "Journal article",
      laustsen2025crossculturalevidencethatint: "Journal article",
      li2024powermotivespersonalitycorre: "Journal article",
      cheng2024prestigebasedleadershipoffer: "Commentary",
      baranski2024personalityandconception: "Journal article",
      cheng2023dominanceandprestigeinlead: "Book chapter",
      cheng2023sexandgendereffectsonpowerst: "Editorial",
      cheng2023eyegazeandvisualattentionasa: "Journal article",
      forby2023readingtheroom: "Journal article",
      gardiner2023theeconomicwellbeingofnation: "Journal article",
      cheng2022whentoughnessbegetsrespect: "Journal article",
      mcclanahan2022twowaystostayatthetop: "Journal article",
      chen2022thevigilanteidentityandorgan: "Journal article",
      zeng2022dominanceinhumans: "Journal article",
      chen2021harshbutexpedient: "Journal article",
      cheng2021dominanceisnecessarytoexplai: "Commentary",
      baranski2021internationaloptimism: "Journal article",
      baranski2021whointheworldistrying: "Journal article",
      gardiner2020happinessaroundtheworld: "Journal article",
      cheng2020overconfidenceiscontagious: "Perspective",
      redhead2021takingchargeandsteppingin: "Journal article",
      aung2021lowfundamentalandformantfreq: "Journal article",
      redhead2021statuscompetitionandpeerrela: "Book chapter",
      redhead2021individualsthatimposecosts: "Book chapter",
      cheng2021thesocialtransmissionofoverc: "Journal article",
      cheng2018forceandpersuasionhowdowe: "Newsletter",
      gardiner2019towardsmeaningfulcompariso: "Book chapter",
      redhead2021higherstatusingroup: "Book chapter",
      lee2020situationalexperiencearoundt: "Journal article",
      vankleef2020powerstatusandhierarchy: "Editorial",
      cheng2020dominanceprestigeandtheroleo: "Journal article",
      cheng2020whysocialstatusisessentialbu: "Commentary",
      vogt2020childhoodgrowthinmathandread: "Journal article",
      cheng2020theneurobiologyofhumansocial: "Book chapter",
      tracy2020theevolutionofprideandsocial: "Book chapter",
      witkower2020twosignalsofsocialrank: "Journal article",
      gardiner2019assessingpersonalityacross13: "Journal article",
      cheng2014jobmarketmemoir: "Perspective",
      redhead2019onthedynamicsofsocialhierarc: "Journal article",
      cheng2018prestigeinalargescalesocialg: "Journal article",
      weidman2018thepsychologicalstructureofh: "Journal article",
      baranski2017comparisonsofdailybehaviorac: "Journal article",
      guillaume2016theworldat7: "Journal article",
      cheng2016listenfollowme: "Journal article",
      weidman2015isshetheonepersonalityjudgme: "Journal article",
      shi2015crossculturalevidenceforthet: "Journal article",
      anderson2014thepsychologyofsocialstatus: "Edited book",
      cheng2014theassessmentofsocialstatus: "Book chapter",
      cheng2014towardaunifiedscienceofhiera: "Book chapter",
      tracy2014pride: "Book chapter",
      cheng2013arenarcissistshardyorvulnera: "Journal article",
      cheng2013theimpactofwealthonprestigea: "Journal article",
      cheng2013twowaystothetop: "Journal article",
      feinberg2012gossipasaneffectiveandlowcos: "Journal article",
      tracy2012theemotionaldynamicsofnarcis: "Book chapter",
      foulsham2010gazeallocationinadynamicsitu: "Journal article",
      shariff2010furtherthoughtsontheevolutio: "Journal article",
      cheng2010pridepersonalityandtheevolut: "Journal article",
      shariff2010naturalismandthetaleoftwofac: "Journal article",
      tracy2010anaturalistsviewofpride: "Journal article",
      tracy2009authenticandhubristicpride: "Journal article"
    };

    publicationItems.forEach(function (publication) {
      const key = getPublicationKey(publication);
      const pubType = PUB_TYPE_MAP[key];

      if (!pubType) {
        return;
      }

      const titleElement =
        publication.querySelector(".title");

      if (!titleElement) {
        return;
      }

      const badge =
        document.createElement("span");

      badge.className = "pub-type-badge";
      badge.textContent = pubType;

      titleElement.appendChild(badge);
    });

    const filterBox =
      document.getElementById("topic-filter-box");

    let currentTopic = "all";
    let currentSearchQuery = "";

    function applyPublicationFilters() {
      publicationItems.forEach(function (publication) {
        const topics =
          publication.getAttribute("data-topics");

        const matchesTopic =
          currentTopic === "all" ||
          !topics ||
          topics.split(" ").indexOf(currentTopic) !== -1;

        const matchesSearch =
          currentSearchQuery === "" ||
          publication.textContent
            .toLowerCase()
            .indexOf(currentSearchQuery) !== -1;

        publication.style.display =
          matchesTopic && matchesSearch ? "" : "none";
      });
    }

    if (filterBox) {
      const filterButtons =
        filterBox.querySelectorAll(".topic-filter-item");

      filterButtons.forEach(function (button) {
        button.addEventListener("click", function () {
          currentTopic =
            button.getAttribute("data-topic");

          filterButtons.forEach(function (otherButton) {
            otherButton.classList.remove("active");
          });

          button.classList.add("active");

          applyPublicationFilters();
        });
      });
    }

    /* =======================================================
       BIBLIOGRAPHY SEARCH (custom, client-side)
       ======================================================= */

    const searchInput =
      document.getElementById("pub-search-input");

    if (searchInput) {
      searchInput.addEventListener("input", function () {
        currentSearchQuery =
          searchInput.value.toLowerCase().trim();

        applyPublicationFilters();
      });
    }
  });
</script>
