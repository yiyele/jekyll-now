---
layout: default
title: Category
permalink: /category/
---

{% for category in site.categories %}
<h2>{{ category | first }}</h2>
<span>{{ category | last | size }}</span>
<ul class="arc-list">
	{% for post in category.last %}
		{% if post.index == category[0] %}
			<li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ post.url }}">{{ post.title }}</a></li>
		{% endif %}
	{% endfor %}
</ul>
{% endfor %}
