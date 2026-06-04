---
layout: page
permalink: /publications/
title: research
description:
nav: true
nav_order: 2
---

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">Publications</h2>

{% bibliography --query @*[category=publications] --group_by none %}

<h2 class="bibliography">Working Papers</h2>

{% bibliography --query @*[category=working_papers] --group_by none %}

<h2 class="bibliography">Policy Work</h2>

{% bibliography --query @*[category=policy_work] --group_by none %}

</div>
