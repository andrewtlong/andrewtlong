---
title: All Posts
---

<div class="container">
  {% for post in site.posts %}
    <div class="card">
      <div class="card-header">
        <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {%- assign date_format = "%b %-d, %Y" -%}
            {{ post.date | date: date_format }}
          </time>
      </div>
      <div class="card-body">
        {{ post.excerpt }}
        <a href="{{ post.url }}"
        title="Read More"
        class="btn btn-shadow btn-sm btn-outline-primary" align="right">
        Read More
        </a>
      </div>
      <div class="card-footer text-muted" align="left">
        {% if post %}
  {% assign categories = post.categories %}
  {% else %}
  {% assign categories = page.categories %}
  {% endif %}
  {% for category in categories %}
  <a href="{{site.baseurl}}/categories/#{{category|slugize}}" class="badge badge-primary">{{category}}</a>
  {% unless forloop.last %}{% endunless %}
  {% endfor %}
      </div>
    </div>
    <br>
  {% endfor %}
</div>