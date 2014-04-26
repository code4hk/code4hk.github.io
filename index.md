---
layout: page
title: Code4HK
tagline: Drive Social Changes By Code
---
{% include JB/setup %}

<h2>Recent posts</h2>

 - Website:        http://www.code4.hk/
 - Facebook group: https://www.facebook.com/groups/code4hk/
 - Twitter:        https://twitter.com/code4hk

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


