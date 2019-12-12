---
layout: page
title: Blog
---

# Posts

{% for post in site.posts %}
* <span>{{post.date | date_to_string}}</span>
  »
  [{{post.title}}]({{post.url}})
{% endfor %}
