---
layout: kba 
title: Passing post variables to includes in Jekyll
date:   2024-01-24 00:00:00 -0800
description: How to pass liquid variables defined in your post or pages layout into your site includes.
author: horacio 
image:  '/images/jekyll.jpg'
tags:   [kba, jekyll]
tags_color: '#477690'
---
By default Jekyll include documents loaded by your layout files do not have access to variables defined in the YAML header in your posts or pages. This can pose a bit of a problem if you want some parts of your site to have access to your post data (e.g. such as its title).

Luckily there is a way to pass variables into liquid includes however the official [documentation](http://jekyllrb.com/docs/templates/#includes) is not very clear on exactly how it works.

## Here is how it works
You pass in the variable in the include directive

{% raw %}
```
{% include sidebar.html links=page.relatedpages  %}
```
{% endraw %}

This code sends the page/post level variable `relatedpages` to sidebar.html and stores it in the variable `links` there.

Now in `sidebar.html` you have access to the `links` variable through `include.links`. You can now use the contents of this variable like any other liquid variable, e.g.

{% raw %}
```
{% if include.links %}
...some code..
{% endif %}
```
{% endraw %}

## Notes

You can pass in as many different variables as you like. In the example below there are two variables passed in to the sidebar.html include `links` and `title`.

{% raw %}
```
{% include sidebar.html links=page.relatedpages title=page.title %}
```
{% endraw %}

You can pass in absolute values as well by surrounding the value with quotes.

{% raw %}
```
{% include sidebar.html links=page.relatedpages title='My awesome page' %}
```
{% endraw %}

If you pass in multiple values with the same name then they overwrite each other (i.e. only the last value will be available). In the example below only the value "title2" will be available for variable `include.title` in the sidebar.html include.

{% raw %}
```markdown
{% include sidebar.html links=page.relatedpages title='title1' title='title2' %}
```
{% endraw %}

## Combining/Concatenating variables

If you want to combine argument values or concatinate them you will need to first capture the value in a new variable and then pass that into the include. In the example below I create a new variable `new_title` and then pass it into the include.

{% raw %}
    {% capture new_title %}Welcome to my page titled {{page.title}} have fun.{% endcapture %}

    {% include sidebar.html links=page.relatedpages title=new_title %}
{% endraw %}

More information on includes can be found in the official [documentation](http://jekyllrb.com/docs/templates/#includes) and on [Tom Johnson's](http://idratherbewriting.com/documentation-theme-jekyll/mydoc_alerts.html#use-liquid-variables-inside-parameters-with-includes) page.

---

> Retrieved from [https://blog.sverrirs.com/2016/10/jekyll-passing-post-variables-to-includes.html](https://blog.sverrirs.com/2016/10/jekyll-passing-post-variables-to-includes.html){:target="_blank"}