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

  CLICK-TO-EXPAND CONTACT DETAILS
  -------------------------------
  Wrapping a name in <details class="person-more"> makes it clickable and
  reveals a contact list underneath (see the PI card). Names not wrapped this
  way stay plain text, so no one gets a clickable name with nothing behind it.
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
  /* A person whose name is wrapped in <details> becomes click-to-expand. */
  .person-more summary {
    display: block;
    cursor: pointer;
    list-style: none;
    outline-offset: 3px;
  }
  .person-more summary::-webkit-details-marker { display: none; }
  .person-more summary::marker { content: ""; }
  .person-more summary:hover .person-name { text-decoration: underline; }
  .person-more .person-name::after {
    content: " \25BE";
    font-size: 0.8em;
    color: #9aa2ab;
  }
  .person-more[open] .person-name::after { content: " \25B4"; }
  .person-contact {
    list-style: none;
    margin: 0.75em 0 0;
    padding: 0.75em 0 0;
    border-top: 1px solid #e5e9ec;
    font-size: 0.82em;
    line-height: 1.7;
    color: #6b7684;
  }
  .person-contact li { margin: 0; }
  @media (max-width: 480px) {
    .people-grid { grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); }
    .person-photo { width: 104px; height: 104px; font-size: 1.6em; }
  }
</style>

## Principal Investigator

<div class="people-grid">

  <div class="person">
    <div class="person-photo"><img src="/images/people/bahador-bahmani.jpg" alt="Bahador Bahmani"></div>
    <details class="person-more">
      <summary>
        <span class="person-name">Bahador Bahmani</span>
        <span class="person-detail">Assistant Professor of Mechanical Engineering</span>
      </summary>
      <ul class="person-contact">
        <li>{{ site.author.employer }}</li>
        <li>{{ site.author.office }}</li>
        <li>{{ site.author.location }}</li>
        <li><a href="mailto:{{ site.author.email }}">Email</a></li>
        <li><a href="{{ site.author.googlescholar }}">Google Scholar</a></li>
        <li><a href="{{ site.author.orcid }}">ORCID</a></li>
        <li><a href="{{ site.author.researchgate }}">ResearchGate</a></li>
        <li><a href="https://www.linkedin.com/in/{{ site.author.linkedin }}">LinkedIn</a></li>
      </ul>
    </details>
  </div>

</div>

## Postdoctoral Researchers

<div class="people-grid">

  <div class="person">
    <div class="person-photo">SH</div>
    <span class="person-name">Sida Hao</span>
    <span class="person-detail">Ph.D., University of Texas at Austin</span>
  </div>

</div>

## Ph.D. Students

<div class="people-grid">

  <div class="person">
    <div class="person-photo">JH</div>
    <span class="person-name">Jinkyo Han</span>
    <span class="person-detail">B.S., Seoul National University</span>
  </div>

  <div class="person">
    <div class="person-photo">AM</div>
    <span class="person-name">Antoine Moats</span>
    <span class="person-detail">B.S., University of Southern California</span>
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
