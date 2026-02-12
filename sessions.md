---
layout: page
title: Sessions
description: Chronicle of Paradise Heights transformation
permalink: /sessions/
---

# Session Summaries

This page chronicles the transformation of Paradise Heights, tracking victories, setbacks, and the community's journey from war zone to thriving neighborhood.

{% assign items = site.sessions | sort: 'index' %}

{% if items.size > 0 %}
<ul>
{% for doc in items %}
  <li><strong>Session {{ doc.index }}:</strong> <a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
<p><em>Sessions will be added as the campaign progresses.</em></p>
{% endif %}

---

## Paradise Heights

**Current Statistics**:

- **Safety:** TBD
- **Employment:** TBD  
- **Health:** TBD
- **Infrastructure:** TBD
- **Education:** TBD
- **Morale:** TBD
- **Crime:** TBD (lower is better)
- **Corruption:** TBD (lower is better)

**Quality of Life Score:** TBD out of 60

---

*The story of Paradise Heights is being written one session at a time.*
