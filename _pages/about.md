---
permalink: /
layout: single
title: "Michael Hasson <br> Neukom Postdoc Fellow @ Dartmouth"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<h2 class="section-header"> Using landscapes to understand Earth's past and future. </h2>

Geomorphologist and enjoyer of satellite data. My current work focuses on quantifying risks that climate change poses to humans and human infrastructure.

See below for past work. 

<h2 class="section-header"> Research </h2>

{% for project in site.data.projects %}

<h3 class="project-title"> {{project.title}} </h3>

![Project Visualization]({{ project.image | relative_url }}){: style="float: right; max-width: 400px; margin-left: 15px; margin-bottom: 10px; border-radius: 1px; box-shadow: 0 4px 10px rgba(0,0,0,0.08);"}

{% for pub in project.publications %}
  {% if pub.url %}
<a href="{{ pub.url }}" target="_blank" style="color: inherit; text-decoration: underline;">{{ pub.text | markdownify | remove: '<p>' | remove: '</p>' }}</a>
  {% else %}
{{ pub.text | markdownify | remove: '<p>' | remove: '</p>' }}
  {% endif %}
{% endfor %}

{{ project.description }}

<div style="clear: both;"></div>

---

{% endfor %}
