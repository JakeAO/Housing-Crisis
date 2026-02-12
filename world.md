---
layout: page
title: World
description: Neo-L.A., Slushies, corporations, factions, and life in the dystopia
permalink: /world/
---

This page contains all player-facing information about the world of Housing Crisis – Neo-L.A., the super-soldier program, corporations and gangs, and the satirical dystopian setting of Underground.

Information is added here as it's discovered during the campaign, session by session.

{% assign groups = site.world | group_by: "topic" | sort: 'name' %}
{% for group in groups %}

  {% if group.items.size > 0 %}
  <h2>{{ group.name }}</h2>
  <ul>
  {% assign items = group.items | sort: 'title' %}
  {% for doc in items %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

## About Paradise Heights

Paradise Heights is your new home—a crumbling 40-story housing project in the worst part of Neo-L.A. (formerly Los Angeles). It was supposed to be "Veteran's Paradise," a luxury complex for super-soldier veterans. Instead, it's a war zone.

The government lied. The elevators barely work. The water's contaminated. Corporate-sponsored gangs control the ground floor. Rent-A-Cops extort residents. The "state-of-the-art facilities" are either broken or nonexistent.

Most residents are desperate, traumatized, or both. Crime is rampant. Infrastructure is failing. The corporations that technically own the land don't care—Paradise Heights is a tax write-off.

But you're Slushies. You didn't survive genetic engineering, combat conditioning, and secret wars to live like this. You're going to fix this place. One block at a time. Whatever it takes.

---

*This section grows as you explore Neo-L.A. and uncover the depth of corporate control, session by session.*
