---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<ul>
{% assign sitepages = site.pages | sort: 'order' %}
{% for sitepage in sitepages %}
{% if sitepage.categories == 'home' %}
  <li >  	
    <a href="{{ sitepage.url }}">{{ sitepage.title }}</a>    
  </li>
  {% endif %}
{% endfor %}
</ul>
