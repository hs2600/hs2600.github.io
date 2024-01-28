---
layout: post
title:  19 Best Laravel Tutorials (Free and Paid Resources)
date:   2024-01-26 01:00:00 -0800
description:
author: horacio 
image:  '/images/laravel.jpg'
tags:   [technology]
tags_color: '#477690'
---

Laravel has been the rock star of PHP application development for many years and with a good reason. Huge ecosystem, active community, strong job market, successful startups — it has everything that makes it worthwhile to adopt a new technology.

If you want to learn Laravel, you need not go further. By browsing through this guide, you can find the best Laravel tutorial for you, matching your knowledge level and learning style.

Ready? Let’s dig deeper!

### Table of Contents

1.  [Why Learn Laravel](#why-learn-laravel)
2.  [How to Learn Laravel](#how-to-learn-laravel)
3.  [5 Best Free Laravel Tutorial Sites](#5-best-free-laravel-tutorial-sites)
4.  [6 Best Free Laravel Tutorial Videos, Screencasts, and Podcasts](#6-best-free-laravel-tutorial-videos-screencasts-and-podcasts)
5.  [8 Best Paid Laravel Tutorial Videos, Screencasts, and Books](#8-best-paid-laravel-tutorial-videos-screencasts-and-books)

Why Learn Laravel[](#why-learn-laravel)
---------------------------------------

There are many reasons why you might want to learn Laravel, so we’ll start with the most important of them. Plus, we’ll also go through some tips on how to efficiently learn the framework before looking into the best Laravel tutorials in detail, including the pros, cons, and use cases of each tutorial.

### 1\. Rapid Development[](#1-rapid-development)

[Laravel](https://laravel.com) is an open source PHP framework for web application development, based on the MVC (Model-View-Controller) architectural pattern. Its expressive and straightforward syntax speeds up development and results in a clean and maintainable codebase and scalable applications.

### 2\. High Popularity[](#2-high-popularity)

[Laravel’s source code](https://github.com/laravel/laravel) is hosted on GitHub where it’s the most popular PHP repository, with more than 60,000 stars and counting. There are also many Laravel tutorials, videos, screencasts, and resources available online that can help you learn the framework and stay up to date with new developments.

### 3\. Huge Ecosystem[](#3-huge-ecosystem)

Thanks to its popularity, Laravel has a massive ecosystem of both official and third-party packages that you can add to your own application. The official packages include server management tools and platforms, developer environments, monitoring and testing tools, an administration panel, and more (see them on [Laravel’s homepage](https://laravel.com) under the ‘Ecosystem’ menu).

If you want to add functionality that doesn’t yet exist, you can also [develop your own Laravel package](https://laravel.com/docs/8.x/packages).

### 4\. Active Community[](#4-active-community)

There’s a huge community around Laravel that you can find on [Laravel.io](https://laravel.io), [Laracasts Discuss](https://laracasts.com/discuss), [LaraChat](https://larachat.co), [Discord](https://discord.com/invite/KxwQuKb), [Reddit](https://www.reddit.com/r/laravel), and other cool places. Laravel also has an official conference called [Laracon](https://laracon.net) that takes place every year on three continents (America, [Europe](https://laracon.eu), [Australia](https://laracon.com.au)).

### 5\. Strong Job Market[](#5-strong-job-market)

Laravel development is a highly in-demand skill and job prospects are excellent. It has an official job board called [Larajobs](https://larajobs.com) where the most common job titles are ‘Laravel Developer’, ‘Backend Laravel Developer’, ‘Full-Stack PHP Developer‘ (Laravel is frequently paired with Vue.js on the frontend), and ‘TALL Stack Developer’ (TALL stands for [Tailwind CSS](https://tailwindcss.com), [Alpine.js](https://github.com/alpinejs/alpine), Laravel, and [Livewire](https://laravel-livewire.com)).

Besides Larajobs, you can find multitudes of Laravel jobs on other job sites such as Monster, Indeed, and LinkedIn, and remote Laravel jobs are also available at [RemoteOK](https://remoteok.io/remote-laravel-jobs), [We Work Remotely](https://weworkremotely.com/remote-jobs/search?utf8=%E2%9C%93&term=laravel),  and other places.

### 6\. Promising Business Opportunities[](#6-promising-business-opportunities)

If you don’t want to work for someone else but build your own business, Laravel can also be an excellent solution for you. There are already many successful businesses built on Laravel, such as [OctoberCMS](https://octobercms.com), [Mailcoach](https://mailcoach.app), [Monica CRM](https://www.monicahq.com), [Invoice Ninja](https://www.invoiceninja.com), and [CodeCourse](https://codecourse.com) (see below in this article, among paid Laravel tutorials), to just name a few.

With Laravel as a foundation and using best practices and high-performing PHP hosting, your app will scale in production without any problems.

How to Learn Laravel[](#how-to-learn-laravel)
---------------------------------------------

To get started with learning Laravel development, you’ll need some pre-existing knowledge.

### Prior Knowledge[](#prior-knowledge)

You’ll need to safely use PHP, especially object-oriented PHP. Knowing how to use the command line and the [Composer](https://getcomposer.org) package manager is also important — these two topics are usually covered by [beginner-level PHP tutorials](/blog/php-tutorials).

Some knowledge of HTML and relational database management systems (Laravel supports four of them: MySQL, PostgreSQL, SQLite, and SQL Server) can also be helpful for an easy start.

### Learning Materials[](#learning-materials)

Learning a PHP framework such as Laravel is somewhat different from learning a programming language such as PHP. Here, you’ll do more hands-on projects and fewer (or zero) programming exercises from the start, as this is how most Laravel tutorials are structured.

Building real-world apps also means that you’ll frequently use Laravel as part of a stack. For instance, many Laravel tutorials use it with a Vue frontend, which means that you’ll also need to learn Vue.js (usually also covered by the same tutorial) to accomplish the project.

It’s also harder to find tutorials for complete beginners and most tutorials are in video format. There are barely any books on Laravel mainly because changes so quickly that by the time a book gets published, the framework is already two versions ahead.

### Laravel Versions[](#laravel-versions)

One of the most important things when picking a Laravel tutorial is paying attention to the Laravel version it covers. You’ll need to be familiar with the following Laravel versioning rules:

*   Since version 6, Laravel and its official packages follow [semantic versioning](https://laravel.com/docs/8.x/releases#versioning-scheme) (`major.minor.patch`), for instance 8.\* is a major release.
*   Before Laravel 6, the framework used the `paradigm.major.minor` convention, for instance 5.8.\* is also a major release.
*   There’s a major release every six months (in February and August).
*   And, there’s one LTS (long-term support) release every 2 years.
*   For general releases, bug fixes are provided for 6 months and security releases are provided for 1 year.
*   For LTS releases, bug fixes are provided for 2 years and security releases are provided for 3 years.
*   So, Laravel’s subsequent major releases are numbered as 5.5.\* (LTS), 5.6.\*, 5.7.\*, 5.8.\*, 6.\* (LTS), 7.\*, 8.\*
*   There are also minor releases and patches, but they don’t contain any breaking changes.

As there are two major releases every year, tutorials can hardly follow along. Most Laravel tutorials you’ll find at any given date will be 1-3 versions back compared to the actual release. This is not a huge problem unless the framework undergoes a complete overwrite, which last happened when Laravel 4 was released in 2013.

Even though it’s recommended to use the latest tutorial available, don’t panic if you have to go back two or three releases, especially if it’s a practical piece that shows how to build the kind of application you want to learn.

You might find some inconsistencies between the different versions, but these are usually noted by either the author or other learners in the discussion section. It’s also a good idea to browse through the [release notes](https://laravel.com/docs/8.x/releases) of each new release to see what has changed, as it can help you know what to pay attention to.

### Learning Budget[](#learning-budget)

Learning Laravel is not expensive at all — you can do it even for free. This guide includes both free and paid Laravel tutorials, but even the paid ones are not very pricey; you can subscribe to a premium tutorial site for ~15-30 USD/month.

Even if you don’t want to spend any money on learning Laravel, it’s also worth browsing through the paid section, as some of the premium tutorial sites come with free trials, occasional free video courses, and other free offerings.

5 Best Free Laravel Tutorial Sites[](#5-best-free-laravel-tutorial-sites)
-------------------------------------------------------------------------

Now, let’s take a closer look at the best Laravel tutorials!

### 1\. Official Laravel Docs (Beginners, Intermediate, Advanced)[](#1-official-laravel-docs-beginners-intermediate-advanced)

The [official Laravel documentation](https://laravel.com/docs) is a matter-of-fact description of the Laravel framework, maintained by the Laravel community and also [available on GitHub](https://github.com/laravel/docs). It starts with an installation guide and provides an overview of all Laravel concepts, such as templating, security, database management, and many others. You can also find the documentation of official Laravel packages here.

**Pros:**

*   most up-to-date Laravel resource
*   information is well-structured and easy to search
*   docs for older Laravel versions are also available
*   includes code examples and best practice tips
*   you can submit [bug reports](https://github.com/laravel/docs/blob/8.x/contributions.md) on GitHub

**Cons:**

*   dry, textbook-like tone and design

#### When to Choose Laravel Docs[](#when-to-choose-laravel-docs)

The official Laravel documentation is useful at any knowledge level for checking out the details of any Laravel-related concept. However, it can be overwhelming for beginners because of its high information density.

It’s the best place to familiarize yourself with the features of new releases or compare different releases.

### 2\. Laravel News (Beginners, Intermediate, Advanced)[](#2-laravel-news-beginners-intermediate-advanced)

[Laravel News](https://laravel-news.com) is an all-inclusive Laravel tutorial site with multiple facets. It has a blog featuring the latest Laravel news, a section for Laravel tutorials covering topics from beginner to expert level, a bi-weekly Laravel podcast, and a Laravel newsletter that delivers every Sunday morning. Laravel News also showcases popular Laravel packages with a brief description and example code.

**Pros:**

*   regularly updated
*   delivers content in different ways blog, podcast, newsletter, etc)
*   best practice pieces
*   free tutorials on building real-world Laravel apps/tasks/tools
*   helpful screenshots and code snippets

**Cons:**

*   some of the posts are sponsored posts (even though it’s clearly stated)
*   hard to navigate (consecutive parts of the same tutorial series are not linked to each other)

#### When to Choose Laravel News[](#when-to-choose-laravel-news)

Laravel News is the best free source for Laravel-related news. The tutorials are high-quality and cover many interesting things — but even if you are not interested in them, it’s worth subscribing to the newsletter to stay up to date with the Laravel framework (each edition includes some Laravel job listings, too). The bi-weekly Laravel News Podcast is also an excellent resource for Laravel developers at any level.

### 3\. Tuts Make (Intermediate, Advanced)[](#3-tuts-make-intermediate-advanced)

[Tuts Make](https://www.tutsmake.com/category/laravel-tutorial) is a popular tutorial blog covering [different programming languages](/blog/scripting-languages) and technologies, including Laravel. The tutorials are succinct and up-to-the-point, discussing common Laravel tasks, errors, and use cases. They include multiple code snippets that you can also use in your own projects.

TutsMake has a separate category for [Laravel interview questions and answers](https://www.tutsmake.com/laravel-interview-questions-answers-for-1235-year-experience), too, with straightforward and thoughtful explanations.

**Pros:**

*   regularly updated
*   practice-based tutorials
*   easy-to-skim content
*   long but well-structured code examples
*   job interview Q&A

**Cons:**

*   tutorials are hard to browse (no tags or other taxonomies)
*   grammar errors here and there

#### When to Choose Tuts Make[](#when-to-choose-tuts-make)

Tuts Make is definitely not for beginners. You’ll need at least an intermediate knowledge of Laravel to understand these tutorials, as they are very code-based, without much discussion of theory. The tutorials are also not related to each other — Tuts Make is a blog, not a step-by-step Laravel tutorial series. If you are looking for a Laravel job, don’t miss out on its interview Q&A section; it’s really good.

### 4\. LaraShout (Beginners, Intermediate, Advanced)[](#4-larashout-beginners-intermediate-advanced)

[LaraShout](https://www.larashout.com) is a free tutorial website focusing completely on the Laravel framework. Besides hands-on Laravel tutorials, it also features guides on important theoretical concepts such as middleware, storage, queues and jobs, and others. Some of the tutorials are grouped as series so that you can get a deeper knowledge of each topic.

Currently, LaraShout has four series: Collections, Design Patterns, E-Commerce Application Development, and Package Development.

**Pros:**

*   easy-to-navigate website
*   tutorials start with a table of content
*   rich content (high-quality images, code examples, alert messages, etc)
*   both theory- and practice-based tutorials

**Cons:**

*   some categories include just two or three tutorials
*   less frequently updated

#### When to Choose LaraShout[](#when-to-choose-larashout)

LaraShout is primarily recommended for intermediate and advanced learners, even though it also has some beginner-level tutorials. The four Laravel tutorial series are especially worth checking out — however, note that they don’t necessarily cover everything you’ll need, as LaraShout is more of a tech blog than a comprehensive educational site.

### 5\. Learn2torials (Beginners, Intermediate)[](#5-learn2torials-beginners-intermediate)

[Learn2torials](https://learn2torials.com/category/laravel) is a one-person project by Sandip Patel, featuring free tutorials on different programming languages and frameworks. The Laravel tutorial section covers many important aspects of the framework, from installation to backups to caching.

They focus more on theory than practice, but as they include many longer code examples, they can help you solve real-world problems, too.

**Pros:**

*   well-written tutorials with thoughtful explanations
*   tutorials use an easy-to-follow question and answer format
*   well-commented code examples
*   many beginner-level tutorials

**Cons:**

*   hard to search website (no taxonomies)
*   tutorials don’t follow a logical order, from beginner pieces to more advanced ones

#### Why Choose Learn2torials[](#why-choose-learn2torials)

If you are a beginner or already know some Laravel development but there are gaps in your knowledge, Learn2torials can be the ideal Laravel resource for you. It also has many overlaps with the official Laravel docs, so you can use the two resources together to solidify your understanding of the underlying concepts.

6 Best Free Laravel Tutorial Videos, Screencasts, and Podcasts[](#6-best-free-laravel-tutorial-videos-screencasts-and-podcasts)
-------------------------------------------------------------------------------------------------------------------------------

### 1\. BitFumes (Beginners, Intermediate, Advanced)[](#1-bitfumes-beginners-intermediate-advanced)

[BitFumes](https://bitfumes.com) is an educational website featuring both free and paid screencasts and video courses in web development. Its [free Laravel tutorial section](https://bitfumes.com/courses/laravel) includes many high-quality video courses aimed mainly at beginners, but you can find some more advanced pieces here, too.

There are also many free Laravel tutorials on [BitFumes’ YouTube channel](https://www.youtube.com/c/Bitfumes/playlists), including a [6.5 hours-long course](https://www.youtube.com/watch?v=BXiHvgrJfkg) covering Laravel development from the very basics to advanced topics such as [Livewire](https://laravel-livewire.com) (needed for the TALL stack).

**Pros:**

*   you don’t need to sign up to watch the free courses
*   videos are structured into chapters and lessons
*   progress tracking functionality
*   tutorials on common tool pairings (Laravel with DigitalOcean, VueJS, PHPUnit, etc.)
*   courses are properly labeled (length, level, number of tutorials, publication date)

**Cons:**

*   hard-to-understand ecosystem (there are free Laravel courses both on the website and YouTube, and it has one premium course)

#### When to Choose BitFumes[](#when-to-choose-bitfumes)

BitFumes’ YouTube channel is worth browsing through in any case, even if you are at an advanced level. The free tutorials on the BitFumes website cover many beginner-level topics that are hard to find for free elsewhere. It also has [one premium Laravel course](https://bitfumes.com/premium/in-depth-laravel) including advanced topics such as Stripe integration and test-driven development.

### 2\. Laravel Business by Povilas Korop (Beginners, Intermediate, Advanced)[](#2-laravel-business-by-povilas-korop-beginners-intermediate-advanced)

[Laravel Business](https://www.youtube.com/channel/UCTuplgOBi6tJIlesIboymGA/featured) is a popular YouTube channel including free video tutorials on how to use Laravel for business. It’s a one-person project by Povilas Korop who is also the author of Laravel Daily (see below in the paid section).

On his channel, he publishes several YouTube videos every week, discussing topics such as Blade, Eloquent, PHPUnit, SaaS applications, and many others. Besides hands-on tutorials, Povilas also does comparisons, provides career and business advice, and under the ‘Community’ tab, he shares the ‘Laravel tip of the day’ on a daily basis.

**Pros:**

*   updated almost every day
*   _very_ practice-based tutorials
*   longer videos are broken into smaller sections
*   ‘Related Links’ recommendations under tutorial videos
*   sometimes he replies to his viewers in video answers ([see example](https://www.youtube.com/watch?v=O3-UstubSYU))

**Cons:**

*   videos are hard to search through

#### When to Choose Laravel Business[](#when-to-choose-laravel-business)

Even though Laravel Business is primarily aimed at more advanced users, it can also be a great Laravel resource for beginners, especially Povilas’ business and career advice.

If you have been doing Laravel development for a while and are a bit bored with your job, this channel can help you gain back your motivation, as it discusses many interesting things, new features, and specific use cases you won’t find elsewhere.

### 3\. Laraning (Beginners, Intermediate)[](#3-laraning-beginners-intermediate)

[Laraning](https://www.laraning.com)‘s name comes from the words ‘Laravel’ and ‘learning’, and it stays true to this name as it’s fully dedicated to Laravel learning. It features free video courses, categorized as ‘Series’, ‘Features’, and ‘Courses’.

‘Series’ are loosely coupled video tutorials on Laravel packages and other topics. ‘Features’ are still under development and currently includes only one video tutorial on the Blade templating engine. ‘Courses’ are longer video tutorial series, such as the comprehensive ‘Laravel from A to Z’ course aimed at beginner learners.

**Pros:**

*   well-structured courses
*   easy-to-navigate website
*   practical, real-world examples
*   full HD videos
*   code content is [available on GitHub](https://github.com/laraning)

**Cons:**

*   still under development
*   no publication date on videos

#### When to Choose Laraning[](#when-to-choose-laraning)

As the Laraning website is not fully baked yet, you’ll find missing features here and there. For instance, the ‘Sign In’ button still doesn’t work and some of the series include only two video pieces. However, the tutorials that are already published are high-quality and definitely worth checking out, especially the Laravel from A to Z course if you are just getting started with the framework.

### 4\. Laravel PHP Framework Tutorial by FreeCodeCamp (Beginners, Intermediate)[](#4-laravel-php-framework-tutorial-by-freecodecamp-beginners-intermediate)

[Laravel PHP Framework Tutorial](https://www.youtube.com/watch?v=ImtZ5yENzgE) is a beginner-level video course by the FreeCodeCamp online learning platform. Even though the backend part of FreeCodeCamp’s curriculum centers around Python, it also shares educational videos on other backend languages on its Youtube channel, created by members of its open source community.

This Laravel tutorial by Victor Gonzalez guides you through building an Instagram clone from scratch, with functionalities such as follow/unfollow, profile editing, resizing images, and others. The video is around 4.5 hours long, but it’s broken into smaller sections so that you can easily follow through.

**Pros:**

*   real-world project
*   in-depth explanation
*   audited by FreeCodeCamp
*   demo code available on [GitHub](https://github.com/coderstape/freecodegram)
*   community members help with questions in the comment section

**Cons**

*   based on Laravel 5.8, so might contain some outdated info (even though you can find fixes for these issues in the comment section)

#### When to Choose Laravel PHP Framework Tutorial by FreeCodeCamp[](#when-to-choose-laravel-php-framework-tutorial-by-freecodecamp)

If you want to learn Laravel through building the clone of a highly popular, real-world application, this is one of the best places to do that for free. Victor’s explanations are thoughtful and easy to understand and the FreeCodeCamp community is very helpful if you bump into issues.

Although it’s aimed at beginners, you might also find it useful if you already have some Laravel knowledge but want to learn how to put together an Instagram-like application.

### 5\. Let’s Build with Laravel: A Linktree Clone (Beginners, Intermediate)[](#5-lets-build-with-laravel-a-linktree-clone-beginners-intermediate)

[Let’s Build with Laravel: A Linktree Clone](https://www.youtube.com/watch?v=30qk04BG9G4) is a fast-paced Laravel screencast that teaches you how to build a social media landing page builder application similar to the popular [Linktree](https://linktr.ee) service.

The video is only 58 minutes long, as it doesn’t explain basic concepts or shows [how to install Laravel](/tutorial/install-laravel), but goes straight into practice. This free Laravel tutorial has been created by Andrew Schmelyun who has [several other Laravel videos](https://www.youtube.com/playlist?list=PL36CGZHZJqsXntCJceGN8J2B9wFZD7GFe) on his YouTube channel that are also worth checking out.

**Pros:**

*   to-the-point explanation with no fluff or distraction
*   you can build a working Laravel app in less than 1 hour
*   video is divided into smaller sections
*   source code is [available on GitHub](https://github.com/aschmelyun/laravel-links)

**Cons:**

*   audio quality is not the best

#### When to Choose ‘Let’s Build with Laravel: A Linktree Clone’[](#when-to-choose-lets-build-with-laravel-a-linktree-clone)

Although the video’s description on Youtube says that it’s meant for beginners, if you are completely new to Laravel, you need to keep in mind that this video assumes some pre-existing knowledge of Laravel, such as installation or initial configuration.

This Laravel tutorial can be ideal for building your first app with the framework, but also if you want to improve your application development skills.

### 6\. The Laravel Podcast (Beginners, Intermediate, Advanced)[](#6-the-laravel-podcast-beginners-intermediate-advanced)

[The Laravel Podcast](https://laravelpodcast.com) is a bi-weekly podcast hosted by Matt Stauffer, featuring Laravel- and PHP-related discussions. Each episode centers around one topic, such as authentication, migrations, debugging, setting up a local environment, and others. The episodes are around 1.5 hours long, and you can listen to them either using the embedded podcast player or on Apple Podcasts.

**Pros**

*   information-heavy content
*   regular updates
*   episodes are well-documented (summary, notes, link recommendations)
*   transcripts are available
*   high-quality audio

**Cons**

*   episodes can’t be downloaded

#### When to Choose The Laravel Podcast[](#when-to-choose-the-laravel-podcast)

Even though a podcast is not a classic tutorial, it’s an excellent way to familiarize yourself with a new technology, hear the views of industry experts, and get updated with the latest features. So, The Laravel Podcast is a highly recommended Laravel resource for developers at any level.

8 Best Paid Laravel Tutorial Videos, Screencasts, and Books[](#8-best-paid-laravel-tutorial-videos-screencasts-and-books)
-------------------------------------------------------------------------------------------------------------------------

### 1\. Laracasts (Beginners, Intermediate, Advanced)[](#1-laracasts-beginners-intermediate-advanced)

[Laracasts](https://laracasts.com) is a premium educational platform offering screencasts on web development. Although its primary focus is the Laravel framework, it also has courses on other technologies, most of which can be used together with Laravel, such as CSS, JavaScript, PHP, SQL, Vue.js, and more.

It also features five [Laracast Journeys](https://laracasts.com/skills/laravel): Laravel, Testing, PHP, JavaScript, and Tooling. A Journey is a collection of screencasts that you need for mastering a given skill.

**Pros:**

*   screencasts are structured in three different ways (topics, series, journeys)
*   easy-to-navigate website
*   very high-quality screencasts (both audio and video)
*   also have screencasts on popular Laravel packages (Envoyer, Forge, Nova, etc) and theory (SOLID principles, design patterns, etc.)
*   active discussion forum (available with a free forum account)

**Cons:**

*   no free trial period

#### When to Choose Laracasts[](#when-to-choose-laracasts)

Laracasts are high-quality video tutorials, recommended at every level. Even though it’s a premium service, you can find some series that are completely free, for instance, an [intermediate series on Envoyer](https://laracasts.com/series/envoyer) and a [beginner series on Forge](https://laracasts.com/series/learn-laravel-forge). However, you can’t filter for free courses, so you’ll need to find them by yourself.

Even if you don’t want to pay for the membership, it’s also worth signing up for a free forum account, especially if you need some community help with your code.

### 2\. Laravel Daily (Beginners, Intermediate, Advanced)[](#2-laravel-daily-beginners-intermediate-advanced)

[Laravel Daily](https://laraveldaily.teachable.com) is the paid Laravel tutorial site of Povilas Korop, the creator of the aforementioned Laravel Business Youtube channel. Povilas has 10 paid and one free Laravel video tutorial series here, covering interesting topics such as creating an invoice making app with Laravel, building a CRUD SPA with Laravel and Vue, mastering Eloquent, creating a REST API with Laravel, and more.

**Pros:**

*   live coding of real-world Laravel projects
*   well-documented, logically structured course content
*   one free [practical crash course for beginners](https://laraveldaily.teachable.com/p/laravel-for-beginners-your-first-project)
*   all code examples are [available on GitHub](https://github.com/LaravelDaily)
*   you can enroll/pay via the secure Teachable platform
*   you can send your questions to Povilas by email

**Cons**

*   there’s no publish date on the courses (although you can guess it from the commit history of the related GitHub repo)

#### When to Choose Laravel Daily[](#when-to-choose-laravel-daily)

Laravel Daily is recommended for Laravel developers at any level. If you are already a subscriber to the Laravel Business channel and like Povilas’ teaching style, his paid video courses on Laravel Daily can be the next logical step in your Laravel journey.

It’s also an excellent choice if you want to acquire skills that are in high demand on the job market, such as API or SaaS development with Laravel.

### 3\. CodeCourse (Intermediate, Advanced)[](#3-codecourse-intermediate-advanced)

[CodeCourse](https://codecourse.com) is a premium screencast platform for web development tutorials. Most of the screencasts are structured as ‘Paths’ and are available in four categories: Flutter, Vue.js, Laravel, and design patterns.

The [Clean Laravel](https://codecourse.com/courses/clean-code-laravel) path consists of a video course and teaches you how to write high-quality, clean Laravel code. CodeCourse also has a shorter Laravel path called [Filtering with Laravel](https://codecourse.com/courses/filtering-in-laravel). Besides the paths, CodeCourse features [single courses](https://codecourse.com/library), too, where you can learn how to build different types of apps with Laravel, including a Twitter clone, a code snippet website, and an e-commerce platform.

**Pros:**

*   new content is regularly added
*   abundant information on paths and courses
*   high-quality screencasts (both video and audio)
*   focuses on hands-on skills
*   features short screencasts called [‘Snippets’](https://codecourse.com/courses/build-a-code-snippet-website-with-me) for free
*   intro videos are available for free

**Cons:**

*   poorly structured website (it’s not clear that they have different types of content, single courses are only available from the ‘Library’ menu, ‘Snippets’ are hard to find, etc)
*   no free trial

#### When to Choose CodeCourse[](#when-to-choose-codecourse)

To benefit from CodeCourse’s Laravel screencasts, you’ll need to be familiar with the basics of Laravel development. However, if you have an intermediate knowledge of the framework or are already working in the industry, you can learn many new things here.

Even though it’s a premium service, it’s really not expensive, so if you find a course or path you are interested in, it’s a good investment of your time and effort.

### 4\. Building APIs and SPAs with Laravel, Vue.js, and Capacitor (Advanced)[](#4-building-apis-and-spas-with-laravel-vuejs-and-capacitor-advanced)

Building APIs and SPAs with Laravel, Vue.js, and Capacitor

[The Ultimate Guide to Building APIs & Single-Page Applications with Laravel, Vue.js, and Capacitor](https://serversideup.net/ultimate-guide-to-building-apis-and-spas-with-laravel-and-vuejs) is an ebook by Dan Pastori and Jay Rogers, available on ServerSideUp. It covers how to develop web and mobile applications from the same codebase — where all your apps communicate with a centralized API.

The book goes through the process of building a real-world app called Roast, a coffee house finder application. It’s not just a demo but an [existing app](https://roastandbrew.coffee) that allows you to sign up, add your favorite cafe, find coffee houses on a map, and more. You can install the Roast app on your [Android](https://play.google.com/store/apps/details?id=coffee.roastandbrew.mobile) or [iOS](https://apps.apple.com/us/app/roast-brew-coffee/id1510419686) device too.

**Pros:**

*   written by industry experts
*   well-structured content (table of content is available on the sales page)
*   two free chapters (however, you need to sign up to the ServerSideUp newsletter to get them)
*   optimized Sketch and Figma icon templates for Capacitor
*   available in three different formats (PDF, EPUB, MOBI)
*   access to a private online community to get help (only if you buy the more expensive package)
*   lifetime access and updates
*   a couple of free, [advanced-level Laravel tutorials](https://serversideup.net/search/?type=courses) on the ServerSideUp site

**Cons:**

*   additional video tutorials (advertised as part of the more expensive package) are still under construction

#### When to Choose ‘Building APIs and SPAs with Laravel, Vue.js, and Capacitor’[](#when-to-choose-building-apis-and-spas-with-laravel-vuejs-and-capacitor)

If you are already a seasoned Laravel developer, this ebook can expand your expertise and further broaden your knowledge. It guides you through how to support three codebases (web, iOS, Android) while building a complex application.

It also pairs Laravel with cutting edge tools — the [Nuxt.js](https://nuxtjs.org) frontend framework (built on top of Vue.js) and the [Capacitor](https://capacitorjs.com) cross-platform runtime ([see docs](https://capacitorjs.com/docs)). Plus, it covers Laravel 8, so right now it’s the freshest Laravel book available on the market (already 380 pages and new chapters are still coming).

### 5\. LinkedIn Learning (Beginners, Intermediate)[](#5-linkedin-learning-beginners-intermediate)

LinkedIn Learning, previously called Lynda.com, is a premium e-learning platform that offers a complete [learning path in Laravel development](https://www.linkedin.com/learning/paths/become-a-laravel-developer).

It consists of five separate courses, starting with (1) Laravel basics, then covering (2) testing, security, and deployment, (3) RESTful API building, (4) Vue basics, and (5) using Vue.js and Laravel together as a full-stack environment. If you accomplish this learning path, you will have sufficient knowledge to start your career as a full-stack Laravel developer.

**Pros**

*   instructors are industry experts (Justin Yost, Ray Villalobos, Michael Sullivan)
*   high-quality, professional videos audited by LinkedIn
*   well-structured, easy-to-navigate content
*   transcripts are available
*   you can earn a Linkedin badge of completion
*   one-month free trial
*   mobile apps available for [Android](https://play.google.com/store/apps/details?id=com.linkedin.android.learning&hl=en) and [iOS](https://apps.apple.com/us/app/linkedin-learning/id1084807225)

**Cons**

*   the courses cover Laravel 5 and 6, so might contain outdated info at some places

#### When to Choose LinkedIn Learning[](#when-to-choose-linkedin-learning)

If you want to work as a full-stack Laravel developer and don’t have a huge portfolio, LinkedIn Learning’s Laravel path might help you find a job, as you can display the completion badge on your LinkedIn profile (see [what it exactly means](https://www.linkedin.com/help/learning/answer/82977/learning-certificates-of-completion-faqs?lang=en)). It can also be a good choice if you want to do a longer course on full-stack Laravel development, where all the necessary content is already collected for you.

### 6\. Udemy (Beginners, Intermediate, Advanced)[](#6-udemy-beginners-intermediate-advanced)

Udemy is a global e-learning marketplace where independent creators are selling their video courses, not just in web development but also in many other subjects.

The [Laravel topic](https://www.udemy.com/topic/laravel) currently includes 280 courses at all knowledge levels. Udemy’s interface provides you with several different filters, such as price, ratings, duration, level, and more, to help you find the best Laravel tutorial for you. Besides English, it offers courses in other languages too.

**Pros**

*   easy-to-navigate user interface
*   abundant information on courses
*   a very wide selection of Laravel courses
*   subtitles in different languages (depending on the course)
*   certificate of completion
*   30-day money-back guarantee
*   mobile apps available for [Android](https://play.google.com/store/apps/details?id=com.udemy.android&hl=en) and [iOS](https://apps.apple.com/us/app/udemy-online-video-courses/id562413829)

**Cons**

*   quality of video and audio varies, as the courses are uploaded by indie authors

#### When to Choose Udemy[](#when-to-choose-udemy)

As Udemy offers almost 300 Laravel tutorial video series, you need to put some time and effort to find what you need. It’s worth paying attention to the ‘best seller’, ‘new’, and ‘hot &  new’ labels, even though you can’t filter for these characteristics.

Don’t forget to read the student reviews and watch the previews, as Udemy is not a centralized platform with a standardized quality assurance process. If you run into a bad apple, you can still get your money back using the 30-day money-back guarantee.

### 7\. Skillshare (Beginners, Intermediate)[](#7-skillshare-beginners-intermediate)

Skillshare is another e-learning marketplace similar to Udemy, however, it uses a different pricing model. Here, you don’t pay for individual courses, but you are charged with a monthly fee for which you can access all Skillshare courses.

Currently, Skillshare lists 22 [Laravel video courses](https://www.skillshare.com/search?query=Laravel) created by independent teachers — however, note that some PHP courses are also listed as a ‘Laravel course’ for some reason.

Most of Skillshare’s Laravel courses focus on practical skills, such as building a personal budget website, a todo app, a mailing list filter, a task scheduler admin panel, and a few others.

**Pros:**

*   well-structured courses
*   easy-to-navigate interface
*   built-in note-taking functionality
*   videos are captioned (English)
*   mobile apps available for [iOS](https://apps.apple.com/app/apple-store/id916819843) and [Android](https://play.google.com/store/apps/details?id=com.skillshare.Skillshare&referrer=utm_source%3Dskillshare%26utm_medium%3Dsite-footer)
*   7-day free trial (credit card details are required)

**Cons:**

*   you have to sign up to see pricing plans
*   video quality varies across courses
*   no publish date on courses (even though you can filter for courses ‘created this year’)

#### When to Choose Skillshare[](#when-to-choose-skillshare)

Although Laravel development is not the main focus of Skillshare, you can find some good, premium-level courses here. If you already have a Skillshare membership, it’s also worth having a look at the Laravel tutorial videos.

Alternatively, if you are new to Skillshare but are interested in other topics they’re teaching (there are plenty besides web development, from photography to music to creative writing), it can also be a good idea to sign up for a membership.

### 8\. Eduonix (Beginners, Intermediate)[](#8-eduonix-beginners-intermediate)

Eduonix is an online learning marketplace with independent instructors, similar to Udemy and Skillshare. It uses the same pricing model as Udemy, so you pay for each course individually (however, it has an option for [lifetime membership](https://www.eduonix.com/lifetime-learning-access) to all Eduonix courses and some [bundle discounts](https://www.eduonix.com/offer-zone) as well).

Currently, it offers [16 Laravel video courses](https://www.eduonix.com/search?proname=laravel), most of which guide you through a hands-on project, such as creating a hotel app with translation into four languages, a single page forum application, a contact manager app with a Vue frontend (this one is in the ‘Learn Laravel Building 10 Projects’ course), and others.

**Pros:**

*   detailed information on course content (including when it was last updated)
*   real-world projects
*   advanced filtering system
*   certificate of completion
*   30-day money-back guarantee

**Cons:**

*   quality of video and audio varies across courses
*   cheap coupon site look & feel

#### When to Choose Eduonix[](#when-to-choose-eduonix)

Eduonix can be a good choice for you if you are more interested in hands-on app building than theory. Even though it doesn’t offer multitudes of courses on Laravel development, it’s worth keeping an eye on it, especially because some creators sell their courses on both Udemy and Eduonix, but with a different price tag (usually Eduonix being the cheaper one).

Summary[](#summary)
-------------------

Setting up a learning goal to know where you are heading can help you a lot in finding the best Laravel tutorial for yourself. If you have prior experience with self-directed online learning, you already know what type of materials you prefer: text-based tutorials, videos, screencasts, podcasts, blogs, or longer books.

You don’t necessarily have to start with just one Laravel tutorial, but you can also opt for a mixed approach. For example, you can begin with a video course while signing up for a newsletter, listening to a podcast, and reading a blog at the same time.

If you are not sure about what skills you’ll need, it can be a good idea to browse job sites such as LaraJobs to see what’s in demand in the market (this can change with time).

You can also use a project planning app such as Trello or one of its alternatives to track your progress, set up deadlines and reminders, and keep motivating yourself by following through your learning plan.

If you choose a paid Laravel tutorial, it’s usually better to start with the monthly subscription than paying for one year in advance, until you know what you can expect (even if the monthly fee is lower with the annual subscription).

Finally, start to build a working Laravel app as early as possible in the learning process. Seeing that you have been able to accomplish a real-world project can help you keep up with learning and reach your goals.
