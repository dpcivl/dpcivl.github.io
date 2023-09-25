---
title: "Today I learned"
layout: archive
permalink: /til
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['til']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}