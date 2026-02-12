---
layout: page
title: Rules & Info
description: Underground RPG rules, Social Change mechanics, and power references
permalink: /info/
---

This page contains player-facing rules clarifications, cheat sheets, and game mechanics for the Housing Crisis campaign using Ray Winninger's Underground RPG.

## Core Resources

- **Underground RPG** – Original rulebook by Ray Winninger (Mayfair Games, 1993)
- **Social Change System** – Neighborhood improvement mechanics central to this campaign
- **Power Generation** – Slushie abilities and creative applications

## Quick Reference

Below are campaign-specific resources and rules clarifications, organized by topic.

{% assign groups = site.info | group_by: "topic" | sort_natural: "name" %}
{% for group in groups %}

  {% assign has_content = false %}
  {% for doc in group.items %}
  {% unless doc.tags contains "nested" %}
  {% assign has_content = true %}
  {% endunless %}
  {% endfor %}

  {% if has_content %}
  <h3>{{ group.name }}</h3>
  <ul>
  {% assign items = group.items | sort: "title" %}
  {% for doc in items %}
  {% unless doc.tags contains "nested" %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endunless %}
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

*New to Underground? The system emphasizes creative power usage, social consequences, and the collateral damage of superhuman violence in a dystopian world.*
