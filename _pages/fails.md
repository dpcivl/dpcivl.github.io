---
title: "실패하더라도 일단 올리고 보자"
layout: archive
permalink: /fails
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['fails']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}