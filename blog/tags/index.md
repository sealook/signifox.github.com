---
layout: page
title: Tags
---

<div id="blog-marks" class="tags">
	{% for tag in site.tags %}
	<article class="hentry" role="article">
	<h1 id="{{ tag[0] }}-ref">{{ tag[0] }}</h1>
	<hr>
	{% for post in tag[1] %}
	<p>
		<time>{{ post.date | date: "%Y-%b-%d" }}</time>  &raquo;   
		<a href='{{ post.url }}'>{{post.title}}</a>
	</P>
	{% endfor %}
    </article>
    {% endfor %}
</div>