---
title: Творчество
short: Мои короткие истории
---

Я иногда радую читателей своими короткими набросками и рассказами, почти все они собраны тут

<table>
  {% for story in site.stories | sort: 'page.title }}' %}
    <tr><td><a href="{{ story.url | prepend: story.baseurl }}">{{ story.title }}</a></td><td>{{ story.short }}</td></tr>
  {% endfor %}
</table>