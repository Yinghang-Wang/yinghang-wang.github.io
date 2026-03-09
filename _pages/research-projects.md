---
layout: single
title: "Research Projects"
permalink: /research-projects/
author_profile: true
---

{% assign cv = site.data.cv %}
{% comment %} First 3 work entries are research projects {% endcomment %}
{% for work in cv.work limit: 3 %}
## {{ work.position }}
**{{ work.company }}** · {{ work.startDate }} – {{ work.endDate }}

{{ work.summary }}

{% if work.highlights.size > 0 %}
<ul>
{% for h in work.highlights %}
  <li>{{ h }}</li>
{% endfor %}
</ul>
{% endif %}

---
{% endfor %}
