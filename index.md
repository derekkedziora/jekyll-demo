---
title: A Dark and Random Jekyll Demo
--- 

This is a quick demo of some handy things you can add to a Jekyll site. 

View the source code on GitHub. 

Check out my [main site](https://derekkedziora.com) or reach out to me at derekkedziora@icloud.com 

## Dark Mode Switch 

Read the [blog post](https://derekkedziora.com/blog/dark-mode-revisited) explaining how to add a dark mode switch to your Jekyll site. 

## Random Post 

You can build a random post link using client side JavaScript! Here's [how to do it](https://derekkedziora.com/blog/Getting-Random-Post-in-Jekyll). 

## Sample Blog Posts 

{% for post in site.posts %}

[{{ post.title }}]({{ post.url }})

{% endfor %}