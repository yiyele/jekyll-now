---
layout: default
title: Category
---

<div class="categories">
<h1><a href="{{ site.baseurl }}/category_C++">{{ categories[0] | first }}</a></h1>
<span>{{ categories[0] | last | size }}</span>
<ul class="arc-list">
	{% if categories[0].last[0].url %}
		<li>{{ categories[0].last[0].date | date:"%d/%m/%Y "}}<a href="{{ categories[0].last[0].url }}">{{ categories[0].last[0].title }}</a></li>
	{% endif %}
	{% if categories[0].last[1].url %}
		<li>{{ categories[0].last[1].date | date:"%d/%m/%Y "}}<a href="{{ categories[0].last[1].url }}">{{ categories[0].last[1].title }}</a></li>
	{% endif %}
	{% if categories[0].last[2].url %}
		<li>{{ categories[0].last[2].date | date:"%d/%m/%Y "}}<a href="{{ categories[0].last[2].url }}">{{ categories[0].last[2].title }}</a></li>
	{% endif %}
</ul>

</div>
