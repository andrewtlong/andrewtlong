---
layout: default
title: Carl Sagan
---
<div class="container">
  <h1>Carl Sagan</h1>
  <p>Carl Sagan is my pet snapping turtle. He was found in my yard as a hatchling, and I have been taking care of him ever since. I have had him for about a year now, and he is growing into quite a remarkable creature. Here you can keep up-to-date on how he is doing, and see what steps I'm taking to ensure he can be safely released back into the wild.</p>
</div>

<div class="container">
  {% for post in site.categories.Turtle limit: 10 %}
    <div class="card">
      <div class="card-header">
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p>Posted in:
          {% if post %}
            {% assign categories = post.categories %}
            {% else %}
              {% assign categories = page.categories %}
          {% endif %}
          {% for category in categories %}
            <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
            {% unless forloop.last %}&#44;&nbsp;{% endunless %}
          {% endfor %}
        </p>
        <p style="font-size: 11px">
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {%- assign date_format = "%b %-d, %Y" -%}
            {{ post.date | date: date_format }}
          </time>
        </p>
      </div>
      <div class="card-body">
        <p>{{ post.excerpt }}</p>
      </div>
      <div class="card-footer text-muted" align="right">
        <a href="{{ post.url }}"
        title="Read More"
        class="btn btn-shadow btn-sm btn-outline-primary" align="right">
        Read More
        </a>
      </div>
    </div>
    <br>
  {% endfor %}
  </div>

  <a href="/categories/#Turtle"
               title="View More Posts"
               class="btn btn-lg btn-danger btn-shadow px-3 my-2 ml-0 text-left" align="right">
              View More Posts
            </a>
