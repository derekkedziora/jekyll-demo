---
title: Tag Page
permalink: /tags
---

<div markdown=1 style="min-height: 100vh;">

You can style the tag menu and each tag section with `min-height: 100vh;`

Then add a back to top link at the bottom of each section. This looks less cluttered when you have lot of tags and posts.

Check out my full guide to [making a tag page in Jekyll](https://derekkedziora.com/blog/tag-page-jekyll).  

Back to the [main page](/).


{% for tag in site.tags %}

[{{ tag[0] }}&nbsp;({{ tag[1] | size }})](#{{tag[0]}})

{% endfor %}

</div>


{% for tag in site.tags %}

<div markdown=1 style="min-height: 100vh;">

## {{tag[0]}}

{% for post in tag[1] %}

[{{ post.title }}]({{ post.url }})

{% endfor %}

[All Tags &#8593;](#)

</div>

{% endfor %}
