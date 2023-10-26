---
title: "I.MX 8M Plus - EVK"
layout: archive
permalink: /imx8mp
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['imx8mp']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}