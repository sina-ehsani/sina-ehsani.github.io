---
title: Blog
layout: page
permalink: /blog/
---

<div class="blog-list">
{% for post in site.posts %}
    {% unless post.hidden %}
        {% include blog-post.html %}
    {% endunless %}
{% endfor %}
</div>
