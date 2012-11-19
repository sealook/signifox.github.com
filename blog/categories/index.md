---
layout: page
title: Categories
---

<div id="blog-marks" class="categories">

	{% for cat in site.categories %}
	<article class="hentry" role="article">
	<h1 id="{{ cat[0] }}-ref">{{ cat[0] }}</h1>
	<hr>
	{% for post in cat[1] %}
	<p>
		<time>{{ post.date | date: "%Y-%b-%d" }}</time>  &raquo;   
		<a href='{{ post.url }}'>{{post.title}}</a>
	</P>
	{% endfor %}
    </article>
    {% endfor %}
</div>
