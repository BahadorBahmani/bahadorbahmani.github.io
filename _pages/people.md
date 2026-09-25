---
title: "People"
permalink: /people/
layout: archive
---

<!--
  ADDING A PHOTO
  --------------
  1. Save the image in /images/people/ (square crops around 400x400 px look best;
     they are cropped to a circle automatically).
  2. Replace the initials placeholder, e.g.

         <div class="person-photo">JH</div>

     with

         <div class="person-photo"><img src="/images/people/jinkyo-han.jpg" alt="Jinkyo Han"></div>

  Nothing else needs to change; the layout is the same either way.


-->

<style>
  .people-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(170px, 1fr));
    gap: 1.9em 1.4em;
    margin: 1.2em 0 2.6em;
  }
  .person {
    text-align: center;
  }
  .person-photo {
    width: 128px;
    height: 128px;
    margin: 0 auto 0.7em;
    border-radius: 50%;
    overflow: hidden;
    background: #eceff1;
    border: 1px solid #dde2e6;
    color: #8a9199;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2em;
    font-weight: 600;
    letter-spacing: 0.03em;
    user-select: none;
  }
  .person-photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center 22%;
    display: block;
  }
  .person-name {
    display: block;
    font-weight: 600;
    line-height: 1.3;
  }
  .person-detail {
    display: block;
    font-size: 0.82em;
    color: #6b7684;
    margin-top: 0.25em;
    line-height: 1.35;
  }
  .person-links {
    display: block;
    margin-top: 0.45em;
    font-size: 1.05em;
    line-height: 1;
  }
  .person-links a {
    display: inline-block;
    margin: 0 0.28em;
    color: #8a9199;
    text-decoration: none;
  }
  .person-links a:hover,
  .person-links a:focus { color: #52adc8; }
  @media (max-width: 480px) {
    .people-grid { grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); }
    .person-photo { width: 104px; height: 104px; font-size: 1.6em; }
  }
</style>

## Postdoctoral Researchers

<div class="people-grid">

  <div class="person">
    <div class="person-photo">SH</div>
    <span class="person-name">Sida Hao</span>
    <span class="person-detail">Ph.D., University of Texas at Austin</span>
    <span class="person-links">
      <a href="https://scholar.google.com/citations?user=lKo5_VkAAAAJ&amp;hl=en" title="Google Scholar" aria-label="Sida Hao on Google Scholar"><i class="ai ai-google-scholar" aria-hidden="true"></i></a>
      <a href="https://orcid.org/0000-0001-7264-1550" title="ORCID" aria-label="Sida Hao on ORCID"><i class="ai ai-orcid" aria-hidden="true"></i></a>
    </span>
  </div>

</div>

## Ph.D. Students

<div class="people-grid">

  <div class="person">
    <div class="person-photo">JH</div>
    <span class="person-name">Jinkyo Han</span>
    <span class="person-detail">B.S., Seoul National University</span>
    <span class="person-links">
      <a href="https://orcid.org/0009-0004-5056-3132" title="ORCID" aria-label="Jinkyo Han on ORCID"><i class="ai ai-orcid" aria-hidden="true"></i></a>
    </span>
  </div>

  <div class="person">
    <div class="person-photo">AM</div>
    <span class="person-name">Antoine Moats</span>
    <span class="person-detail">B.S., University of Southern California</span>
    <span class="person-links">
      <a href="https://orcid.org/0009-0008-1434-7028" title="ORCID" aria-label="Antoine Moats on ORCID"><i class="ai ai-orcid" aria-hidden="true"></i></a>
    </span>
  </div>

  <div class="person">
    <div class="person-photo">KB</div>
    <span class="person-name">Kyrillos Bastawros</span>
    <span class="person-detail">B.S., California Institute of Technology</span>
  </div>

</div>

<!--
  ALUMNI - uncomment when the first member moves on.

## Alumni

<div class="people-grid">

  <div class="person">
    <div class="person-photo">XY</div>
    <span class="person-name">Name</span>
    <span class="person-detail">Ph.D. 20XX &middot; now at Somewhere</span>
  </div>

</div>
-->
