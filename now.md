---
title: Now Page
description: "This is what I would be doing now if this were a real site"
nowPage: true
permalink: /now
---

{{ site.categories.now[0].content }}

## Previous Now Pages

{% for post in site.categories.now offset: 1 %}

[{{ post.title }}]({{ post.url }})

{% endfor %}