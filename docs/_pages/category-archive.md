---
title: "Posts by Category"
layout: categories
permalink: /categories/
author_profile: true
---

<div id="page-category">
  <h1 class="pl-lg-2">
    <i class="far fa-folder-open fa-fw text-muted"></i>
    {{ page.title }}
    <span class="lead text-muted pl-2">{{ page.posts | size }}</span>
  </h1>

  <ul class="post-content pl-0">
    {% assign post_long_df = site.data.date_format.post.long | default: '%b %e, %Y' %}

    {% for post in page.posts %}
    <li class="d-flex justify-content-between pl-md-3 pr-md-3">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="dash flex-grow-1"></span>
      <span class="text-muted small">{{ post.date | date: post_long_df }}</span>
    </li>
    {% endfor %}
  </ul>
</div>
