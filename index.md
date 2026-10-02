---
layout: default
title: "Home"
permalink: /
author_profile: true
---

<style>
  .homepage-nav {
    position: sticky;
    top: 0;
    background-color: white;
    border-bottom: 1px solid #e0e0e0;
    padding: 12px 0;
    margin-bottom: 30px;
    z-index: 100;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
  }
  
  .homepage-nav ul {
    list-style: none;
    margin: 0;
    padding: 0 20px;
    display: flex;
    gap: 30px;
  }
  
  .homepage-nav li {
    margin: 0;
  }
  
  .homepage-nav a {
    display: inline-block;
    color: #0066cc;
    text-decoration: none;
    font-size: 1.1em;
    font-weight: 500;
    padding: 5px 0;
    border-bottom: 3px solid transparent;
    transition: all 0.2s;
  }
  
  .homepage-nav a:hover {
    color: #0052a3;
    border-bottom-color: #0066cc;
  }
  
  html {
    scroll-behavior: smooth;
  }
  
  .section {
    scroll-margin-top: 100px;
    margin-bottom: 60px;
  }
  
  .section h2 {
    border-bottom: 2px solid #0066cc;
    padding-bottom: 10px;
    margin-bottom: 30px;
  }
</style>

<nav class="homepage-nav">
  <ul>
    <li><a href="#research">Research</a></li>
    <li><a href="#talks">Talks</a></li>
    <li><a href="#teaching">Teaching</a></li>
    <li><a href="#conferences">Conferences</a></li>
  </ul>
</nav>

<div id="main" role="main">
  {% include sidebar.html %}

  <article class="page">
    <div class="page__inner-wrap">
      <section class="page__content">

<!-- RESEARCH SECTION -->
<div class="section" id="research">
<h2>Research</h2>

<p>My research interests include differential geometry, geometric flows, and Spin(7)-structures.</p>

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

</div>

<!-- TALKS SECTION -->
<div class="section" id="talks">
<h2>Talks</h2>

{% for post in site.talks reversed %}
  {% include archive-single.html %}
{% endfor %}

</div>

<!-- TEACHING SECTION -->
<div class="section" id="teaching">
<h2>Teaching</h2>

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}

</div>

<!-- CONFERENCES SECTION -->
<div class="section" id="conferences">
<h2>Conferences</h2>

<p>Below is a list of conferences I have attended:</p>

{% for conference in site.data.conferences %}
<div style="margin-bottom: 30px;">
  <h3>{{ conference.title }}</h3>
  <p><strong>{{ conference.date }}</strong> • {{ conference.location }} • {{ conference.venue }}</p>
  {% if conference.description %}<p>{{ conference.description }}</p>{% endif %}
</div>
{% endfor %}

</div>

      </section>
    </div>
  </article>
</div>
