---
title: "Posts"
layout: collection
permalink: /postsGrid/
collection: posts
entries_layout: list
author_profile: false
pagination: 
  enabled: true
  paginate: 1
  category: posts
---
<ul>
  {% for post in paginator.posts %}
    <!-- what you want to output. title, url, image, etc. -->
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}">Newer Posts</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}">Older Posts</a>
  {% endif %}
{% endif %}