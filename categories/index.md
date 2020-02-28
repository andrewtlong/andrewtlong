---
layout: page
permalink: /categories/
title: Categories
---


<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head">{{ category_name }}</h3>
      <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        <article class="archive-item">
          <div class="card">
            <div class="card-header">
              <h4>
                <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>
              </h4>
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
        </article>
        {% endfor %}
        </div>      
  </div>
{% endfor %}
</div>
