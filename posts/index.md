---
title: All Posts
---

<div class="container">
  {% for post in site.posts %}
    <div class="card">
      <div class="card-header">
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p style="font-size: 11px">
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {%- assign date_format = "%b %-d, %Y" -%}
            {{ post.date | date: date_format }}
          </time>
        </p>
      </div>
      <div class="card-body">
        {{ post.excerpt }}
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