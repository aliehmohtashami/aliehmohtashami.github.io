---
layout: default
title: Learning Python
categories: home
folder: python
---

<h1>{{ page.title }}</h1>
<ul class="posts">

{% assign chapKeys_chapValues = "chap0-Python Programming 1, chap1-Python Programming 2 , chap2-Python Programming 3 , chap3-Python Programming 4, chap4-Pandas modules, chap5-Numpy modules"  | split: ", "%}

{% for key_value in chapKeys_chapValues  %}
	{% assign key_value_array = key_value | split: "-" %}
	<h2>{{key_value_array[1]}}</h2>
  	{% assign child_cat = page.folder | append: '\' | append: key_value_array[0] %}
  	{% for post in site.categories[child_cat] %}
  	<li>
  	<span>{{ post.date | date_to_string }}</span> <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  	</li>
  	{% endfor %}  
  	<br>
{% endfor %}


 
