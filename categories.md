---
layout: default
title: Categories
---

<div class="home" id="home">
  <h1 class="pageTitle">Categories</h1>
  	{% for category in site.categories %}
		{% assign t = category | first %}
		{% assign posts = category | last %}

		<a href="/categories/{{t | downcase | replace:" ","-" }}" class="btn btn-sm btn-default">{{ t }}</a>
    {% endfor %}
</div>
