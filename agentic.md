---
layout: default
title: Agentic AI Repositories
---

# Agentic AI repositories

<table>
  <thead>
    <tr>
      <th>GitHub Repository</th>
      <th>Way of Extraction</th>
      <th>Paper (If it exists)</th>
      <th>Patterns Detected</th>
    </tr>
  </thead>
  <tbody>
  {% for item in site.data.agentic %}
    {% assign parts = item.repo | split: "/" %}
    <tr>
      <td><a href="{{ item.repo }}">{{ parts[3] }}/{{ parts[4] }}</a></td>
      <td>{{ item.extraction }}</td>
      <td>{% if item.paper and item.paper != "" %}<a href="{{ item.paper }}">paper</a>{% else %}-{% endif %}</td>
      <td>{% if item.patterns %}{{ item.patterns | join: ", " }}{% else %}-{% endif %}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
