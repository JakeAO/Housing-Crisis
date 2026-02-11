---
layout: page
title: Rules & Info
description: Kids On Bikes rules, mechanics, and cheat sheets
permalink: /info/
---

This page contains player-facing rules clarifications, cheat sheets, and game mechanics for the Autumn Hollow campaign.

## Core Resources

- **[Kids On Bikes Official Site](https://www.huntersentertainment.com/kids-on-bikes)** – Publisher's home page
- **[Kids On Bikes on DriveThruRPG](https://www.drivethrurpg.com/product/231938/Kids-on-Bikes)** – Digital rulebook
- **[Character Sheets](https://www.huntersentertainment.com/character-sheets)** – Official downloadable sheets

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

*New to Kids On Bikes? The system is designed to be easy to learn—you can start playing with just the Quick Reference sheet above!*
