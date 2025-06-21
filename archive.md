---
layout: default
title: All Posts
permalink: /archive/
---

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}

{% for year in posts_by_year %}
## {{ year.name }}

<ul>
    {% for post in year.items %}
    <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-date"> - {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
    {% endfor %}
</ul>
{% endfor %}
