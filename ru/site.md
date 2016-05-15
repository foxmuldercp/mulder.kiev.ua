---
title: О сайте (карта)
short: Техническое описание сайта и карта
---

Несколько лет этот сайт жил и работал на [WordPress](WordPress.org) и занимал около 100 мебагайт дискового
места, но компоненты WP обновлялись в среднем раз в месяц, чего нельзя сказать о содержимом, которое не
обновлялось годами

Около полгода этот сайт жил и работал на моём домашнем роутере, Cisco 1841

С февраля 2016 сайт использует генератор статического сайта Jekyll и занимает около мегабайта, не считая CV
и моих композиций

### Карта

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
