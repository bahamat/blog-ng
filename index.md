---
layout: home
---

<!-- # To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults -->

Hello, this is the index.

<h2>Most Recent Post</h2>
{% assign latest = site.posts.first %}
<article>
  <h2><a href="{{ latest.url | relative_url }}">{{ latest.title }}</a></h2>
  <small>{{ latest.date | date: "%b %-d, %Y" }}</small>
  <div>
    {{ latest.content }}
  </div>
</article>

<h2>Recent Posts</h2>
<ul>
  {% for post in site.posts limit: site.recent_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
