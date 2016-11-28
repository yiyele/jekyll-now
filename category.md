---
layout: default
title: Category
---

<div class="categories">
{% for category in site.categories %}
<h1>{{ category | first }}</h1>
<span>{{ category | last | size }}</span>
<ul class="arc-list">
	{% if category.last[0].url %}
		<li>{{ category.last[0].date | date:"%d/%m/%Y "}}<a href="{{ category.last[0].url }}">{{ category.last[0].title }}</a></li>
	{% endif %}
	{% if category.last[1].url %}
		<li>{{ category.last[1].date | date:"%d/%m/%Y "}}<a href="{{ category.last[1].url }}">{{ category.last[1].title }}</a></li>
	{% endif %}
	{% if category.last[2].url %}
		<li>{{ category.last[2].date | date:"%d/%m/%Y "}}<a href="{{ category.last[2].url }}">{{ category.last[2].title }}</a></li>
	{% endif %}
</ul>
{% endfor %}
</div>
