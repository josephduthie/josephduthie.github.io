---
layout: archive
title: "Conferences attended"
permalink: /conferences/
author_profile: true
---

<p>Below is a template for listing conferences I have attended.</p>

{% if site.data.conferences %}
  {% for conference in site.data.conferences %}
    <div class="conference-entry" style="margin-bottom: 1.5rem;">
      <h3>
        {% if conference.url %}
          <a href="{{ conference.url }}">{{ conference.title }}</a>
        {% else %}
          {{ conference.title }}
        {% endif %}
      </h3>
      <p>
        <strong>{{ conference.date }}</strong>
        {% if conference.location %}
          • {{ conference.location }}
        {% endif %}
        {% if conference.venue %}
          • {{ conference.venue }}
        {% endif %}
      </p>
      {% if conference.description %}
        <p>{{ conference.description }}</p>
      {% endif %}
    </div>
  {% endfor %}
{% else %}
  <p>No conference entries have been added yet.</p>
{% endif %}
