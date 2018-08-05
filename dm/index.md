---
layout: default
title: Data Mining
categories: home
folder: dm
---

<h1>{{ page.title }}</h1>
<ul class="posts">

{% assign chapKeys_chapValues = "chap1_Be Familiar With Data, chap2_Pre Processing"  | split: ", "%}

{% for key_value in chapKeys_chapValues  %}
	{% assign key_value_array = key_value | split: "_" %}
	<h2>{{key_value_array[1]}}</h2>
  	{% assign child_cat = page.folder | append: '\' | append: key_value_array[0] %}
  	{% for post in site.categories[child_cat] %}
  		<li>
  			<span>
  			{{ post.date | date_to_string }}
  		</span> 
  		<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  	</li>
  	{% endfor %}  
  	<br>
{% endfor %}


 
