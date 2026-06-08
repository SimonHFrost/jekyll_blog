---
layout: page
title: Drafts
permalink: /drafts/
noindex: true
sitemap: false
---

Works in progress. Not linked from anywhere — bookmark this page.

<ul class="post-list">
  {%- assign draft_posts = site.posts | where: "draft", true -%}
  {%- if draft_posts.size > 0 -%}
    {%- for post in draft_posts -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <h4>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h4>
    </li>
    {%- endfor -%}
  {%- else -%}
    <li>No drafts right now.</li>
  {%- endif -%}
</ul>
