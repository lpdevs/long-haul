---
layout: default
title: Posts by tags
---

<div class="home" id="home">
  <h1 class="pageTitle">Posts by Tags</h1>
  	{% for tag in site.tags %}
		{% assign t = tag | first %}
		{% assign posts = tag | last %}

		<a href="/tags/{{ t | downcase }}" class="btn btn-sm btn-default">{{ t }}</a>
    {% endfor %}
</div>
