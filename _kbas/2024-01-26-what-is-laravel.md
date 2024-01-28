---
layout: post
title:  
date:   2024-01-26 01:00:00 -0800
description:
author: horacio 
image:  '/images/laravel.jpg'
tags:   [technology, laravel]
tags_color: '#477690'
---

The development of web applications and websites has become increasingly simple in recent years. Even the most technologically challenged among us have become fairly adept with products such as WordPress and Wix.

For the more advanced developer, a host of tools exists to help simplify the development process. One of the most useful of those tools is Laravel.

This article answers the question “What is Laravel?” by breaking it into an overview of the basics of PHP frameworks that are used in web development. We’ll follow that with an overview of the features of Laravel, a list of the important structures and components of Laravel, and a description of some of the more useful Laravel packages.

### Table of Contents

1.  [What Is Laravel?](#what-is-laravel)
2.  [Why Should You Use Laravel?](#why-should-you-use-laravel)
3.  [What Does Laravel Do?](#what-does-laravel-do)
4.  [How Does Laravel Work?](#how-does-laravel-work)
5.  [How Do You Get Started With Laravel?](#how-do-you-get-started-with-laravel)
6.  [What Else Can Laravel Do?](#what-else-can-laravel-do)
7.  [Laravel Now](#laravel-now)

What Is Laravel?[](#what-is-laravel)
------------------------------------

The simple answer to the question, “What is Laravel?” is straightforward: Laravel is a cross-platform PHP framework for building web applications.

But truly understanding the benefits of Laravel and its uses requires a deeper dive. Laravel allows a developer to take advantage of a large library of pre-programmed functionality (such as [authentication](/blog/laravel-authentication/), routing, and HTML templating). Access to this library makes it simpler to build robust web applications quickly while minimizing the amount of coding necessary.

Laravel offers a highly functional development environment, as well as intuitive and expressive command-line interfaces. In addition, Laravel [uses](https://blog.yellowant.com/orm-rethinking-data-as-objects-8ddaa43b1410) [object-relational mapping](https://blog.yellowant.com/orm-rethinking-data-as-objects-8ddaa43b1410) (ORM) for simpler data access and manipulation.

Laravel applications are highly scalable and have easy-to-maintain codebases. Developers can also seamlessly add functionality to their applications, thanks to Laravel’s modular packaging system and robust dependency management.

### Is Laravel Frontend or Backend?[](#is-laravel-frontend-or-backend)

Laravel is primarily a backend development framework, though it does offer some frontend functionality. Many of Laravel’s features, however, are frontend agnostic.

### Is Laravel a Programming Language?[](#is-laravel-a-programming-language)

Laravel is a PHP framework and uses a scripting language rather than being a strict PHP programming language. While scripting languages and programming languages are related, they have several noticeable differences, primarily in ease of use and speed of execution.

Scripting languages are platform-specific, interpreted languages. In contrast, programming languages are platform-agnostic, compiled languages. Being platform-specific, scripting languages rely on the compiler of the application in which they are working.

Applications built using scripting languages are compiled at runtime, meaning that each instruction is interpreted individually at runtime, rendering the application slower than a pre-compiled application. Runtime compilation also results in the application stopping or shutting down if it encounters a runtime error; in contrast, pre-compiled applications perform error checking during compilation, making them more robust at runtime. For many users, though, the disadvantages of scripting languages are more than offset by their ease of use and iteration.

### What Is a PHP Framework?[](#what-is-a-php-framework)

PHP (a recursive acronym for PHP Hypertext Preprocessor) is an open source, server-side scripting language widely used for web development. As of early 2021, nearly 80% of all websites are using PHP. While many may not be familiar with PHP, everyone is familiar with one of the most well-known PHP applications –  WordPress.

A PHP framework provides a set of code libraries containing pre-programmed modules that allow a user to build applications faster. They offer web developers a number of benefits, including more rapid development, a reduced need to write code, and enhanced security. They also help novice developers build up good coding practices, since they require specific organization of code. What’s more, PHP frameworks typically require less maintenance than applications built from the ground up.

Many modern PHP frameworks are object-oriented. Because of this, it’s beneficial to have a basic understanding of concepts like classes, objects, and inheritance before diving into a framework.

PHP frameworks use a Model-View-Controller (MVC) architecture. For those unfamiliar with MVC architecture, the Model is the data for the application, along with all associated logic. A table of subscribers, for example, can be a Model. The View provides a point of interaction with a user, where data from the Model can be viewed and modified. The Controller is a conduit between the View and the Model. In other words, the Controller takes user requests, retrieves the requisite information from the Model, processes it, and returns it to the view.

PHP applications, such as WordPress, have some known vulnerabilities. The [most notable examples](https://www.freecodecamp.org/news/php-security-vulnerabilities/) are code injection and SQL injection. Laravel includes features that help prevent SQL injection and other attacks.

However, developers should undertake additional efforts, such as penetration testing, to ensure the security of their applications. According to IT expert Barbara Ericson of [Cloud Defense](https://www.clouddefense.ai/blog/penetration-testing), web application security consists of both penetration testing and web application firewalls, which go hand-in-hand.

Penetration tests are intended to be more complex tests performed by qualified cybersecurity professionals, who will attempt to break into your system without any prior knowledge of its development in order to identify unpatched security vulnerabilities.

Why Should You Use Laravel?[](#why-should-you-use-laravel)
----------------------------------------------------------

Having answered “What is Laravel?,” the next question is, “Why Laravel?” Laravel provides a large set of robust tools that helps make the web app development process easier and faster, and the final application codebases are well-structured and easily maintained.

Some of the specific benefits of Laravel are:

### Laravel is Easy to Learn[](#laravel-is-easy-to-learn)

Laravel is relatively easy to learn, given the proper background. Laravel does require a general understanding of PHP and object-oriented programming (OOP) concepts for effective use. Knowing at least some HTML is helpful as well. And for any MVC architecture, it is also helpful to comprehend relational database management systems, such as MySQL or PostgreSQL.

### Laravel Simplifies the Development Process[](#laravel-simplifies-the-development-process)

From the beginning, Laravel was designed to simplify tasks that are common across a variety of web development projects like routing, authentication, migration, caching, and more. Laravel makes it simple to integrate pre-made modules into an application, using intuitive and expressive command line interfaces and Composer.

Laravel also has an [extensive collection of online documentation](https://laravel.com/docs/8.x), which is a good starting point for more experienced developers. A wide variety of online learning resources directed to all skill levels are also available.

### Laravel Has Tools for Developers of All Levels[](#laravel-has-tools-for-developers-of-all-levels)

Laravel describes itself as a progressive framework, meaning that it includes a variety of functionality that users of all levels will find useful. For example, beginners have access to starter kits for modules such as basic authentication features. Many of these tools are discussed in greater detail below.

Laravel project structure. (Source: [ITSolutionStuff.com](https://www.itsolutionstuff.com/upload/laravel-5-7-modular-system.png))

More experienced users can take advantage of the engines underlying the starter kits to build their own authentication processes and integrate them with their preferred frontends.

### Laravel Scales Easily[](#laravel-scales-easily)

Laravel is highly scalable. With integrated support for fast, distributed cache systems, Laravel applications are capable of addressing millions of requests per month. Laravel also offers a serverless deployment platform, Vapor, which is based on AWS and provides a high degree of scalability.

### Laravel Has a Massive Ecosystem and Community[](#laravel-has-a-massive-ecosystem-and-community)

Laravel has a tremendous ecosystem supported by a large community of developers. Because Laravel is one of the most used PHP frameworks, the library of available Laravel applications and packages is substantial. Both official Laravel packages and third-party packages are readily available.

Laravel’s official packages (many of which are discussed below) include authentication, server management, subscription billing, browser testing and automation, and more. Third-party packages are available on a number of sites, including [Packalyst](https://packalyst.com/) and [Laravel News](https://laravel-news.com/category/packages).

There is also a huge amount of information available from the Laravel developer community. Developers with questions are sure to find an answer by visiting one of the many Laravel forums, like [Laravel.io](https://laravel.io/), [The Laravel subreddit](https://www.reddit.com/r/laravel/), and [Laracasts](https://laracasts.com/).

### Laravel Is Widely Used[](#laravel-is-widely-used)

Many companies use Laravel to help build highly functional websites:

[Vacations by Rail](https://www.vacationsbyrail.com/) is a train-travel planning site built using the Laravel PHP framework. It is also integrated with the booking engine of Softrip.

The [Setapp](https://setapp.com/) website of curated apps for Mac and iOS is also built using the Laravel PHP framework.

[Restaurants.com](https://www.restaurants.com/)’s restaurant search application is very intuitive to use, thanks to the fact that it’s built using Laravel mobile app templates.

What Does Laravel Do?[](#what-does-laravel-do)
----------------------------------------------

Laravel’s feature set is far too extensive to cover fully in this brief overview. A few of the more significant features include:

### Route Handling[](#route-handling)

Laravel provides straightforward and intuitive route handling, using simple names to identify routes rather than long path names. The use of route identifiers also makes it easier to maintain applications, as the route name can be changed in one place rather than having to change it throughout. All web interface routes in a Laravel application are registered in the routes/web.php file.

### Security[](#security)

Laravel includes a [number of security features](https://iwconnect.com/laravel-security-features/) including user authentication, user role authorizations, email verification, encryption services, password hashing, and password reset features.

### Migration[](#migration)

Laravel provides version control for application databases using migrations. Migrations track how a database has been modified over time, making it easier to destroy or recreate the database when necessary.

### Templating[](#templating)

Blade is Laravel’s PHP templating engine. PHP templating engines [help divide business logic](/kba/what-is-php/) from HTML templating, resulting in a code base that is more easily maintained. Many of the features of Laravel rely on Blade templates. Blade offers more functionality than other templating engines because Blade allows use of plain PHP code, which others do not.

### Sessions[](#sessions)

Laravel uses sessions to store information about the user across several requests. Cookies are an example of a built-in Laravel session driver.

### Data Validation[](#data-validation)

Laravel makes it simple to [validate incoming user data](https://en.wikipedia.org/wiki/Data_validation). Laravel includes a number of data validation rules, with customizable error messages.

### Cache Handling[](#cache-handling)

Laravel supports data caching to minimize application task processing times. Laravel’s cache API supports a variety of third-party cache backends such as Memcached and Redis.

### Error Handling[](#error-handling)

Error handling is automatically configured upon starting a new Laravel project. Laravel applications can be [run in debug mode](https://pineco.de/debugging-in-laravel/), generating detailed error messages for all errors that occur.

### Testing[](#testing)

Laravel offers substantial testing figures out of the box. Laravel supports unit testing, which tests small, isolated sections of application code, as well as feature testing, which tests larger sections of code and higher-level functionality.

### Storage and File Management[](#storage-and-file-management)

Laravel uses the [Flysystem PHP package](https://flysystem.thephpleague.com/v2/docs/) to provide drivers for working with a variety of filesystems, from local filesystems to cloud-based storage such as Amazon S3. Laravel also provides for file transfer with SSH File Transfer Protocol (SFTP).

### Email[](#email)

Laravel includes an email API based on the SwiftMailer library, which allows sending email through a service of choice. Laravel supports email attachments and email queuing.

### Notifications[](#notifications)

Laravel supports sending notifications over a number of channels, whether well-known channels such as SMS or Slack, or using channels developed by the Laravel community.

How Does Laravel Work?[](#how-does-laravel-work)
------------------------------------------------

In order to best understand what Laravel can do, it is important to understand how Laravel deals with requests, i.e., the request lifecycle. As discussed above, Laravel is based on MVC architecture, and responds to requests from users, which the controller uses to retrieve and process data from the model and present information back to the user in a view.

A request enters a Laravel application via the public/index.php file, which loads the rest of the framework and retrieves an instance of the Laravel application. After retrieval of the application instance, the request is routed to the console kernel or HTTP kernel.

Among other tasks, the kernel [defines a selection of bootstrappers](https://developpaper.com/interpretation-of-laravel-kernel-http-kernel/) that perform tasks that must be completed before request handling takes place, as well as defining any middleware that requests must pass through prior to handling. Among these pre-handling tasks is loading any service providers required for the application.

Once bootstrapping is complete and service providers have been registered, the request passes to the router, which then directs the request to a route or to a controller. In addition, the router runs any required route-specific middleware. After the request passes through all required middleware, execution of a route or controller method returns a response that passes back through the chain to the View.

How Do You Get Started With Laravel?[](#how-do-you-get-started-with-laravel)
----------------------------------------------------------------------------

To begin with Laravel, it is necessary to understand some of the most important structures and functionalities in Laravel.

### Service Containers[](#service-containers)

The service container is one of the core components of Laravel. Service containers manage class dependencies and dependency injection.

Service containers are where a developer binds everything necessary to run a Laravel application.

### Service Providers[](#service-providers)

Equally important are Laravel service providers, which are where classes and dependencies are injected into the service containers.

### Facades[](#facades)

A facade is [a static interface](https://www.tutorialspoint.com/laravel/laravel_facades.htm) for classes bound in the service container. Facades create ease of use by providing easily memorable syntax as a proxy for a long class name.

### Packages[](#packages)

Packages are how functionality is added to Laravel. There are both stand-alone packages and application-specific packages. Service providers tell Laravel where to load package resources.

Laravel, like many other local development tools, relies on Docker. Docker is a container-based tool that allows developers to more easily create and deploy their applications. Using Docker containers, a developer packages their application with its dependencies, and deploys it as a single package.

### Command-Line Interfaces[](#commandline-interfaces)

Laravel includes a set of command-line interfaces (CLIs). The Artisan Console includes commands that help developers quickly build skeleton code, simplify and automate repetitive tasks, and more easily complete an application build. Sail is a lighter-weight command-line interface introduced in Laravel 8. Sail lets the developer interact with Docker, Laravel’s default development environment.

### Eloquent[](#eloquent)

Eloquent is an object-relational mapper (ORM) that [allows easy interaction](https://www.fullstackpython.com/object-relational-mappers-orms.html) with databases. Using the MVC architecture, the models correspond to individual tables in a database. With Eloquent, developers can be assured of quick retrieval, simple insertions and updates, and intuitive definition of relationships.

### Composer[](#composer)

Composer is a third-party application-level PHP dependency management tool. Composer manages the libraries, modules, and plug-ins required by a Laravel application.

### Homestead[](#homestead)

Laravel Homestead is a development environment allowing development on a virtual machine by providing a pre-packaged [Vagrant](https://www.vagrantup.com/) box. Homestead includes everything needed for Laravel application development, including PHP, MySQL, Nginx, Composer, Redis, and much more, so the developer need not install these packages on their local machine. Homestead does require the installation of Vagrant and either [VirtualBox](https://www.virtualbox.org/) or [Parallels](https://www.parallels.com/).

### Authentication Starter Kits[](#authentication-starter-kits)

Laravel includes a number of packages to help get developers up and running quickly. Prior to diving in, you may wish to review some of the [many available resources for learning Laravel](/blog/laravel-tutorial/). Laravel includes a couple of starter kits to help the developer implement common functionality quickly.

Laravel Breeze is an authentication starter kit. It includes common authentication and user account features such as user registration, login, email verification, and password confirmation and reset. Breeze also includes a javascript frontend through [Vue](https://vuejs.org/). Breeze has a default view layer that uses Blade templates and Tailwind CSS.

For more advanced authentication features, Laravel now offers Jetstream, first introduced in Version 8. In addition to the features found in Breeze, Jetstream also offers additional advanced features such as two-factor authentication, session management, API support via Laravel Sanctum, and optional team management.

For developers that prefer to use their own authentication frontend, Laravel offers Fortify—an authentication backend that is frontend agnostic. Fortify is the [engine for the Jetstream authentication starter kit](https://programmingfields.com/create-auth-using-jetstream-and-intertia-js-in-laravel-8/) and includes all of the Laravel authentication features (e.g. user registration, login, email verification, two-factor authentication, etc.). Fortify is not the underlying engine for Laravel Breeze.

Laravel also offers social media-based authentication (OAuth) through Laravel Socialite.

For developers who want to deploy their applications with minimal server configuration or, indeed, want serverless deployment, Laravel offers Forge and Vapor. Forge allows for deployment through a variety of infrastructure providers with minimal configuration efforts. Vapor is a serverless deployment platform based on AWS.

For those looking to take the next step, developers can deploy their Laravel applications through their own self-hosted website. This is because self-hosting your website will require you to [set up several defined databases](https://hostingcanada.org/how-to-host-your-own-website-from-home/) with a single PHP command (using the latest version) and SSH access to the server. Laravel offers both in one open-sourced PHP framework, and as an added bonus, it’s quite easy to install.

What Else Can Laravel Do?[](#what-else-can-laravel-do)
------------------------------------------------------

The better question might be, “What _can’t_ Laravel do?” Thousands of packages exist that accomplish any number of functions. Some of the more interesting official Laravel packages are:

### Cashier and Spark[](#cashier-and-spark)

Laravel Cashier provides an interface for subscription billing services from Stripe and Paddle. Cashier also provides advanced subscription functionality, such as coupons and cancellation grace periods.

Cashier is the engine for Laravel Spark, [a billing management panel](https://spark.laravel.com/) that allows users to create and manage their subscriptions. Spark is also limited to Stripe and Paddle as payment providers; custom providers are not yet compatible with Spark. Spark does, however, allow the developer to choose their frontend.

### Valet[](#valet)

Laravel Valet is a macOS development environment focused on speed and minimal resource usage (around 7 MB of RAM). Valet is not intended to be a complete replacement for Sail or Homestead. Instead, it’s meant for users with specific needs and resource limitations.

For more packages, see the Laravel website or [Packalyst](https://packalyst.com/).

Laravel Now[](#laravel-now)
---------------------------

The [current version of Laravel is version 10](/blog/laravel-10/), initially released in February 2023. This version includes a number of new features and improvements. Some of the new features in version 8 include Laravel Jetstream, job batching (allows execution of a batch of jobs, followed by performance of defined actions), Dynamic Blade components (allows runtime component rendering based on a runtime value), and use of [Tailwind CSS](https://tailwindcss.com/) by default in the Laravel paginator, among others. Improvements were also made to rate limiting and maintenance mode.

In the past, new Laravel releases happened every six months. However, this resulted in a lot of questions, comments, and confusion about Laravel’s new release process. With the release of Laravel 9 in February 2022, the framework has now moved to a 12-month major release cycle.

Summary[](#summary)
-------------------

Developers seeking fast and simple web application development should [consider learning Laravel](/blog/laravel-tutorial/). Laravel provides an extensive and robust set of resources that simplifies the development process by eliminating the need to code many common tasks from scratch.

Laravel also provides a secure virtual development environment and intuitive command-line interfaces. And because Laravel is simple to learn and has a strong support community and ecosystem, it’s a natural choice for many developers, be they beginners or experts with years of experience.
