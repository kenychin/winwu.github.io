---
layout: page
title:  Frontend Developer Note.
tagline: Just Share
---
{% include JB/setup %}

    
## Latest Posts

<ul id="latest_post_ul" class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}"  data-pjax='#pjax-container'>{{ post.title }}</a></li>
  {% endfor %}
</ul>



