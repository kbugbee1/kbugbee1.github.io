---
layout: default
title: About
permalink: /about/
---

<style>
/* About page only — no changes to the site's shared stylesheet needed. */
.about-page { padding-top: 56px; padding-bottom: 75px; }
.about-page .about-eyebrow { color: #668398; text-transform: uppercase; font-size: 11px; letter-spacing: .18em; font-weight: 700; margin: 0 0 22px; }
.about-page .about-intro { display: grid; grid-template-columns: minmax(0, 1.5fr) minmax(220px, .8fr); gap: 45px; align-items: center; padding-bottom: 55px; border-bottom: 1px solid #dddcd4; }
.about-page .about-title { font-family: Georgia, 'Times New Roman', serif; font-size: clamp(39px, 5.2vw, 66px); font-weight: 400; line-height: 1.08; letter-spacing: -.035em; color: #233d50; margin: 0 0 22px; }
.about-page .about-deck { font-size: clamp(17px, 1.8vw, 20px); line-height: 1.7; color: #536777; max-width: 650px; margin: 0; }
.about-page .about-orbit { position: relative; min-height: 290px; display: flex; align-items: center; justify-content: center; }
.about-page .about-orbit img { width: 100%; max-width: 330px; opacity: .75; }
.about-page .about-section { display: grid; grid-template-columns: minmax(150px, .45fr) minmax(0, 1.5fr); gap: 36px; padding: 43px 0; border-bottom: 1px solid #dddcd4; }
.about-page .about-section h2 { font-family: Georgia, 'Times New Roman', serif; font-size: 27px; font-weight: 400; color: #233d50; line-height: 1.25; margin: 0; }
.about-page .about-section p { color: #425a6b; line-height: 1.85; margin: 0 0 16px; }
.about-page .about-section p:last-child { margin-bottom: 0; }
.about-page .about-highlight { background: #efeee7; border-left: 2px solid #b79d75; padding: 24px 27px; margin: 22px 0; }
.about-page .about-highlight p { font-family: Georgia, 'Times New Roman', serif; font-size: 20px; line-height: 1.6; color: #28475a; margin: 0; }
.about-page .about-tags { display: flex; flex-wrap: wrap; gap: 9px; margin: 20px 0 0; }
.about-page .about-tag { border: 1px solid #c9d0d0; border-radius: 100px; padding: 7px 12px; font-size: 12px; color: #4a6879; }
.about-page .about-links { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 26px; }
.about-page .about-links a { display: inline-block; text-decoration: none; color: #244a61; border-bottom: 1px solid #b6a47f; padding: 5px 0; margin-right: 14px; font-weight: 600; }
.about-page .about-note { font-size: 13px; color: #657683; line-height: 1.7; }
@media (max-width: 760px) {
  .about-page { padding-top: 35px; }
  .about-page .about-intro { grid-template-columns: 1fr; gap: 5px; padding-bottom: 35px; }
  .about-page .about-orbit { min-height: 190px; }
  .about-page .about-orbit img { max-width: 230px; }
  .about-page .about-section { grid-template-columns: 1fr; gap: 15px; padding: 32px 0; }
}
</style>

<div class="wrap about-page">
  <section class="about-intro" aria-labelledby="about-heading">
    <div>
      <p class="about-eyebrow">About · Scientific informatics · Open science</p>
      <h1 id="about-heading" class="about-title">The human side of scientific discovery.</h1>
      <p class="about-deck">I'm interested in what happens to scientific knowledge after the moment of discovery: how we preserve it, make sense of it, connect it to new questions, and carry it forward.</p>
    </div>
    <div class="about-orbit" aria-hidden="true">
      <img src="{{ '/assets/images/orbit-archive.svg' | relative_url }}" alt="">
    </div>
  </section>

  <section class="about-section" aria-labelledby="work-heading">
    <h2 id="work-heading">My work</h2>
    <div>
      <p>I'm a scientific informatics and data stewardship professional working at NASA's Marshall Space Flight Center. My work focuses on the systems, practices, and collaborations that help scientists discover, understand, share, and reuse research data and other scientific outputs.</p>
      <p>Across initiatives in open science, scientific information discovery, research repositories, and data governance, I've worked to connect technical capabilities with the needs of researchers and the responsibilities of long-term stewardship.</p>
      <div class="about-tags" aria-label="Areas of focus">
        <span class="about-tag">Scientific informatics</span>
        <span class="about-tag">Data stewardship</span>
        <span class="about-tag">Open science</span>
        <span class="about-tag">Information discovery</span>
        <span class="about-tag">Data governance</span>
      </div>
    </div>
  </section>

  <section class="about-section" aria-labelledby="perspective-heading">
    <h2 id="perspective-heading">What drives me</h2>
    <div>
      <p>Scientific discovery is often told through missions, instruments, and breakthroughs. I'm equally interested in the work that makes those breakthroughs possible: documenting context, preserving evidence, building connections across disciplines, and ensuring that knowledge can be interpreted by people who weren't there when it was created.</p>
      <div class="about-highlight"><p>Scientific data have a history, a context, and a future. Informatics helps connect all three.</p></div>
      <p>I believe scientific informatics deserves recognition not simply as technical support, but as a discipline that shapes what researchers can discover—and what future generations can learn from today's science.</p>
    </div>
  </section>

  <section class="about-section" aria-labelledby="explore-heading">
    <h2 id="explore-heading">Explore further</h2>
    <div>
      <p>This site is a place for independent writing, research perspectives, historical reflections, and conversations about the future of scientific informatics.</p>
      <nav class="about-links" aria-label="Explore more of this site">
        <a href="{{ '/publications/' | relative_url }}">Talks &amp; Publications ↗</a>
        <a href="{{ '/writing/' | relative_url }}">Writing ↗</a>
        <a href="{{ '/cv/' | relative_url }}">CV ↗</a>
        <a href="https://orcid.org/0000-0001-6733-5698" rel="me noopener noreferrer" target="_blank">ORCID ↗</a>
      </nav>
    </div>
  </section>

  <section class="about-section" id="disclaimer" aria-labelledby="disclaimer-heading">
    <h2 id="disclaimer-heading">About this site</h2>
    <div>
      <p class="about-note">This is an independent personal website. The views and opinions expressed here are my own and do not necessarily reflect those of NASA, the U.S. Government, or any organization with which I am affiliated. Content is shared in my personal capacity and does not represent official agency policy or endorsement.</p>
      <p class="about-note">This is not an official NASA website. References to professional affiliations are provided for biographical context only.</p>
    </div>
  </section>
</div>
