---
permalink: /random
--- 

<script>
// this stops a white flash from happening while the random post script is running

let theme = sessionStorage.getItem('theme');
if (theme === "dark") {
  document.documentElement.setAttribute('data-theme', 'dark');
} else if (theme === "light") {
  document.documentElement.setAttribute('data-theme', 'light');
}

</script>

{% comment %}
Use liquid to get an the number of posts in the site
{% endcomment %}

{%- assign i = 0 -%}
{%- for post in site.posts -%}
    {%- assign i = i | plus: 1 -%}
{%- endfor -%}

<script>

  const comingFromPost = document.referrer; 

  const allPosts = 
    [{%- for post in site.posts -%}
    {%- unless post.unlisted -%}
      {%- assign i = i | minus: 1 -%}
      "{{ site.url }}{{ post.url }}"{%- unless i == 0 -%},{%- endunless -%}
    {%- endunless -%}
    {%- endfor -%}];

  function linkToRandomBlogPost() {
      const randomPostLink = allPosts[Math.floor(Math.random() * allPosts.length)];
      return randomPostLink;
  }

  location.replace(linkToRandomBlogPost())

</script>

<noscript mardown="1">

# Random Blog Post

To get a random post, turn on JavaScript! 

</noscript>

