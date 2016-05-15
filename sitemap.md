---
title:      Карта сайта
short:      Карта сайта
---
<ul>
  {% for collection in site.collections %}
    <li><a href='{{ site.url }}/{{ collection.label }}'>{{ collection.title }}</a> - {{ collection.short }}
      <ul>
      {% for doc in collection.docs %}
        <li><a href='{{ doc.url }}'>{{ doc.title }}</a> {{ doc.short if doc.short }}</li>
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  {% for page in site.pages unless page.title %}
    <li><a href='{{ page.url }}'>{{ page.title }}</a> {{ page.short if page.short }}</li>
  {% endfor %}
</ul>