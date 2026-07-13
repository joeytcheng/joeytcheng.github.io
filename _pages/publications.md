---
layout: page
permalink: /publications/
title: Publications
description: Articles and book chapters by year of publication
nav: true
nav_order: 4
---

<!-- _pages/publications.md -->

<style>
  /* =========================================================
     PUBLICATIONS PAGE
     ========================================================= */

  .publications {
    margin-top: 1.5rem;
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
    margin: 0;
    padding: 1.7rem 0 2rem;
    border-bottom: 1px solid var(--global-divider-color);
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
    margin: 0 0 0.35rem;
    color: var(--global-text-color-light);
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.25;
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
    color: var(--global-text-color);
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

  /* =========================================================
     STATIC OVERVIEW BOX
     ========================================================= */

  /*
   * The abstract field from the .bib file is always visible
   * as a lightly shaded overview box.
   */

  .publications div.abstract,
  .publications div.abstract.hidden,
  .publications .publication-overview {
    display: block !important;
    width: 100%;
    margin: 0.95rem 0 0.85rem;
    padding: 0.9rem 1rem;

    border: 1px solid var(--global-divider-color);
    border-left: 3px solid var(--global-theme-color);
    border-radius: 5px;

    background-color: var(--global-code-bg-color);
    color: var(--global-text-color-light);

    font-size: 0.94rem;
    font-weight: 400;
    line-height: 1.65;
  }

  /*
   * Small Overview label within the box.
   */

  .publications div.abstract::before,
  .publications .publication-overview::before {
    content: "Overview";
    display: block;
    margin-bottom: 0.35rem;

    color: var(--global-text-color-light);
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.06em;
    line-height: 1.2;
    text-transform: uppercase;

    opacity: 0.8;
  }

  .publications div.abstract p,
  .publications .publication-overview p {
    margin-top: 0;
    margin-bottom: 0.7rem;
    color: inherit;
  }

  .publications div.abstract p:last-child,
  .publications .publication-overview p:last-child {
    margin-bottom: 0;
  }

  /* =========================================================
     PUBLICATION BUTTONS
     ========================================================= */

  .publications .links {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.45rem;
    margin-top: 0.75rem;
  }

  /*
   * Hide the old Abstract or Overview button because the
   * overview is permanently visible.
   */

  .publications .links .abstract,
  .publications .links a.abstract,
  .publications .links button.abstract {
    display: none !important;
  }

  /* URL, PDF, Code, Data, and other buttons */

  .publications .links a.btn,
  .publications .links button.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;

    min-height: 2rem;
    margin: 0;
    padding: 0.35rem 0.72rem;

    border: 1px solid var(--global-divider-color);
    border-radius: 5px;

    background-color: transparent;
    box-shadow: none;

    color: var(--global-theme-color);
    font-family: inherit;
    font-size: 0.88rem;
    font-weight: 500;
    line-height: 1.25;
    text-transform: none;

    cursor: pointer;

    transition:
      border-color 0.2s ease,
      background-color 0.2s ease,
      color 0.2s ease;
  }

  .publications .links a.btn:hover,
  .publications .links a.btn:focus,
  .publications .links button.btn:hover,
  .publications .links button.btn:focus {
    border-color: var(--global-theme-color);
    background-color: var(--global-code-bg-color);
    color: var(--global-theme-color);
    text-decoration: none;
    outline: none;
  }

  /* BibTeX dropdown */

  .publications div.bibtex {
    margin-top: 1rem;
  }

  /* Search box */

  #bibsearch {
    margin-bottom: 1.5rem;
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
      padding: 0.8rem 0.9rem;
      font-size: 0.91rem;
      line-height: 1.6;
    }
  }
</style>

<!-- Bibliography search feature -->

{% include bib_search.liquid %}

<div class="publications">

  {% bibliography %}

</div>

<div class="reading-list-section">

## Books that I am reading, have read, or will read

- *The Psychology of Social Status*
- *Gender*
- *Current Opinion in Psychology*

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
       ======================================================= */

    const yearHeadings =
      publicationsContainer.querySelectorAll(
        "h2.bibliography"
      );

    yearHeadings.forEach(function (yearHeading) {
      /*
       * Extract only a four-digit year from the heading.
       */

      const headingText =
        yearHeading.textContent.trim();

      const yearMatch =
        headingText.match(/\b(?:19|20)\d{2}\b/);

      if (!yearMatch) {
        return;
      }

      const yearText = yearMatch[0];

      let publicationsList =
        yearHeading.nextElementSibling;

      /*
       * Find the bibliography list following this year
       * heading.
       */

      while (
        publicationsList &&
        !publicationsList.matches("ol.bibliography")
      ) {
        publicationsList =
          publicationsList.nextElementSibling;
      }

      if (!publicationsList) {
        return;
      }

      const publicationsForYear =
        publicationsList.querySelectorAll(
          ":scope > li"
        );

      publicationsForYear.forEach(function (publication) {
        /*
         * Avoid inserting the year more than once.
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

        const yearElement =
          document.createElement("div");

        yearElement.className =
          "publication-year-above-title";

        yearElement.textContent = yearText;

        title.insertAdjacentElement(
          "beforebegin",
          yearElement
        );
      });
    });

    const publicationItems =
      publicationsContainer.querySelectorAll(
        "ol.bibliography > li"
      );

    publicationItems.forEach(function (publication) {
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
              /(?:\s*[,.;]\s*|\s+)\(?(?:19|20)\d{2}\)?[.,;]?\s*$/,
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

      /* =====================================================
         DISPLAY THE OVERVIEW PERMANENTLY
         ===================================================== */

      const overviewContent =
        publication.querySelector(
          "div.abstract"
        );

      const overviewButton =
        publication.querySelector(
          ".links a.abstract, .links button.abstract"
        );

      if (overviewButton) {
        overviewButton.remove();
      }

      if (overviewContent) {
        overviewContent.classList.remove(
          "hidden",
          "overview-visible"
        );

        overviewContent.classList.add(
          "publication-overview"
        );

        overviewContent.removeAttribute(
          "hidden"
        );

        overviewContent.removeAttribute(
          "aria-hidden"
        );

        const links =
          publication.querySelector(
            ".links"
          );

        /*
         * Place the overview beneath the journal information
         * and above the publication links.
         */

        if (periodical) {
          periodical.insertAdjacentElement(
            "afterend",
            overviewContent
          );
        } else if (links) {
          links.insertAdjacentElement(
            "beforebegin",
            overviewContent
          );
        }
      }

      /* =====================================================
         RELABEL PUBLICATION BUTTONS
         ===================================================== */

      const publicationButtons =
        publication.querySelectorAll(
          ".links a.btn, .links button.btn"
        );

      publicationButtons.forEach(function (button) {
        const originalLabel =
          button.textContent
            .trim()
            .toLowerCase();

        /*
         * Change HTML to URL.
         */

        if (
          originalLabel === "html" ||
          button.classList.contains("html") ||
          button.getAttribute("data-type") === "html"
        ) {
          button.textContent = "URL";

          button.setAttribute(
            "aria-label",
            "Open publication URL"
          );
        }

        /*
         * Change Website to Data.
         */

        if (originalLabel === "website") {
          button.textContent = "Data";

          button.setAttribute(
            "aria-label",
            "View data"
          );
        }

        /*
         * Remove any remaining Abstract or Overview button.
         */

        if (
          originalLabel === "abstract" ||
          originalLabel === "overview"
        ) {
          button.remove();
        }
      });
    });
  });
</script>