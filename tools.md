---
layout: default
title: Tools
---
 
<ul>
{% for post in site.categories['tools'] %}
	<li>
		<a href="{{ post.url }}">{{ post.title }}</a>
        <img src="{{ post.image }}" width="200" >
        {{ post.excerpt }}
	</li>
{% endfor %}
</ul>
