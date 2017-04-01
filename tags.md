---
layout: default
title: Tags
---

<div class="home" id="home">
  <h1 class="pageTitle">Tags</h1>
  	{% for tag in site.tags %}
		{% assign t = tag | first %}
		{% assign posts = tag | last %}

		<a href="/tags/{{t | downcase | replace:" ","-" }}" class="btn btn-sm btn-default">{{ t }}</a>
    {% endfor %}
</div>
