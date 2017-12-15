---
layout: page
title: Blog
permalink: /blog/
feature-img: "img/color.png"
---

<div class="posts">
  <h2 class="post-header">My Posts</h2>
  <ul>
    {% for post in paginator.posts %}
    <li class="post-teaser">
      <header>
        <h3>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
            {{ post.title }}
          </a>
        </h3>
        <p class="meta">
          {{ post.date | date: "%B %-d, %Y" }}
        </p>
      </header>
      <div class="excerpt">
        {{ post.excerpt | | strip_html | strip_newlines | truncate: 120 }}
      </div>
      <a href="{{ post.url | prepend: site.baseurl }}">
        {{ site.theme_settings.str_continue_reading }}
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
