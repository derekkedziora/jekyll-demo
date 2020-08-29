---
title: A Dark and Random Jekyll Demo
--- 

This is a quick demo of some handy things you can add to a Jekyll site. 

View the [source code on GitHub](https://github.com/derekkedziora/jekyll-demo). 

Check out my [blog](https://derekkedziora.com) or get in touch at derekkedziora@icloud.com 

## Dark Mode Switch 

Read [my guide to dark mode](https://derekkedziora.com/blog/dark-mode-revisited) to see how I created the dark mode switch on this Jekyll site. 

Make sure you have the mode toggle on each page, otherwise you'll always display the system color preference.

## Random Post 

You can build a random post link using client side JavaScript! Here's [how to do it](https://derekkedziora.com/blog/Getting-Random-Post-in-Jekyll), or you can go to a [random post](/random). 

## Now Page 

Check out my dynamic [now page](/now).

## Tag Page 

Jekyll doesn't have a built-in tag page, but it's easy to make your own. Here' my guide to [making a tag page](https://derekkedziora.com/blog/tag-page-jekyll).

Here's my [demo tag page](/tags).

## Demo Blog Posts 

{% for post in site.posts %}
{% unless post.categories contains "now" %}

[{{ post.title }}]({{ post.url }})

{% endunless %}
{% endfor %}