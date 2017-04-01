---
layout: default
title: Posts by tags
---

<div class="home" id="home">
  <h1 class="pageTitle">Posts by Tags</h1>
  <ul class="posts noList">
  	{% for tag in site.tags %}
		{% assign t = tag | first %}
		{% assign posts = tag | last %}

		{{ t | downcase }}
		<ul>
		{% for post in posts %}
	  	  {% if post.tags contains t %}
	  	  <li>
		    <a href="{{ post.url }}">{{ post.title }}</a>
		    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
	  	  </li>
	  	  {% endif %}
	    {% endfor %}
	    </ul>
    {% endfor %}
  	<!--
    {% for post in paginator.posts %}
      <li>
        <span class="date">{{ post.date | date: '%B %d, %Y' }}</span>
        <h3><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
        <p class="description">{% if post.description %}{{ post.description | strip_html | strip_newlines | truncate: 250 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 250 }}{% endif %}</p>
      </li>
    {% endfor %}
    -->
  </ul>
  <!-- Pagination links -->
  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | prepend: site.baseurl }}" class="previous button__outline">Newer Posts</a> 
    {% endif %}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | prepend: site.baseurl }}" class="next button__outline">Older Posts</a>
    {% endif %}
  </div>
</div>
