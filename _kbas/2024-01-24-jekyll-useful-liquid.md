---
layout: post
title:  
date:   2024-01-24 00:00:00 -0800
description:
author: horacio 
image:  '/images/jekyll.jpg'
tags:   [kba, jekyll, liquid]
tags_color: '#477690'
---

- ### Escaping double curly braces inside a markdown code block in Jekyll

{% assign openTag = '{%' %}
{% raw %}
You can use {% raw %} to ensure content is unmodified by Jekyll:
{% endraw %}

{% assign openTag = '{%' %}
{% raw %}
```
{% raw %}
    This is inserted literally: {{foo}}
    I'm a code block, because I'm indented by 4 spaces
{% endraw %}{{ openTag }} endraw %}
```

- ### Citing the author of a blockquote using Markdown syntax

```
> Quote here.
>
> -- <cite>Benjamin Franklin</cite>
```

which results in:

> Quote here.
>
> -- <cite>Benjamin Franklin</cite>


- ### Create random numbers

{% raw %}
```
{% assign random = site.time | date: "%s%N" | modulo: site.data.inspirational-quotes.size %}

<blockquote>{{ site.data.inspirational-quotes[random].quote }}&rdquo; <cite>{{ site.data.inspirational-quotes[random].person }}</cite></blockquote>
```
{% endraw %}

The following example is for a number between 65 & 80.

{% raw %}
```
{% assign min = 65 %}
{% assign max = 80 %}
{% assign diff = max | minus: min %}
{% assign randomNumber = "now" | date: "%N" | modulo: diff | plus: min %}
```
{% endraw %}

- ### Sort Jekyll collection by date

This Liquid loop for Jekyll sorts a collection by date in reverse order

{% raw %}
```
{% comment %}
*
*  This loop loops through a collection called `collection_name`
*  and sorts it by the front matter variable `date` and than filters
*  the collection with `reverse` in reverse order
*
*  To make it work you first have to assign the data to a new string
*  called `sorted`.
*
{% endcomment %}
<ul>
    {% assign sorted = site.collection_name | sort: 'date' | reverse %}
    {% for item in sorted %}
    <li>{{ item.title }}</li>
    {% endfor %}
</ul>
```
{% endraw %}

- ### Pass variable to `include`

{% raw %}
```
[comment]: # (pass loop index)
{% for kba in site.kbas %}
  {% include article.html index = forloop.index %}
{% endfor %}

[comment]: # (call index as `include.index`)
{% assign random = site.time | date: "%s%N" | plus: include.index | modulo: 30 %}
<img class="lazy" data-src="{{site.baseurl}}/images/photo-{{ random }}.jpeg" alt="{{kba.title}}">
```
{% endraw %}
