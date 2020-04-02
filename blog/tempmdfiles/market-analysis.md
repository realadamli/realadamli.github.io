---
layout: page
title: About
---

<section>
<header class ="major">
<h1>Market Analysis</h1>
</header>
<div class = "row">
  {% for post in site.posts %}
  {% if post.categories == "market analysis" %}
    <div class="6u 12u$(small)">
    <header class ="major">
      <h2>{{ post.title}}</h2>
      <p>{{ post.date | date_to_string }} | {{ post.categories}}</p>
      </header>
     {{ post.excerpt | strip_html | strip_newlines | truncate: 126 }}

<br />
<br />
      <ul class="actions">
        <li><a href="{{ post.url }}" class="button">Read Now</a></li>
      </ul>
    </div>
    <div class="6u 12u$(small)">
      <span class="image fit">  <img src="{{ post.thumbnail }}" style="width: 100%; max-height: 100%" alt="{{ post.alt }}"/></span>
    </div>
    {% endif %}
  {% endfor %}
</div>