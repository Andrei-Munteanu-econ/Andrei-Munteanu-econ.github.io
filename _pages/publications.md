---
layout: page
permalink: /publications/
title: research
description:
nav: true
nav_order: 2
---

<style>
  /* AEA-style hanging-indent references */
  .publications ol.bibliography > li { margin-bottom: 1rem; }
  .publications .row { display: block; margin: 0; }
  .publications .econ-ref { padding-left: 2em; text-indent: -2em; line-height: 1.55; }
  .publications .econ-ref .links { text-indent: 0; }
  .publications .econ-ref .links a.btn { text-indent: 0; }
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
