# Agentic AI repositories

| Repo link | Extraction method | Paper | Patterns detected |
|---|---|---|---|
{% raw %}{% for item in site.data.agentic %}{% endraw %}
| {{ item.repo }} | {{ item.extraction }} | {{ item.paper }} | {{ item.patterns | join: ", " }} |
{% raw %}{% endfor %}{% endraw %}
