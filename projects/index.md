---
layout: archive
title: "Projects"
permalink: /projects/
---
{% for project in site.projects %}
- [{{ project.title }}]({{ project.url | relative_url }}) — {{ project.excerpt }}
{% endfor %}
