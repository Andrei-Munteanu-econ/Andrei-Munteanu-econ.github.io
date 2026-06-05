---
layout: page
title: About me
permalink: /
---

<div class="about-grid">

<div class="about-side">
<img src="{{ '/assets/img/profile_pic.jpg' | relative_url }}" alt="Andrei Munteanu" class="about-photo img-fluid z-depth-1 rounded" loading="eager">
<h2 class="about-name">Andrei Munteanu</h2>
<p class="about-affil">Department of Economics<br>Université du Québec à Montréal</p>
</div>

<div class="about-main">
<h2 class="about-heading">About me</h2>
<p class="about-bio">I am an Assistant Professor of Economics at the <a href="https://uqam.ca" target="_blank" rel="noopener">Université du Québec à Montréal (UQAM)</a>. I am an applied microeconomist interested in the <strong>economics of education, inequality, and labor</strong>.</p>
<p class="about-bio">I am also the Academic Director of the CIQSS-UQAM-INRS Research Data Center.</p>
<p class="about-cv">You can find my CV <a href="{{ '/assets/pdf/cv.pdf' | relative_url }}" target="_blank" rel="noopener">here</a>.</p>
<p class="about-contact"><span class="about-contact-label">Contact:</span> <a href="mailto:munteanu.andrei@uqam.ca">munteanu.andrei@uqam.ca</a><button type="button" class="copy-email" data-email="munteanu.andrei@uqam.ca" aria-label="Copy email address">Copy</button></p>
<div class="social"><div class="contact-icons"><a href="mailto:munteanu.andrei@uqam.ca" title="Email"><i class="fa-solid fa-envelope"></i></a><a href="https://scholar.google.com/citations?user=yEWUz3cAAAAJ" title="Google Scholar" target="_blank" rel="noopener"><i class="ai ai-google-scholar"></i></a><a href="https://orcid.org/0000-0003-3235-7437" title="ORCID" target="_blank" rel="noopener"><i class="ai ai-orcid"></i></a><a href="https://twitter.com/andrei_mntn" title="X (Twitter)" target="_blank" rel="noopener"><i class="fa-brands fa-x-twitter"></i></a><a href="https://bsky.app/profile/andrei-econ.bsky.social" title="Bluesky" target="_blank" rel="noopener"><i class="fa-brands fa-bluesky"></i></a><a href="https://www.linkedin.com/in/andreimunteanu1" title="LinkedIn" target="_blank" rel="noopener"><i class="fa-brands fa-linkedin"></i></a><a href="https://github.com/andrei-munteanu-econ" title="GitHub" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i></a></div></div>
</div>

</div>

<style>
  /* Homepage "About me" — two-column layout: photo + name + affiliation on the LEFT,
     "About me" heading + intro + CV + contact + socials on the RIGHT. This <style> only
     loads on the homepage, so selectors targeting gem elements (.post-header) are
     effectively scoped to "/". */

  /* Hide the page layout's top title; "About me" now lives in the text column instead */
  .post-header { display: none; }

  .about-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    align-items: flex-start;
    margin-top: 1rem;
  }
  .about-side { flex: 0 0 250px; text-align: center; } /* photo column, on the left */
  .about-main { flex: 1 1 340px; min-width: 16rem; }   /* text column, on the right */

  /* Rounded-rectangle profile photo (not circular) */
  .about-photo {
    display: block;
    width: 100%;
    max-width: 220px;
    height: auto;
    margin: 0 auto 1rem;
  }

  .about-name  { font-size: 1.7rem; font-weight: 700; margin: 0.25rem 0 0.15rem; line-height: 1.2; }
  .about-affil { margin: 0; line-height: 1.45; opacity: 0.85; font-size: 0.95rem; }

  .about-heading { text-align: left; font-size: 1.6rem; font-weight: 700; }
  .about-bio,
  .about-cv,
  .about-contact { text-align: left; }
  .about-contact-label { font-weight: 600; margin-right: 0.25rem; }

  /* Consistent vertical spacing between every block in the text column */
  .about-main > *            { margin-top: 0; margin-bottom: 1.25rem; }
  .about-main > *:last-child { margin-bottom: 0; }

  /* Email "Copy" button */
  .copy-email {
    margin-left: 0.5rem;
    padding: 0.12rem 0.55rem;
    font-size: 0.75rem;
    line-height: 1.4;
    color: inherit;
    background: transparent;
    border: 1px solid var(--global-divider-color, #ccc);
    border-radius: 0.3rem;
    cursor: pointer;
    vertical-align: middle;
  }
  .copy-email:hover { color: var(--global-theme-color); border-color: var(--global-theme-color); }

  /* Social icons row (left-aligned in the text column); even spacing via flex gap */
  .social .contact-icons {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
    align-items: center;
    gap: 0.65rem;
    font-size: 1.6rem;
  }
  .social .contact-icons a i.fa-envelope::before       { color: #ea4335; } /* email red     */
  .social .contact-icons a i.fa-linkedin::before       { color: #0a66c2; } /* LinkedIn blue */
  .social .contact-icons a i.fa-bluesky::before        { color: #1185fe; } /* Bluesky blue  */
  .social .contact-icons a i.ai-google-scholar::before { color: #4285f4; } /* Scholar blue  */
  .social .contact-icons a i.ai-orcid::before          { color: #a6ce39; } /* ORCID green   */
  /* X and GitHub inherit var(--global-text-color) so they stay visible in dark mode */
  .social .contact-icons a:hover { opacity: 0.75; transition: opacity 0.2s ease-in-out; }

  /* On narrow screens, the columns stack (photo + name on top) */
  @media (max-width: 576px) {
    .about-side { flex-basis: 100%; }
  }
</style>

<script>
  document.querySelectorAll('.copy-email').forEach(function (btn) {
    btn.addEventListener('click', function () {
      navigator.clipboard.writeText(btn.dataset.email).then(function () {
        var prev = btn.textContent;
        btn.textContent = 'Copied!';
        setTimeout(function () { btn.textContent = prev; }, 1500);
      });
    });
  });
</script>
