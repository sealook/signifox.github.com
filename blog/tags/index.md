---
layout: page
title: Tags
---

<div id="blog-marks" class="tags">
	{% for tag in site.tags %}
	<article class="hentry" role="article">
	<h3 id="{{ tag[0] }}-ref">{{ tag[0] }}</h3>
	<hr>
	{% for post in tag[1] %}
	<p>
		<time>{{ post.date | date: "%Y-%b-%d" }}</time>  &raquo;   
		<strong><a href='{{ post.url }}'>{{post.title}}</a></strong>
	</P>
	{% endfor %}
    </article>
    {% endfor %}
</div>