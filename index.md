---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
<ul>
{% assign sitepages = site.pages | sort: 'order' %}
{% for sitepage in sitepages %}
{% if sitepage.categories == 'home' %}
  <h2 >  	
    <a class="post-link" href="{{ sitepage.url }}">{{ sitepage.title }}</a>    
  </h2>
  {% endif %}
{% endfor %}
</ul>
