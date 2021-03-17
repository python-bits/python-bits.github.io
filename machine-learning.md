---
layout: default
title: Machine Learning
---

<ul>
{% for post in site.categories['machine-learning'] %}
	<li>
		<a href="{{ post.url }}">{{ post.title }}</a>
        <img src="{{ post.image }}" width="200" >
        {{ post.excerpt }}
	</li>
{% endfor %}
</ul>