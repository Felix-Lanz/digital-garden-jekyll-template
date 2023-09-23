---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

### Führen im Team

[[fit_index]]

### ITSec

[[Kontrollfragen Lektion 1]]
[[Kontrollfragen Lektion 2]]
[[Kontrollfragen Lektion 3]]


### Projektmanagment

[[Projektmanagment]]

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
