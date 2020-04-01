---
layout: page
title: About
---

<section>
<header class ="major">
<h1>All Posts</h1>
</header>
<div class = "row">
  {% for post in site.posts %}
    <div class="6u 12u$(small)">
    <header class ="major">
      <h2>{{ post.title}}</h2>
      <p>{{ post.date | date_to_string }} | {{ post.category}}</p>
      </header>
     {{ post.excerpt | strip_html | strip_newlines | truncate: 156 }}

<br />
<br />
      <ul class="actions">
        <li><a href="{{ post.url }}" class="button">Read</a></li>
      </ul>
    </div>
    <div class="6u 12u$(small)">
      <span class="image fit">  <img src="{{ post.thumbnail }}" style="width: 100%; max-height: 100%"/></span>
    </div>
  {% endfor %}
</div>