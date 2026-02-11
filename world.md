---
layout: page
title: World
description: Setting, characters, locations, and mysteries revealed during play
permalink: /world/
---

This page contains all player-facing information about the world of Autumn Hollow – the town, its inhabitants, key locations, and the cosmic mysteries lurking beneath the surface.

Information is added here as it's discovered during the campaign, loop by loop.

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

## About Autumn Hollow

Autumn Hollow is a small Indiana town frozen in October 31st, 1986. Population: 3,847. Main Street has a hardware store, diner, movie theater, and arcade. Most families have lived here for generations. Everyone knows everyone.

But something happened three nights ago. Or maybe it was three hundred nights ago—time doesn't work right anymore. The loop resets at midnight. Most people don't notice. But you do.

And in the woods at the edge of town, something ancient is stirring.

---

*This section grows as you explore the town and uncover its secrets, loop by loop.*
