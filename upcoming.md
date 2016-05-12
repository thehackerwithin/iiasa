---
layout: layout
title: "Upcoming Topics"
---

<section class="content">

Upcoming Topics
================

**Spring 2015**

The Hacker Within will explore the following tentative set of topics in
Spring 2015. In addition to these topics, Lightning Talks are welcome at the
end of every session, so please don't hesitate to bring some tidbit to share.
Also, if you would like to contribute to a topic, contact the volunteer in
charge of that topic to see if they would like to collaborate.


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
