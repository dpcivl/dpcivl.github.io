---
title: "What I tried"
layout: archive
permalink: /trial
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['trial']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}