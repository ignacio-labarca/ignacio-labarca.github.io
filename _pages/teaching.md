---
layout: page
permalink: /teaching/
title: Teaching
description: Undergraduate and Graduate teaching at different institutions.
nav: true
nav_order: 3
---

<div class="publications">

{% assign sorted_courses = site.data.teaching | sort: "semester" | reverse %}
{% assign years = sorted_courses | map: "year" | uniq %}

{% for year in years %}
<h2 class="bibliography">{{ year }}</h2>
<ol class="bibliography">
  {% for course in sorted_courses %}
    {% if course.year == year %}
    <li>
      <div class="title">{{ course.code }} - {{ course.title }}</div>
      <div class="periodical"><em>{{ course.institution }}</em>, {{ course.semester }}</div>
      <div class="links">
        {% if course.material %}
          <a href="{{ course.material }}" class="btn btn-sm z-depth-0" role="button">Material</a>
        {% endif %}
      </div>
    </li>
    {% endif %}
  {% endfor %}
</ol>
{% endfor %}

</div>
