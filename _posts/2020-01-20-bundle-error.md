---
layout: post
title:  Jekyll Bundle Error
date:   2020-01-20 17:27:34 -0800
categories: jekyll 
description:
author: horacio 
image:  '/images/blog_tech6.jpg'
tags:   [technology, jekyll]
tags_color: '#477690'
---
When creating a new jekyll site, the following error occurs:

Retrying download gem from https://rubygems.org/ due to error (1/4): Bundler::PermissionError There was an
error while trying to write to `/usr/share/gems/cache/`. It is likely that you need to grant write permissions for that path.

The error message is indicating that there's a permission issue when to write to the gem cache directory (/var/lib/gems/3.0.0/cache). This often happens because some of the gem files are owned by root or another user, or the permissions are set incorrectly.
 
Run the following command:

{% highlight bash %}
  sudo chown -R $USER /usr/share/gems/
{% endhighlight %}

This command changes the owner of all files and directories under /usr/share/gems/ to the current user.
If changing the owner doesn't solve the problem, try to change the permissions of directory. 

