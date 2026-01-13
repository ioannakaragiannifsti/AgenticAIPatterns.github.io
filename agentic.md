---
layout: default
title: Agentic AI Repositories
---

# Agentic AI repositories

| GitHub Repository Link | Way of Extraction | Paper (If it exists) | Patterns Detected |
|---|---|---|---|
{% for item in site.data.agentic %}
| [repo]({{ item.repo }}) | {{ item.extraction }} | {% if item.paper %}[paper]({{ item.paper }}){% else %}-{% endif %} | {{ item.patterns | join: ", " }} |
{% endfor %}
