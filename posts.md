---
layout: page
title: Posts
permalink: /posts/
---

<div class="listofposts">
<p>
{% for category in site.categories %}
  <div name="{{ category | first }}" class="{{ category | first }}">
  <h3>{{ category | first }}</h3>
    <ol>
    {% for posts in category %}
      {% for post in posts %}
        {% if post.url %}
           <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endif %}
      {% endfor %}
    {% endfor %}
    </ol>
  </div>
{% endfor %}
</p>
</div>