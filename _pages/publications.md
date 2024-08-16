---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
<style>
    /* General body text */
    body {
        font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
        font-size: 14px;
        line-height: 1.6;
        color: #333;
        background-color: #f8f9fa;
        margin: 0;
        padding: 0;
    }
    /* Headers */
    h1, h2, h3, h4, h5, h6 {
        font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
        font-weight: bold;
        color: #2c3e50;
        margin-bottom: 18px;
    }
    h1 {
        font-size: 18px;
        margin-top: 30px;
    }
    h2 {
        font-size: 16px;
        margin-top: 25px;
    }
    h3 {
        font-size: 14px;
        margin-top: 20px;
    }
    /* Link styling */
    a {
        color: #3498db;
        text-decoration: none;
    }
    a:hover {
        text-decoration: underline;
    }
    /* List styling */
    ul, ol {
        margin-bottom: 20px;
        padding-left: 20px;
    }
    li {
        margin-bottom: 10px;
    }
    /* General content padding */
    .content {
        padding: 20px;
        max-width: 800px;
        margin: auto;
    }
</style>

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.categories contains category[0] %}
        {% unless title_shown %}
          <h2>{{ category[1].title }}</h2>
          <hr />
          {% assign title_shown = true %}
        {% endunless %}
        {% include archive-single.html %}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% else %}
  <h2>All Publications</h2>
  <hr />
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
