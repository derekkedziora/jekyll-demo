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

{% for listOfTag in listOfTags %}
  <a href="#{{listOfTag}}">{{listOfTag | replace: "-", " "}}</a>
{% endfor %}


You can style the tag menu and each tag section with height: 100vh;

Then add a back to top link at the bottom of each section. This looks less cluttered when you have lot of tags and posts.

Check out my full guide to [making a tag page in Jekyll](https://derekkedziora.com/blog/tag-page-jekyll).  

Back to the [main page](/).

{% for listOfTag in listOfTags %}
<h3 id='{{listOfTag}}'>{{listOfTag | replace: "-", " "}}</h3>
	
{% for post in site.posts %}

{% if post.tags contains listOfTag %}
<a href="{{post.url}}">{{post.title}}</a>
{% endif %}

{% endfor %}
{% endfor %}