---
layout: default
title: Hispanics in Computing
subtitle: Gatherings
navigation: true
banner: banner.jpg
comment: above line for navigation for bofs
---

Our group gets together in Birds of a feather at various conferences. If you organize a gathering, take pictures and send us info so we can collect it here.

{% assign items = site.pages | where: "event","bof" | sort: 'year' %}
{% for c in items %}
  <li><a href="{{c.url | absolute_url}}">{{c.title}}</a></li>
{% endfor %}

