---
layout: single
title: "All Public Repos"
permalink: /projects/all/
---
{% assign repos = site.github.public_repositories | where: "owner.login", "berkeleyo" | sort: "pushed_at" | reverse %}
{% for repo in repos %}
  {% unless repo.name == "berkeleyo.github.io" %}
    {% include repo-card.html repo=repo %}
  {% endunless %}
{% endfor %}
