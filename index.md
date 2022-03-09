---
layout: default
---

{% include introduction.md %}

<ul class="posts">
  {% for post in site.posts %}
    <li class="post">
      <div class="post__date">
        <div class="post__date">{{ post.date | date_to_string }}</div>
      </div>
      <div class="post__details">
        <a class="post__title" href="{{ post.link }}">{{ post.title }}</a>
        {% if post.author %}
          <div class="post__author">by {{ post.author }}</div>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
