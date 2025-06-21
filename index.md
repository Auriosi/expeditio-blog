---
layout: default
title: Expeditio Dev Blog
---

## Latest Developer Blogs

{% for post in site.posts limit: 5 %}
### [{{ post.title }}]({{ post.url | relative_url }})
<p class="post-meta">{{ post.date | date: "%B %d, %Y" }} - {{ post.categories | join: ", " }}</p>
{{ post.excerpt }}
[Read More &raquo;]({{ post.url | relative_url }})
{% endfor %}

---
