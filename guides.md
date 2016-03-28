---
layout: page
title: "Guides"
permalink: /guides/
---

<!-- Repeat all of the guides -->
{% for post in site.posts %}
{% if post.category == 'guide' %}

  <div class = "guideItem">
  <h4 class = "guideItemTitle"><a href="{{ post.url }}">{{ post.title }}</a></h4>
  <h5 class = "guideItemDesc">{{post.shortDescription}}</h5>
  </div>

{% endif %}
{% endfor %}
