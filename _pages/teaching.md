---
layout: page
permalink: /teaching/
title: Teaching
description: Undergraduate and Graduate teaching at different institutions.
nav: true
nav_order: 3
---

<div class="publications">

{% for course in site.data.teaching %}
<div class="row">
  <div class="col-sm-10">
    <div class="title">{{ course.code }} - {{ course.title }}</div>
    <div class="periodical"><em>{{ course.institution }}</em>, {{ course.semester }}</div>
    <div class="links">
      {% if course.material %}
        <a href="{{ course.material }}" class="btn btn-sm z-depth-0" role="button">Material</a>
      {% endif %}
    </div>
  </div>
</div>
{% endfor %}

</div>
