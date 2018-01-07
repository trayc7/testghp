---
layout: page
title: Activities
permalink: /Activities/
---

<h1 class="page-title">{{ page.title | escape }}</h1>

<div class="section">
<div style="background: #ddd">
    <div class="container last-post">
        <ul class="collection">
	        {% for post in site.posts %}
		        <li class="collection-item avatar">
		          {% assign date_format = site.minima.date_format | default: "%m/%d" %}
		          <div class="date-post">{{ post.date | date: date_format }}</div>
		          <span class="title"><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></span>
		          <p>
		             {{ post.content | truncatewords: 10 }}
		          </p>
		          <a href="{{ post.url | relative_url }}" class="secondary-content"><i class="material-icons">navigate_next</i></a>
	        {% endfor %}
 