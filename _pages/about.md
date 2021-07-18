---
layout: about
title: about
permalink: /
description: Notebook for papers we read

profile:
  align: #right
  image: #prof_pic.jpg

news: fals  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---

<div class="post">

  <div class="header-bar">
    <h1>{{ site.blog_name }}</h1>
    <h2>{{ site.blog_description }}</h2>
  </div>


  <ul class="post-list">
    {% for post in paginator.posts %}
      <li>
        <h3><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
        <p class="post-meta">{{ post.date | date: '%B %-d, %Y' }}</p>
        <p>{{ post.description }}</p>
      </li>
    {% endfor %}
  </ul>

  {% include pagination.html %}

</div>

