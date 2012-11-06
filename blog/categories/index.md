---
layout: page
title: Categories
---

<div id="blog-marks" class="categories">
	{% for cat in site.categories %}
	<article>
	<h1 id="{{ cat[0] }}-ref">{{ cat[0] }}</h1>
	<hr>
	{% for post in cat[1] %}
		<h3>{{ post.date | date: "%Y-%b-%d"}}  &raquo; <a href='{{ post.url }}'>{{post.title}}</a><h3>
	{% endfor %}
    </article>
    {% endfor %}
</div>
