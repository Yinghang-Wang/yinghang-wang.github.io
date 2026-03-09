---
layout: single
title: "Honors"
permalink: /honors/
author_profile: true
---

{% assign cv = site.data.cv %}

<ul class="honors-list">
{% for award in cv.awards %}
  <li><strong>{{ award.date }}</strong> — {{ award.name }}</li>
{% endfor %}
</ul>
