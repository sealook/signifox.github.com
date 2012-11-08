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
		<h4>
			<time>{{ post.date | date: "%Y-%b-%d" }}</time>  &raquo;   
			<a href='{{ post.url }}'>{{post.title}}</a>
		</h4>
	{% endfor %}
    </article>
    {% endfor %}
</div>