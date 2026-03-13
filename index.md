---
layout: default
title: Viewpoints
permalink: /
---

<p class="page-intro">
  Concise viewpoint papers: focused arguments, explicit assumptions, and references when needed.
  This is intentionally lighter than formal review papers.
</p>

{% assign notes = site.topics | where_exp: "n", "n.status != 'draft'" | sort: "date" | reverse %}

{% if notes.size > 0 %}
<ul class="topic-list">
  {% for note in notes %}
    {% assign stamp = note.updated | default: note.date %}
    <li class="topic-card">
      <h2><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h2>
      <p class="meta">{{ note.topic }} · Updated {{ stamp | date: "%Y-%m-%d" }}</p>
      <p>{{ note.summary }}</p>
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty">No published viewpoint yet. Add one file to <code>_topics/</code>.</p>
{% endif %}

