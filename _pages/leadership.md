---
layout: single
title: "Leadership"
permalink: /leadership/
author_profile: true
---

{% assign cv = site.data.cv %}
{% comment %} Work entries 4–6 are leadership / community involvement {% endcomment %}
{% for work in cv.work offset: 3 limit: 3 %}
## {{ work.position }}
**{{ work.company }}** · {{ work.startDate }}{% if work.endDate != work.startDate %} – {{ work.endDate }}{% endif %}

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
