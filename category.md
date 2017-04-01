---
layout: default
title: Categories
---

<div class="home" id="home">
  <h1 class="pageTitle">Category</h1>
  	{% for category in site.categories %}
		{% assign t = category | first %}
		{% assign posts = category | last %}

		<a href="/category/{{t | downcase | replace:" ","-" }}" class="btn">{{ t }}</a>
    {% endfor %}
</div>
