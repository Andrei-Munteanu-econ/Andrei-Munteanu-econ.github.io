---
layout: about
title: about
permalink: /

profile:
  align: right
  image: profile_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Department of Economics</p>
    <p>Université du Québec à Montréal</p>

selected_papers: false
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false

latest_posts:
  enabled: false
---

I am an Assistant Professor of Economics at the [Université du Québec à Montréal (UQAM)](https://uqam.ca), and Academic Director of the CIQSS-UQAM-INRS Research Data Center. I am an applied microeconomist interested in the economics of education, inequality, and labor.

<style>
  /* Size + even spacing for the homepage social icons. The gem ships a huge 4rem
     container whose inter-icon whitespace scales with it (oversized, and uneven because
     academicons vs FontAwesome glyphs differ in width). Flexbox `gap` removes the
     whitespace entirely so spacing is uniform; tweak gap/font-size below to taste. */
  .social .contact-icons {
    display: flex;
    flex-wrap: wrap;
    justify-content: center; /* matches the gem's .social { text-align: center } */
    align-items: center;
    gap: 0.6rem;             /* spacing between icons */
    font-size: 1.6rem;       /* icon size */
  }
  /* Brand-color the homepage social icons (dark-mode-safe: black/white brands omitted) */
  .social .contact-icons a i.fa-linkedin::before       { color: #0a66c2; } /* LinkedIn blue */
  .social .contact-icons a i.fa-bluesky::before        { color: #1185fe; } /* Bluesky blue  */
  .social .contact-icons a i.ai-google-scholar::before { color: #4285f4; } /* Scholar blue  */
  .social .contact-icons a i.ai-orcid::before          { color: #a6ce39; } /* ORCID green   */
  .social .contact-icons a i.fa-envelope::before       { color: #ea4335; } /* email red     */
  /* GitHub, X, and CV inherit var(--global-text-color) so they stay visible in dark mode */
  .social .contact-icons a:hover { opacity: 0.75; transition: opacity 0.2s ease-in-out; }
</style>
