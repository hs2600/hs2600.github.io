---
layout: post
title:  What Is PHP?
date:   2024-01-26 00:00:00 -0800
description:
author: horacio 
image:  '/images/php.jpg'
tags:   [technology]
tags_color: '#477690'
---

[PHP](https://www.php.net/) is an open-source, server-side scripting and [programming language](/blog/scripting-languages/) that’s primarily used for web development. The bulk of the core WordPress software is written in PHP, which makes PHP a very important language for the WordPress community. Some like to state that PHP as a programming language is dead but that’s not true.

There are different versions of PHP that you can [install on your server](/tutorial/install-php/), with the newer PHP 8.0, 8.1, and 8.2 offering significant performance improvements over the previous versions. 

In this post, we’ll explain more about what “server-side” means and how PHP functions. Then, we’ll move into some of the ways that PHP specifically applies to WordPress and WordPress sites.

### Table of Contents

1.  [How Does PHP Work?](#how-does-php-work)
2.  [What Is a PHP Framework?](#what-is-a-php-framework)

How Does PHP Work?[](#how-does-php-work)
----------------------------------------

In the brief definition above, you learned that PHP is a server-side language. But what does “server-side” actually mean? Server-side means that all of the processing happens on your web server before anything gets delivered to your visitor’s browser.

Here’s an example. Say someone visits your WordPress site. Before sending any files to that visitor, your server will first run the PHP code contained in the WordPress core and any themes/plugins you have installed on your site.

Then, once your server has processed the code, it delivers the output of all that PHP (which is the HTML code that a visitor’s browser actually receives).

The end result is that, unlike HTML, your website’s visitors will never see the PHP code that powers your WordPress site. They’ll just see the already-processed code that your server delivers to their browser.

### PHP 5 vs PHP 7 and PHP 8[](#php-5-vs-php-7-and-php-8)

According to W3Techs, [PHP is used by 77.4%](https://w3techs.com/technologies/details/pl-php/all/all) of all websites that use a server-side programming language, with [ASP.NET coming in second place](https://w3techs.com/technologies/history_overview/programming_language) with a little over 7% market share.

Like other programming languages, there are different versions of PHP that you can use. PHP 5, 7.0, 7.1, 7.2, 7.3, and 7.4 are older versions of PHP that have reached their end of life. This means they will no longer receive active support and have ceased (or will soon cease) receiving security support.

PHP 8.0, 8.1, and 8.2 offer significant performance and security improvements.

What Is a PHP Framework?[](#what-is-a-php-framework)
----------------------------------------------------

A PHP framework is a platform that enables developers to create PHP-based applications more efficiently. It consists of code libraries that help you perform common functions like form validation and data sanitization.

This is a much faster alternative than writing your own original code. However, speed and convenience aren’t the only reasons to consider using a PHP framework.

PHP frameworks also offer an easy way to access quality coding practices. Here, in Symfony, you can see that functions are organized neatly into different directories:

PHP framework directory

Additionally, PHP frameworks encourage refracturing of code and DRY development (Don’t Repeat Yourself). As a result, you’ll have a leaner codebase that’s easy to maintain. Plus, you don’t need to worry about maintaining the core framework yourself.

What’s more, PHP frameworks offer a simple way to make your PHP-based applications more secure. Although you’ll still need to write secure code, a framework can reduce the chance of hacker exploits. Some frameworks also provide built-in data sanitization protection against [common PHP security threats](https://docs.php.earth/security/intro/) like SQL injections and cross-site scripting.

### 3 Best PHP Frameworks[](#3-best-php-frameworks)

Now that you know a bit more about why to use PHP frameworks, here are some of the best options to consider.

#### 1\. Laravel[](#1-laravel)

[Laravel](https://laravel.com) offers clean architecture and everything you need to build a web application. It enables tons of features, such as user authentication, file storage, database migration, and much more.

It’s also super easy to get started with Laravel. You don’t even need to install PHP, a web server, or any other software on your system. Instead, it comes as a pre-packaged development environment that’s lightweight, fast, and secure.

#### 2\. Symfony[](#2-symfony)

[Symfony](https://symfony.com/) functions as a PHP framework and as a collection of PHP components to build websites. It’s one of the most flexible options, enabling you to choose the exact components that you need for your project.

Additionally, Symfony supports tons of databases, including Drizzle, MySQL, and Oracle. Better yet, Symfony is commercially backed by Sensio Labs, so you’ll find lots of support available (unlike other PHP frameworks).

#### 3\. CodeIgniter[](#3-codeigniter)

[CodeIgniter](https://codeigniter.com/) has very minimal configuration, so you can get it set up quickly. Like Symfony, you can add the components that you want. Therefore, you can easily build a light application with no bloat.

What’s more, CodeIgniter is a scalable solution that helps protect you against security threats like cross-site scripting. Plus, you’ll find some performance-based features like caching to speed up your apps.

