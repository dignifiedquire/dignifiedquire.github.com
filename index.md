---
layout: page
title: latest.posts
---



{% for post in site.posts limit 4 %}
<div class="row">
  <div class="span10">
  <h2>
    <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    <small>{{ post.date | date_to_string }}</small>
  </h2>
  <p>
    {{ post.content | strip_html | truncatewords:75}}<br>
    <a href="{{ post.url }}">Read more...</a><br><br>
  </p>        
  </div>
</div>
{% endfor %}