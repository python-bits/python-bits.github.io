---
layout: default
title: Grundlagen
---

<ul>
{% for post in site.categories['grundlagen'] %}
	<li>
		<a href="{{ post.url }}">{{ post.title }}</a>
        <img src="{{ post.image }}" width="200" >
        {{ post.excerpt }}
	</li>
{% endfor %}
</ul>