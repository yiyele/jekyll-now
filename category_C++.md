---
layout: default
title: C++
category: C++
---
<div class="category">
{% for post in site.categories.[page.category] %}
	<li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>