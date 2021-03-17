---
layout: default
title: "Hauptseite"
---

<ul>
{% for post in site.posts %}
	<li>
		<a href="{{ post.url }}">{{ post.title }}</a>
        <img src="{{ post.image }}" width="200" >
        {{ post.excerpt }}
	</li>
{% endfor %}
</ul>
