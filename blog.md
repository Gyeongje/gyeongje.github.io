---
layout: page
title: Blog
subtitle: Writeups & Notes
permalink: /blog/
---

<div>
{% assign postsCategory = site.posts | group_by_exp:"post", "post.categories"  %}
{% for category in postsCategory %}
<h4 class="post-teaser__month">
<strong>
{% if category.name %}
- - - - -  {{ category.name }} - - - - -
{% else %}
{{ Print }}
{% endif %}
</strong>
</h4>
<ul class="list-posts">
{% for post in category.items %}
<li class="post-teaser">
<a href="{{ post.url | prepend: site.baseurl }}">
<span class="post-teaser__title">{{ post.title }}</span>
<span class="post-teaser__date">{% if post.period %}{{ post.period }}{% else %}{{ post.date | date: "%d %B %Y" }}{% endif %}</span>
</a>
</li>
{% endfor %}
</ul>
{% endfor %}
</div>

<div class="about">
<div class="about__divider">*****</div>
<div class="about__text"><strong>Old Blog: <a href="https://blog.gye0ngje.com">blog.gye0ngje.com</a></strong></div>
</div>
