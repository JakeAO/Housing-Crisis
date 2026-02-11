---
layout: page
title: Sessions
description: Session summaries and loop chronicle
permalink: /sessions/
---

Below are session summaries documenting your journey through the loops of Autumn Hollow, ordered chronologically.

{% assign items = site.sessions | sort: 'index' %}

{% if items.size > 0 %}
<ul>
{% for doc in items %}
  <li><strong>Session {{ doc.index }}:</strong> <a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
<p><em>No sessions have been recorded yet. The first loop begins soon!</em></p>
{% endif %}

---

*Summaries are added after each session to track your progress, discoveries, and theories about breaking the loop.*
