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
        line-height: 1.6; /* This adds spacing between lines of text */
        color: #333;
        background-color: #f8f9fa; /* Light background color for better readability */
        margin: 0;
        padding: 0;
    }

    /* Headers */
    h1, h2, h3, h4, h5, h6 {
        font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
        font-weight: bold;
        color: #2c3e50;
        margin-bottom: 18px; /* Adds space below headers */
    }

    h1 {
        font-size: 18px;
        margin-top: 30px; /* Adds space above main header */
    }

    h2 {
        font-size: 16px;
        margin-top: 25px; /* Adds space above this level header */
    }

    h3 {
        font-size: 14px;
        margin-top: 20px; /* Adds space above this level header */
    }

    /* Link styling */
    a {
        color: #3498db;
        text-decoration: none; /* Removes underline from links */
    }

    a:hover {
        text-decoration: underline; /* Adds underline on hover for clarity */
    }

    /* List styling */
    ul, ol {
        margin-bottom: 20px; /* Adds space below lists */
        padding-left: 20px; /* Adds padding to the left of lists */
    }

    li {
        margin-bottom: 10px; /* Adds space between list items */
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

<!-- Added header for Publications -->
<h2>Publications</h2><hr />

{% for post in site.publications reversed %}
  {% if post.type == "publication" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<!-- Added header for Work in Progress -->
<h2>Work in Progress</h2><hr />

{% for post in site.publications reversed %}
  {% if post.type == "work_in_progress" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
