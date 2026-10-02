---
layout: single
title: "Conferences Attended"
permalink: /conferences/
author_profile: true
---

Below is a list of conferences I have attended:

{% for conference in site.data.conferences %}

### {{ conference.title }}

**{{ conference.date }}** • {{ conference.location }} • {{ conference.venue }}

{{ conference.description }}

---

{% endfor %}
