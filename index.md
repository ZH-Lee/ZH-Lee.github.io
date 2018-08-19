---
layout: home
permalink: /
image:
  feature: spot.jpg
---

<div class="tiles">
{% for post in site.posts %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
