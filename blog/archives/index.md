---
layout: page
title: Blog Archive
footer: false
---

<div id="blog-archives">
	{% for post in site.posts reverse %}
	{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
	{% unless year == this_year %}
	{% assign year = this_year %}
	<h2>{{ year }}</h2>
	{% endunless %}
	<article>
	<h1><a href='{{ post.url }}'>{{post.title}}</a></h1>

	<time>{{ post.date | date: "<span class='month'>%b</span> <span class='day'>%d</span>" }}</time>
	
	<footer>
	<time>{{ page.date | date: "%Y-%b-%d" }}</time>
	<span class="categories">
		Category:
		{% for cat in post.categories %}
		<a class='category' href='/blog/categories/index.html#{{ cat }}-ref/'> {{ cat }} </a>
		{% endfor %}
	</span>
	<span class="tags">
		Tags:
		{% for tag in post.tags %}
		<a class='tag' href='/blog/tags/index.html#{{ tag }}-ref/'> {{ tag }} </a>
		{% endfor %}
	</span>
	</p>
	</footer>
	</article>
	{% endfor %}
</div>
