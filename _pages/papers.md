---
title: "기초 논문 공부"
layout: archive
permalink: /papers
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['papers']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}