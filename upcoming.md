---
layout: layout
title: "Upcoming Topics"
---

<section class="content">

Upcoming Topics
================

The list of topics is ever-changing, here are the topics we already have
scheduled for upcoming talks

<ul class="listing">
{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts reversed %}
    {% assign postStartDate = post.date | date: '%s' %}
	{% if postStartDate >= curDate %}
	<li>
	<span>{{ post.date | date: "%B %e, %Y" }}</span>
	<a href="{{ base }}{{ post.url }}">
	{{ post.title }} {% if post.author %} &ndash; {{ post.author }} {% endif %}
	</a></li>
    {% endif %}
{% endfor %}
</ul>

</section>
