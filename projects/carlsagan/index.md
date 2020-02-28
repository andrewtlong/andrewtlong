---
layout: default
title: Carl Sagan
---
<div class="container">
  <h1>Carl Sagan</h1>
  <p>Carl Sagan is my pet snapping turtle. He was found in my yard as a hatchling, and I have been taking care of him ever since. I have had him for about a year now, and he is growing into quite a remarkable creature. Here you can keep up-to-date on how he is doing, and see what steps I'm taking to ensure he can be safely released back into the wild.</p>
</div>

{% for post in site.categories.Turtle %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
