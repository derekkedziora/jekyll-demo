---
title: "Now: A Self-Updating Page"
category: now
---

Check out my full guide to setting up a [dynamic now page](https://derekkedziora.com/blog/dynamic-now-page).

This page does everything I want: 

- Automatically updates 
- Includes each new "Now" entry in my RSS feed
- Doesn't include now pages on my post list 

Each now post needs to have the category "now" added to the front matter. Otherwise, you can write like a regular post. 

Make sure you add this to your `_config` file. You'll get your now posts in your regular RSS feed (example: [/feed.xml](https://demo.derekkedziora.com/feed.xml) and a second feed with just now posts to boot (example: [/feed/now.xml](https://demo.derekkedziora.com/feed/now.xml))

```
plugins:
  - jekyll-feed

feed: 
  categories: 
  - now
```

The only code on the static `now.md` you need to display the most recent now post is this: 

```
{% raw %}{{ site.categories.now[0].content }}{% endraw %}
```

Back to the [main page](/) or maybe a [random post](/random)? 