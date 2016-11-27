---
layout: default
title: Category
permalink: /category/
---

<div class="category">
{% for category in site.categories %}
<h1><a href="{{ site.baseurl }}/myhtml/test.html">{{ category | first }}</a></h1>
<span>{{ category | last | size }}</span>
<ul class="arc-list">
	{% for post in category.last %}
		<li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>
{% endfor %}
</div>
