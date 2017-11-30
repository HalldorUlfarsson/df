---
layout: page
title: older
---
Everything older than 2013, newest first.

<div class="posts">
  {% for post in site.posts %}
  {% assign this_post_year = post.date | date: "%Y" %}

  {% if this_post_year == "2012,2011,2010,2009" %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    {{ post.content }}
  </div>
  {% endif %}
  {% endfor %}
</div>
