---
layout: page
title: Tags
---
<div id="blog-marks" class="tags">
	{% for tag in site.tags %}
	<article>
	<h1 id="{{ tag[0] }}-ref">{{ tag[0] }}</h1>
	<hr>
	{% for post in tag[1] %}
		<h3>{{ post.date | date: "%Y-%b-%d"}}  &raquo;  <a href='{{ post.url }}'>{{post.title}}</a></h3>
	{% endfor %}
    </article>
    <br>
	{% endfor %}
</div>

