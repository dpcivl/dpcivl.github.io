---
title: "꾸준히 하면 뭐든 되겠지.."
layout: archive
permalink: /daily
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['daily']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}