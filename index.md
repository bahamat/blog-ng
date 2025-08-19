---
layout: default
---

<!-- # To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults -->

Hello, this is the index.

<h2>Recent Posts</h2>
<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
