---
layout: default
title: Category
permalink: /category/
---

{% for category in site.categories %}
<h2><a href="{{ category.url }}">{{ category | first }}</a></h2>
<span>{{ category | last | size }}</span>
<ul class="arc-list">
	{% for post in category.last %}
		<li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>
{% endfor %}
