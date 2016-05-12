---
layout: layout
title: Previous Topics
---

<section class="content">

Previous Topics
===============


<ul class="listing">
{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
    {% assign postStartDate = post.date | date: '%s' %}
	{% if postStartDate < curDate %}
	<li>
	<span>{{ post.date | date: "%B %e, %Y" }}</span>
	<a href="{{ base }}{{ post.url }}">
	{{ post.title }} {% if post.author %} &ndash; {{ post.author }} {% endif %}
	</a></li>
    {% endif %}
{% endfor %}
</ul>

</section>
