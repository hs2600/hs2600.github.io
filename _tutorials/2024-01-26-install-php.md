---
layout: post
title:  "Install PHP: A Beginner's Tutorial"
date:   2024-01-26 00:00:00 -0800
description: Quick Guide on Installing PHP on Any Server (Linux, macOS, Windows)
author: horacio 
image:  '/images/php.jpg'
tags:   [technology]
tags_color: '#477690'
---

Setting up a server can be a daunting task, especially when installing languages like PHP. If you want to get a WordPress test server up and running, it’s a necessary skill to learn.

Got no idea where to start to get PHP on your server? Depending on your unique setup, there are many ways to do it. Where do you download PHP, which version, what do you need to make it work, and how do you install PHP on various OSes?

We’ll answer them all in this one-stop PHP installation guide.

Let’s begin!

### Table of Contents

1.  [What is PHP?](#what-is-php)
2.  [PHP Prerequisites](#php-prerequisites)
3.  [How to Install PHP on Linux](#how-to-install-php-on-linux)
4.  [How to Install PHP on Windows](#how-to-install-php-on-windows)
5.  [How to Install PHP on macOS](#how-to-install-php-on-macos)
6.  [All About PHP Extensions](#all-about-php-extensions)

### Check out our video guide to installing PHP[](#check-out-our-video-guide-to-installing-php)

What is PHP?[](#what-is-php)
----------------------------

[PHP](/kba/what-is-php) is an open source [scripting language](/blog/scripting-languages) primarily used for web development and server-side (backend) scripting. In simple terms:

*   PHP can be installed on a server to run scripts (e.g. pieces of code to add forms to your site).
*   It is run server-side rather than client-side, so it works in the backend rather than in the browser.
*   It integrates well with HTML, making it highly suitable for web development.

It’s also one of the easiest web scripting languages to [learn](/blog/php-tutorials), making it a popular choice for beginners. But it’s also quite powerful and suitable for advanced website functions.

Many websites and tools use PHP and its many extensions (.NET, Apache, and MySQL may sound familiar). 

PHP is a great launching point for beginner devs. It’s straightforward to use compared to other web scripting languages, but that doesn’t come at any expense of functionality. You can do all sorts of things with it if you’re skilled enough.

PHP is also quite popular. So, you can find plenty of extensions and resources online.

That said, let’s get into the server setup instructions.

PHP Prerequisites[](#php-prerequisites)
---------------------------------------

Before installing PHP, you’ll need to make sure your server can handle it. Luckily, the requirements are fairly basic, and a lot of the software is likely already installed on your computer.

If you’ve never created a server before, you should check out this [guide to set up a local server](https://www.maketecheasier.com/setup-local-web-server-all-platforms) on multiple OSes. The exact specifics vary depending on your operating system, but you should know how to work with the command line and be ready to install new software.

Whatever operating system you’re installing PHP on, you’ll need a web server to run it. You’ll also likely need to install a database like MySQL, so keep that in mind.

Here are the PHP prerequisites for each OS, starting with [Linux](https://www.php.net/manual/en/install.unix.php):

*   An ANSI C compiler.
*   Module-specific components like GD graphics libraries or PDF libraries.
*   Optional: Autoconf 2.59+ (for PHP versions < 7.0), Autoconf 2.64+ (for PHP versions > 7.2), Automake 1.4+, Libtool 1.4+, re2c 0.13.4+, and Bison.

You should also be familiar with navigating Unix-like OSes already.

Now the PHP requirements for [Windows](https://www.php.net/manual/en/install.windows.requirements.php):

*   Multiple Windows OSes are supported on PHP 5.5+, but 7.2.0+ users cannot use Windows 2008 or Windows Vista.
*   Visual C Runtime (CRT).
*   Visual Studio 2012, 2015, 2017, or Microsoft Visual C++ Redistributable for Visual Studio 2019, depending on your PHP version.

Lastly, there are no prerequisites for [macOS](https://www.php.net/manual/en/install.macosx.php) because PHP comes bundled with the system. We’ll explain how to enable it below.

### Where to Download PHP[](#where-to-download-php)

If you need to download the PHP files manually, you should get them from the official site’s [PHP downloads page](https://www.php.net/downloads).

Avoid installing it from third-party sites unless you know they’re safe, as downloading files from third-party sites can lead to accidentally installing malware.

If you’re downloading for a Windows machine, look for the “Windows downloads” link in each version of PHP and make sure you’re installing the proper files.

You can also install [older versions of PHP](https://www.php.net/releases/index.php), but this is not recommended unless you know what you’re doing, as they expose your server to bugs and major security flaws.

If you’re running a Linux distribution, you usually don’t need to get the files through the website, and you should use the command line. We’ll go over that in detail below.

### Which PHP Version Should I Use?[](#which-php-version-should-i-use)

If you’ve clicked that download link above, you’re likely looking at all those files and feeling overwhelmed. Which PHP version is the right one?

Generally speaking, if you’re starting a brand new project where compatibility issues aren’t a problem, you should get the latest stable version of PHP.

It is sometimes possible to download beta versions of PHP, which are even newer, but these are often buggy and only released to help the developers gather feedback. Most of the time, you should stick with the stable releases.

What about older versions? Every PHP version comes with new features, but that means new incompatibilities with older features. If you need to do something specific that{s not supported on the latest PHP version, you can use an older version, but you should stick only with the currently supported versions.

If you’re not sure, then use the latest version of PHP.

Take note that WordPress is only compatible with [certain versions of PHP](https://make.wordpress.org/hosting/handbook/handbook/server-environment/#php). It technically supports PHP versions starting at 5.6.20+, but these are quite old and thus not recommended. Version 7.4 and 8.0  are currently the best-supported versions for WordPress.

PHP version 8 is also compatible, but currently, this is very new, and not all plugins work properly. If you’re worried about compatibility issues, stick with PHP version 7.4. You can read our PHP benchmarks post to see how various PHP CMSes and frameworks perform on different PHP versions.  

How to Install PHP on Linux[](#how-to-install-php-on-linux)
-----------------------------------------------------------

Before starting, you should be familiar with the Terminal and how to operate Unix-like OSes in general. Generally, these command line codes should work on any Linux distribution that uses the normal syntax in the Terminal, but we’ve left some notes below for specific OSes.

First, you should make sure your packages are up to date, so run this [Linux command](/blog/40-linux-commands) in the Terminal.

    sudo apt-get update && sudo apt-get upgrade

Now you’re ready to install PHP. The command to do so is effortless and straightforward.

    sudo apt-get install php

Installing PHP via terminal

This will install the latest version of PHP along with several extensions. You can use this code to see which version you have.

    php –v

What if you want to install a specific version of PHP, such as PHP 7.4? You’ll need to use a PPA, or Personal Package Archive, by [Ondřej Surý](https://launchpad.net/~ondrej/+archive/ubuntu/php). This is a safe way to install older supported versions of PHP. Run these three commands one at a time:

    sudo apt install software-properties-common
    sudo add-apt-repository ppa:ondrej/php
    sudo apt-get update

Now your system recognizes the archive, and you can install PHP 7.4. Type in the following command:

    sudo apt install php7.4

And of course, you can replace this number with whatever PHP version you want.

That covers the basics, but if you need extra help with configuration, the [PHP installation documentation](https://www.php.net/manual/en/install.unix.php) for Unix can help.

### Installing PHP on Ubuntu[](#installing-php-on-ubuntu)

For Ubuntu users, there aren’t many specific concerns as long as you follow the guide above. Ubuntu is one of the most popular distributions, so most Linux guides are practically made for that system.

One alternative option available to you is downloading a LAMP stack. LAMP stands for Linux, Apache, MySQL, and PHP. It’s essentially a bundle of all the software you need to get a server up and running.

While you can manually download each of these tools separately, you could get Taskel, a bundle that will install all these at once. Just run these two commands in succession in the Terminal:

    sudo apt install tasksel
    sudo tasksel install lamp-server

Installing LAMP stack with Taskel via terminal

### Installing PHP on CentOS 7[](#installing-php-on-centos-7)

This operating system is a little different from other Linux distributions. On CentOS, the apt and apt-get commands are not the ideal ways to install the software. Instead, it uses [yum](https://access.redhat.com/solutions/9934), Yellowdog Updater Modified, a better package manager for RHEL-based operating systems.

Otherwise, the commands you’ll need to use are pretty similar. To update your packages, run this command instead:

    sudo yum install epel-release && sudo yum update

As for other commands, you can usually replace `apt-get` with yum. To install PHP, use this command.

    sudo yum install php

PHP commands such as `php –v` should work the same on CentOS 7, so you don’t need to worry about that.

### Installing PHP on Debian[](#installing-php-on-debian)

Last for Unix-like operating systems is [Debian](https://www.php.net/manual/en/install.unix.debian.php). This time there are just a few minor concerns, but most of the commands listed above should work fine.

For Debian, you can use either `apt-get` or `aptitude` in your Terminal commands. The `aptitude` command is a little more comprehensive and provides a menu interface. It’s up to personal preference which you use, and either will get the job done.

So instead of using the usual `apt-get` command, you could run this one instead:

    sudo aptitude install php

Debian can be finicky. If you find PHP isn’t parsing or extensions aren’t working, make sure you’ve updated your server’s web configuration file and that it’s loading the extension **ini** files.

Besides a few small things, instructions for Debian are practically identical to those for other Linux distributions.

How to Install PHP on Windows[](#how-to-install-php-on-windows)
---------------------------------------------------------------

If you’re using a Windows system, unlike macOS and Linux, you don’t need to install PHP through the [command line](https://www.php.net/manual/en/install.windows.manual.php) (though it is an option if you’d prefer).

An easy way to install PHP from here is to [enable IIS](https://www.howtogeek.com/112455/how-to-install-iis-8-on-windows-8) and then use [WebPI](https://www.microsoft.com/web/downloads/platform.aspx) to install PHP. After launching WebPI, you can find it under the **Products** tab. Click **Add** on the version you want, then click **Install**.

Enabling IIS on Windows

You can also [download PHP for Windows](https://windows.php.net/download) and [manually configure](https://docs.microsoft.com/en-us/iis/application-frameworks/install-and-configure-php-on-iis/install-and-configure-php) it to work with IIS. Make sure to get a non-thread-safe version if you’re using IIS.

If all this is too complicated, you could instead install WampServer or XAMPP, as these come with everything you need to start working with a web server: Apache, a database, and of course PHP.

These instructions will work with most modern Windows OSes such as Windows 10, 7, and Vista. If you’re using an older version of Windows, you should check out the [legacy Windows installation](http://php.adamharvey.name/manual/en/install.windows.legacy.index.php) documentation.

Windows may need a little extra configuration to get PHP working properly, so make sure to check the [recommended Windows configuration](https://www.php.net/manual/en/install.windows.recommended.php) documentation. You just have to make a few small **ini** tweaks.

How to Install PHP on macOS[](#how-to-install-php-on-macos)
-----------------------------------------------------------

PHP comes preinstalled on most [macOS](https://www.php.net/manual/en/install.macosx.php) systems, so you usually don’t need any manual installation.

All you need to do is uncomment a few lines of code in the Apache configuration file **httpd.conf**, which you can usually find at `/private/etc/apache2/httpd.conf`. Uncomment these two lines by removing the hashtag symbol:

    # LoadModule php5_module libexec/httpd/libphp5.so
    # AddModule mod_php5.c

You may need to do [extra configuration](https://www.php.net/manual/en/install.macosx.bundled.php) if you don’t like some file settings’ default values. Otherwise, find the DocumentRoot, then create and load a PHP file with this code:

    <?php phpinfo(); ?>

You can always check the PHP version with the `php –v` command to make sure PHP was installed correctly.

If you do need to download PHP manually, then you should [install Homebrew](https://brew.sh) and use this simple command:

    brew install php

All About PHP Extensions[](#all-about-php-extensions)
-----------------------------------------------------

Once you’ve got PHP up and running, it’s a good idea to think about extensions. These compiled libraries add all sorts of extra, helpful functionality. Think of them as plugins that add on to what PHP already offers. Some of these are required to run PHP frameworks, such as Laravel and Symfony.

While it’s completely possible to code everything yourself without ever touching an extension, there’s no reason to do it all on your own when widely-used shortcuts exist to make your life easier.

PHP already comes with dozens of built-in extensions, some of which you must enable manually, and others you can start using right away. You can also install PHP extensions through sites like [PECL](https://pecl.php.net), which hosts hundreds of third-party packages.

The PHP manual offers [extension documentation](https://www.php.net/manual/en/extensions.php) for many of these as well, so you can get the hang of using them.

Not sure where to start? Here are just a handful of a few popular PHP extensions:

*   Apache: Apache is a widely used web server software recommended by WordPress due to its great compatibility with it and PHP. Apache comes bundled with PHP, so you don’t need to install it manually.
*   [.NET](https://dotnet.microsoft.com): .NET is a popular software framework that you can use to build web applications and more. It works with multiple languages, including PHP. You may also be interested in [PeachPie](https://www.peachpie.io), which allows you to run PHP code in .NET.
*   MySQLi: A better version of the old MySQL extension, MySQLi enables you to work with MySQL database software. This one is a must-have to help you set up your database.

Whenever you install an extension, you need to uncomment it. Just open up **php.ini** and remove the semicolon (**;**) in front of `extension=extensionname`.

You should also check out these PHP frameworks if you’d like to standardize your code and build with premade libraries. They’re a great way to get started with developing web applications with PHP.

Summary[](#summary)
-------------------

Whatever operating system you’re using, installing PHP isn’t such a hard process. Make sure you download PHP either through the command line or from its [official site](https://www.php.net/downloads). 
