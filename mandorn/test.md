---
layout: default
title: test
permalink: /mandorn/test/
---

{% for category in site.categories.test %}
<h2><a href="{{ category.url }}/{{ category.title }}">{{ category | first }}</a></h2>
<span>{{ category | last | size }}</span>
<ul class="arc-list">
	{% for post in category.last %}
		<li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>
{% endfor %}
