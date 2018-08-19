---
layout: archive
title: "Python"
excerpt: "A collection of Python3.x Usage."
image:
  feature:
  teaser:
---

<div class="tiles">
{% for post in site.categories.python %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
