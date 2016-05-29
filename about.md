---
layout: page
permalink: /about/index.html
title: Serge Ballif
tags: 
  - Serge
  - Ballif
imagefeature: fourseasons.jpg
chart: true
published: true
---
<figure>
  <img src="{{ site.url }}/images/SergeBallif.jpg" alt="Serge Ballif">
</figure>

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}

My name is **Serge Ballif**, and I am a mathematician at Nevada State College. I love teaching and sharing ideas. I am a strong believer that everyone can enjoy and succeed in mathematics. I have a Ph.D. in Mathematics from The Pennsylvania State University, a M.S. in Mathematics from Utah State University, and a B.S. in Mathematics from Utah State University. I have a wonderful wife and three entertaining children who are good at keeping me busy and smiling. 


