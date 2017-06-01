---
layout: single
title: tags
---
<div>
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
  <span class="site-tag">
    <a href="{{ tag | first | slugify }}">
      {{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
    </a>
  </span>
  {% endfor %}
</div>
