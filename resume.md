---
layout: resume
title: Resume
permalink: /resume/
---

{% for job in site.data.jobs %}
<section class = "opportunity">
  <header><h1>{{job.title}}<span> {{job.employer}}</span></h1></header>
  <div class="timeline">{{job.start_date | start_date: "%b %Y"}} to {% if job.end_date %}{{ job.end_date | end_date: "%b %Y"}}{% else %}present{% endif %}<br/>{{job.location}}</div>
  <ul>
  {% for task in job.tasks %}
    <li>{{task.item}}</li>
  {% endfor %}
  </ul>
</section>
{% endfor %}