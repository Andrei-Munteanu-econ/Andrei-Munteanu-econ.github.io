---
layout: page
permalink: /publications/
title: research
description:
nav: true
nav_order: 2
---

<style>
  /* ---------------------------------------------------------------------
     Publication list — "academic site" layout (see _layouts/bib.liquid).
     Colours come from al_folio_core's --global-* variables so light/dark
     mode both work without a second ruleset.
     --------------------------------------------------------------------- */

  .publications ol.bibliography { padding-left: 0; }
  .publications ol.bibliography > li { margin-bottom: 1.6rem; list-style: none; }
  .publications .row { display: block; margin: 0; }

  .publications h2.bibliography {
    margin: 2.2rem 0 1.2rem;
    padding-bottom: 0.35rem;
    border-bottom: 1px solid var(--global-divider-color);
    font-size: 1.1rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--global-text-color-light);
  }

  /* ---- entry grid: chip gutter + body ---- */
  .publications .pub-entry {
    display: grid;
    grid-template-columns: 5.5rem 1fr;
    column-gap: 1rem;
    padding: 0;
  }

  .publications .pub-chip-col { padding-top: 0.15rem; }

  .publications .pub-chip {
    display: inline-block;
    width: 100%;
    padding: 0.3rem 0.2rem;
    border-radius: 4px;
    background-color: var(--global-theme-color);
    color: #fff;
    font-size: 0.7rem;
    font-weight: 700;
    line-height: 1.2;
    text-align: center;
    letter-spacing: 0.02em;
    word-break: break-word;
  }

  /* ---- body lines ---- */
  .publications .pub-title {
    margin-bottom: 0.18rem;
    font-size: 1.06rem;
    font-weight: 700;
    line-height: 1.35;
    color: var(--global-text-color);
  }

  .publications .pub-authors {
    font-size: 0.92rem;
    line-height: 1.45;
    color: var(--global-text-color-light);
  }

  .publications .pub-self {
    font-weight: 700;
    color: var(--global-text-color);
  }

  .publications .pub-year::before {
    content: " · ";
    color: var(--global-divider-color);
  }

  .publications .pub-venue {
    margin-top: 0.1rem;
    font-size: 0.92rem;
    line-height: 1.45;
    color: var(--global-text-color-light);
  }

  .publications .pub-venue em {
    font-style: italic;
    color: var(--global-text-color);
  }

  /* ---- status pill ---- */
  .publications .pub-meta {
    margin-top: 0.4rem;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.5rem;
    font-size: 0.82rem;
    color: var(--global-text-color-light);
  }

  .publications .pub-status {
    display: inline-block;
    padding: 0.1rem 0.5rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 999px;
    font-size: 0.74rem;
    font-weight: 600;
    letter-spacing: 0.02em;
    text-transform: uppercase;
    white-space: nowrap;
    color: var(--global-text-color-light);
  }

  .publications .pub-status--conditionally-accepted {
    border-color: var(--global-theme-color);
    background-color: var(--global-theme-color);
    color: #fff;
  }

  /* ---- link buttons ---- */
  .publications .links { display: inline-block; margin-top: 0.5rem; }
  .publications .links .btn { margin-right: 0.3rem; }

  /* ---- narrow screens: chip moves above the title ---- */
  @media (max-width: 576px) {
    .publications .pub-entry {
      grid-template-columns: 1fr;
      row-gap: 0.4rem;
    }
    .publications .pub-chip { width: auto; padding: 0.2rem 0.55rem; }
  }
</style>

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">Publications</h2>

{% bibliography --query @*[category=publications] --group_by none %}

<h2 class="bibliography">Working Papers</h2>

{% bibliography --query @*[category=working_papers] --group_by none %}

<h2 class="bibliography">Policy Work</h2>

{% bibliography --query @*[category=policy_work] --group_by none %}

</div>
