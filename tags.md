---
title: Tag Page
permalink: /tags
---

{% for tag in site.tags %}
  {% assign placeHolderTag = tag | first %}
  {% assign listOfTags = listOfTags | append: placeHolderTag %}
  {% assign listOfTags = listOfTags | append: ',' %}
{% endfor %}

{% assign listOfTags = listOfTags | split: ',' | sort_natural %}

<div style="min-height: 100vh;" markdown="1">

{% for listOfTag in listOfTags %}
  <p><a href="#{{listOfTag}}">{{listOfTag | replace: "-", " "}}</a></p>
{% endfor %}

You can style the tag menu and each tag section with `min-height: 100vh;`

Then add a back to top link at the bottom of each section. This looks less cluttered when you have lot of tags and posts.

Check out my full guide to [making a tag page in Jekyll](https://derekkedziora.com/blog/tag-page-jekyll).  

Back to the [main page](/).

</div>

{% for listOfTag in listOfTags %}
<div style="min-height: 100vh;">
<h3 id='{{listOfTag}}'>{{listOfTag | replace: "-", " "}}</h3>

{% for post in site.posts %}
{% if post.tags contains listOfTag %}
<p><a href="{{post.url}}">{{post.title}}</a></p>
{% endif %}
{% endfor %}
<a href="#">Back to all tags</a>
</div>
{% endfor %}