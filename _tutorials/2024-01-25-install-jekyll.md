---
layout: post
title:  Installing Jekyll
date:   2024-01-25 00:00:00 -0800
description: Install Jekyll - a simple, blog aware static site generator Ruby Gem.
author: horacio 
image:  '/images/jekyll.jpg'
tags:   [technology, jekyll, tutorial]
tags_color: '#477690'
---

Jekyll is a Ruby Gem that can be installed on most systems. It's a straightforward process on both Mac and Linux, and only slightly more involved on Windows. Either way, it won't take you long to get set up with Jekyll!

See [Jekyll docs](https://jekyllrb.com/docs){:target="_blank"} for more info

## How to install Jekyll

Jekyll is a Ruby Gem, which means you will need to install a couple of dependencies to allow the Gem to run on your system.

## You will need:

1. [Ruby][1]{:target="_blank"} version 2.4.0 or higher, including all development headers (check by running the command ruby -v)
2. [RubyGems][2]{:target="_blank"} (check by running the command gem -v)
3. [GCC][3]{:target="_blank"} (check by running the command gcc -v, g++ -v)
4. [Make][4]{:target="_blank"} (check by running the command make -v)

[1]: https://www.ruby-lang.org/en/downloads
[2]: https://rubygems.org/pages/download
[3]: https://gcc.gnu.org/install
[4]: https://www.gnu.org/software/make

For a step-by-step walkthrough to help you install these, head to the Jekyll installation guides and follow the instructions for your system.

## Install Jekyll

Once you have done that you are ready to install the Jekyll gem. Go to your command line interface and run

```bash
gem install jekyll bundler
```

## Final installation check

To check that the Jekyll installation has worked properly, run the following command:

```bash
jekyll -v
```

## Create and run your first Jekyll project

Let’s get started by creating a basic Jekyll project and taking a look at it. With your preferred command-line tool, navigate to somewhere you would like to create the project and run:

```bash
jekyll new learn-jekyll
```

We’ve given the project the name “learn-jekyll” for now, but you can use whatever name you’d like. When this is done, navigate into the newly created project folder with your command-line tool and run:

```bash
bundle exec jekyll serve
```

This will “build” your site and make it viewable on your web browser. Any time you make any changes, this will trigger a “rebuild” so that you don’t have to run this command again. Now, open your browser on:

```bash
http://127.0.0.1:4000/
```

You should see a minimal but pleasant blog - all from a few commands. If you want to stop the project at any time, use Ctrl + C. Now let’s look at how a Jekyll project works.

## Basic Jekyll structure

Jekyll is a “convention over configuration” framework, and the basic setup is quite simple. You should now see two main folders - `_posts` and `_site` (you can ignore `.jekyll-cache` altogether):

- `_posts` is simply where your blog posts will go in future.
- `_site` is where your finished site is “built”. In other words, this is where your viewable website will be created - ready for deployment. Any files such as CSS, JS, and images will also end up here in an `assets` folder.

There are some other files worth mentioning too:

- `_config.yml` is where you manage the configuration for your project, like global variables, “collections”, or default names/paths. This where a lot of customization is done.
- `.gitignore` is for files/folders you don’t want to save into version control (e.g., information you don’t want available publicly).
- `Gemfile/Gemfile.lock` is how you manage any extensions to Jekyll.

You might have also noticed a number of Markdown files. These are used to make it easy to write content - especially blog posts. In fact, there are no about.html and index.html by default. These are actually built into HTML - automatically - from `about.markdown` and `index.markdown` into the `_site` folder.

## Further conventions

In addition to these basics, you can also manually add other folders with specific names that Jekyll will recognize. We will set these up in future lessons, but for now it’s just good to know about them:

- `_data:` any “data” files your site needs (like a small database)
- `_drafts:` posts that you don’t want automatically published
- `_layouts:` files that you want to use as a “frame” for specific pages - e.g., the layout for all of your posts
- `_includes:` parts of HTML files you want to reuse in multiple pages - e.g., navigation, footer.

## Building and serving your website

There are a few different commands worth looking at for different purposes in Jekyll. For more detail, see the Jekyll Command Line page.

- `bundle exec jekyll serve` - when **developing** your site, you’ll want to create your site’s files as well as serve them so that you can view the site in the browser.
- `jekyll build` - when **deploying** your site to production, you’ll just want to build its files.
- `jekyll help` - run this if you need general command-line help, or `jekyll help` `<command name>` for more specific help.

For local development, you can also use `jekyll serve`, but we recommend the slightly longer `bundle exec jekyll serve`. Don’t worry much about the difference - this is just so the versions you installed locally are used (and not some other version), which might save you some troubleshooting.

> [Checkout](/blog/welcome-to-jekyll) the welcome page