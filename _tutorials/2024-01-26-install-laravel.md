---
layout: post
title:  How To Install Laravel on Windows, macOS, and Linux
date:   2024-01-26 00:00:00 -0800
description:
author: horacio 
image:  '/images/laravel.jpg'
tags:   [technology]
tags_color: '#477690'
---

Having a strong and efficient framework is important when working in web development. Laravel is an elegant and powerful [PHP](/kba/what-is-php) web application framework that simplifies the development process while offering a range of key features and functionality.

But if you’re new to the framework or don’t know how to use it yet, don’t worry! This guide will help you get up and running with Laravel in no time.

This article will guide you through the process of installing Laravel on Windows, macOS, and Linux operating systems.

But first, let’s talk about what Laravel is, why it’s useful, and who can make the most of it.  

### Table of Contents

1.  [What Is Laravel?](#what-is-laravel)
2.  [Who Uses Laravel?](#who-uses-laravel)
3.  [Advantages of Using Laravel](#advantages-of-using-laravel)
4.  [Laravel Prerequisites](#laravel-prerequisites)
5.  [How To Install Laravel](#how-to-install-laravel)
6.  [How To Install Laravel on Windows](#how-to-install-laravel-on-windows)
7.  [How To Install Laravel on macOS](#how-to-install-laravel-on-macos)
8.  [How To Install Laravel on Linux](#how-to-install-laravel-on-linux)

What Is Laravel?[](#what-is-laravel)
------------------------------------

[Laravel](https://laravel.com) is a powerful and elegant PHP web application framework that streamlines web application development through an MVC (Model-View-Controller) architecture. Created by [Taylor Otwell](https://www.w3schools.in/laravel/history), Laravel has gained immense popularity due to its simplicity and ease of use, making it a top choice for web developers worldwide.

### Key Features and Functionality[](#key-features-and-functionality)

Some of the key features and functionality offered by Laravel include:

#### Eloquent ORM For Database Interactions[](#eloquent-orm-for-database-interactions)

Laravel’s [Object-Relational Mapping](https://www.freecodecamp.org/news/what-is-an-orm-the-meaning-of-object-relational-mapping-database-tools) (ORM) allows for smooth and intuitive interactions with your database, making it easy to perform CRUD (Create, Read, Update, Delete) operations and manage relationships between tables.

#### Blade Templating Engine[](#blade-templating-engine)

Blade is Laravel’s simple yet powerful templating engine, allowing you to create dynamic and reusable HTML templates with ease. With its concise syntax, Blade makes it easy to separate your application’s logic from its presentation.

#### Artisan Command-Line Tool[](#artisan-commandline-tool)

Laravel’s Artisan command-line tool offers a range of helpful commands for common tasks, such as generating controllers, migrations, and more. This speeds up the development process and helps you maintain a clean, organized codebase.

#### Built-in Support For Tasks Scheduling and Authentication[](#builtin-support-for-tasks-scheduling-and-authentication)

Laravel offers built-in support for task scheduling, making it easy to automate tasks like sending emails or cleaning up old data. Additionally, Laravel’s [authentication system](/blog/laravel-authentication) simplifies the process of adding secure user authentication to your web applications.

All of this is great to know but exactly who can make the best use of Laravel? Let’s explore that next.

Who Uses Laravel?[](#who-uses-laravel)
--------------------------------------

Laravel is a popular choice among various types of users, each of whom finds different benefits in using this powerful [PHP framework](/kba/what-is-laravel). Some of the key user groups include:

*   **Startups**: For startups, Laravel offers a rapid development process, which helps bring their ideas to life quickly and efficiently. The framework’s built-in tools and libraries save precious time and resources during the initial stages of a project.
*   **Established companies**: Laravel’s scalability and maintainability make it an attractive choice for established companies looking to build or upgrade their web applications. The framework’s strong community support ensures businesses can rely on Laravel for long-term projects.
*   **PHP web developers**: Developers appreciate Laravel’s elegant syntax and ease of use, which streamline the web application development process. Laravel’s features allow for efficient and effective coding practices.
*   **Backend engineers**: For backend engineers, Laravel’s powerful features, including its support for task scheduling, authentication, and the Artisan command-line tool, make it an essential tool in their toolkit. Laravel enables backend engineers to create robust and secure web applications with ease.

Now, here are some examples of companies that use Laravel in their projects:

### Bankrate[](#bankrate)

[Bankrate](https://www.bankrate.com) is a leading financial services company that uses Laravel to build and maintain its online applications. The framework helps Bankrate manage complex data structures and speed up development cycles.

### The New York Times[](#the-new-york-times)

The [New York Times](https://www.nytimes.com) uses Laravel for its internal web applications, helping the company to build and maintain complex web applications quickly and effectively.

### St Jude Children’s Research Hospital[](#st-jude-childrens-research-hospital)

[St Jude Children’s Research Hospital](https://www.stjude.org) uses Laravel to power its online donation platform and other web applications. The framework helps the hospital efficiently manage large amounts of data and ensure secure user authentication.

### Geocodio[](#geocodio)

[Geocodio](https://www.geocod.io) is a geocoding service that converts addresses to latitude and longitude coordinates and vice versa. Laravel powers Geocodio’s web application, allowing it to provide its customers a reliable and efficient geocoding service.

### October CMS[](#october-cms)

[October CMS](https://octobercms.com) is a free, open-source content management system (CMS) built on top of Laravel. By leveraging the power and flexibility of the Laravel framework, October CMS provides a user-friendly and customizable solution for managing website content.

As you can see, Laravel is a powerful framework used by companies of all sizes, from startups to large enterprises. But you still might not be sure about the benefits this framework offers to developers. Let’s explore that now.

Advantages of Using Laravel[](#advantages-of-using-laravel)
-----------------------------------------------------------

Laravel offers a number of advantages that make it a popular choice among web developers:

### Rapid Development Process[](#rapid-development-process)

Laravel provides intuitive syntax, built-in tools, and extensive documentation, enabling developers to create web applications quickly and efficiently, significantly reducing development time.

### Readable and Maintainable Code[](#readable-and-maintainable-code)

Laravel promotes clean and well-structured code, making it easier to read and maintain. This is particularly beneficial when working in a team or on large projects, as it helps ensure consistency and code quality.

### Strong Community and Support[](#strong-community-and-support)

Laravel has a large and active community of developers who contribute to its growth and provide support through forums, blogs, and social media. This makes it easy to find help and resources when needed.

### Built-In Tools and Libraries[](#builtin-tools-and-libraries)

Laravel comes with many built-in tools and libraries, such as [Eloquent ORM](https://laravel.com/docs/10.x/eloquent), Blade templating engine, and Artisan command-line tool, which simplify the development process and reduce the need for external dependencies.

So you know you want to use Laravel, but what do you need to know before getting started with it? That’s what we’ll discuss next.

Laravel Prerequisites[](#laravel-prerequisites)
-----------------------------------------------

Before diving into Laravel, there are a few things you should be familiar with:

*   Basic knowledge of PHP programming
*   Understanding of the MVC (Model-View-Controller) architectural pattern
*   Familiarity with command line/terminal
*   Experience with HTML, CSS, and JavaScript (optional but helpful)

### System Requirements[](#system-requirements)

Ensure your system meets the following requirements:

*   **Supported operating systems**: Windows, macOS, Linux
*   **Hardware requirements**: Minimal (dependent on PHP and Composer)
*   **PHP installation**: Required before installing Laravel
*   **Composer installation**: Required for Laravel installation

### Versions[](#versions)

When choosing a version of Laravel, consider the following:

*   **Stable vs. latest versions**: Choose based on project needs. [Stable versions](/blog/laravel-10) offer reliability, while the latest versions may include new features and improvements.
*   **Importance of checking compatibility**: Ensure smooth integration with other libraries and PHP versions by verifying that your chosen version of Laravel is compatible with your project’s dependencies.

How To Install Laravel[](#how-to-install-laravel)
-------------------------------------------------

Once you’ve familiarized yourself with Laravel and the system requirements, you can begin installing it. The installation process is straightforward and consists of straightforward steps but they do vary from operating system to operating system.

Follow along with the instructions for your specific operating system below.

How To Install Laravel on Windows[](#how-to-install-laravel-on-windows)
-----------------------------------------------------------------------

To install Laravel on Windows, follow these detailed steps:

1.  [Install XAMPP](#windows-1)
2.  [Install Composer](#windows-2)
3.  [Verify Composer Installation](#windows-3)
4.  [Install Laravel Using Composer](#windows-4)
5.  [Verify Laravel Installation](#windows-5)
6.  [Start The Server](#windows-6)
7.  [Run The Project In Your Browser](#windows-7)

### 1\. Install XAMPP[](#windows-1)

XAMPP is a free and open-source web server solution stack that includes PHP, MySQL, and Apache. To install XAMPP on Windows, follow these steps:

Visit the [XAMPP download page](https://www.apachefriends.org/download.html) and download the appropriate installer for your Windows version.

Run the installer and follow the on-screen instructions. During the installation process, you can choose which components to install. Make sure to select PHP and MySQL.

Once installed, launch the **XAMPP Control Panel** and start the Apache and MySQL services.

### 2\. Install Composer[](#windows-2)

Composer is a dependency management tool for PHP that is required to install Laravel. To install Composer on Windows, follow these steps:

Visit the [Composer download page](https://getcomposer.org/download) and download the **Composer-Setup.exe** file.

Run the **Composer-Setup.exe** file and follow the on-screen instructions.

You’ll also be prompted to select the install mode. Be sure to pick **Install for all users (recommended)**.

Make sure to select the correct PHP executable during the installation process (usually located in the XAMPP installation folder under xampp/php/php.exe).

Click **Next** to move through the on-screen instructions then click **Install**.

Once installation is completed, click **Finish**.

### 3\. Verify Composer Installation[](#windows-3)

To verify that Composer was installed correctly, open the Command Prompt and run the following command:

    composer --version

If the installation was successful, you should see the Composer version displayed.

### 4\. Install Laravel Using Composer[](#windows-4)

You can use Composer, which is now installed, to install Laravel globally on your system. To do so, open the Command Prompt and run the given command:

    composer create-project laravel/laravel app-name

This will automatically download all the relevant Laravel files to create a new project.

### 5\. Verify Laravel Installation[](#windows-5)

To verify that Laravel was installed correctly, open the Command Prompt and run the following command:

    laravel --version

After a successful installation, you will be able to see the Laravel version.

### 6\. Start The Server[](#windows-6)

With your new app project created, you will then need to start a server. To do this, type in the following:

    cd app-name

    php artisan serve

### 7\. Run The Project In Your Browser[](#windows-7)

With the server started you should then be able to access your app project via your web browser. To do this, open your browser and go to the following: https://localhost:8000

With this, you can start developing web applications using Laravel on your Windows machine.

How To Install Laravel on macOS[](#how-to-install-laravel-on-macos)
-------------------------------------------------------------------

To install Laravel on macOS, follow these detailed steps:

1.  [Install Homebrew](#mac-1)
2.  [Install Node.js and npm](#mac-2)
3.  [Install PHP](#mac-3)
4.  [Install Composer](#mac-4)
5.  [Verify PHP and Composer Installations](#mac-5)
6.  [Install Laravel Using Composer](#mac-6)
7.  [Verify Laravel Installation](#mac-7)
8.  [Create a New Project](#mac-8)
9.  [Run The Laravel Server](#mac-9)

### 1\. Install Homebrew[](#mac-1)

[Homebrew](https://brew.sh) is a package manager for macOS that simplifies the installation of software. To install Homebrew, open the Terminal and run the following command:

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Follow the on-screen instructions to complete the installation.

### 2\. Install Node.js and npm[](#mac-2)

Next, install Node.js and npm (Node.js package manager) using Homebrew. In the Terminal, type the following command:

    brew install node

This command installs both Node.js and npm on your system.

### 3\. Install PHP[](#mac-3)

With Homebrew installed, you can now use it to install PHP. Run the following command in the Terminal:

    brew install php

Wait for the installation to complete.

### 4\. Install Composer[](#mac-4)

Composer is a dependency management tool for PHP that is required to install Laravel. To install Composer on macOS, run the following commands in the Terminal:

    curl -sS https://getcomposer.org/installer | php sudo mv composer.phar /usr/local/bin/composer

### 5\. Verify PHP and Composer Installations[](#mac-5)

To verify that PHP and Composer were installed correctly, open the Terminal and run the following commands:

    php --version composer --version

If the installations were successful, you should see the PHP and Composer versions displayed.

### 6\. Install Laravel Using Composer[](#mac-6)

Now that you have Composer installed, you can use it to install Laravel. Open the Terminal and run the following command to install Laravel globally on your system:

    composer global require laravel/installer

Wait for the installation process to complete.

### 7\. Verify Laravel Installation[](#mac-7)

To verify that Laravel was installed correctly, open the Terminal and run the following command:

    laravel --version

You will know that the installation is successful if you see the version of Laravel displayed.

### 8\. Create a New Project[](#mac-8)

To create a new Laravel project, use the following command in the Terminal:

    composer create-project --prefer-dist laravel/laravel app-name

Replace app-name with the desired name for your project. This command will create a new directory with the specified name and install the Laravel framework inside it.

Next, navigate to the newly created project directory:

    cd app-name

Remember to replace app-name with the actual name you used for your project.

### 9\. Run The Laravel Server[](#mac-9)

To start the local development server, execute the following command within the project directory:

    php artisan serve

This command will launch a local development server on port 8000. You can access your Laravel application by opening your web browser and navigating to:

http://127.0.0.1:8000

You should now see the default Laravel welcome page, indicating that your application is running successfully. You can start building your Laravel application and see the changes live on the local development server.

How To Install Laravel on Linux[](#how-to-install-laravel-on-linux)
-------------------------------------------------------------------

To install Laravel on Linux, follow these detailed steps:

1.  [Install Apache Web Server](#linux-1)
2.  [Install PHP](#linux-2)
3.  [Install MariaDB](#linux-3)
4.  [Install Composer](#linux-4)
5.  [Verify PHP, MariaDB, and Composer Installations](#linux-5)
6.  [Install Laravel Using Composer](#linux-6)
7.  [Run the Laravel Server](#linux-7)

To install Laravel on Linux, follow these detailed steps:

### 1\. Install Apache Web Server[](#linux-1)

First, update your package index and install Apache by running the following commands in the Terminal:

    sudo apt update sudo apt install apache2

After installation, enable the Apache service and start it:

    sudo systemctl enable apache2 sudo systemctl start apache2

### 2\. Install PHP[](#linux-2)

To install PHP, use the following command in the Terminal:

    sudo apt install php libapache2-mod-php php-mbstring php-xmlrpc php-soap php-gd php-xml php-cli php-zip php-bcmath php-tokenizer php-json php-pear

### 3\. Install MariaDB[](#linux-3)

MariaDB is an open-source relational database management system. Install it by running the following command:

    sudo apt install mariadb-server

After installation, secure your MariaDB installation by running:

    sudo mysql_secure_installation

Follow the on-screen instructions to set up a root password and other security settings.

### 4\. Install Composer[](#linux-4)

Composer is a dependency management tool for PHP. Download and install Composer by executing the following commands in the Terminal:

    curl -sS https://getcomposer.org/installer | php
    sudo mv composer.phar
    sudo chmod +x /usr/local/bin/composer

### 5\. Verify PHP, MariaDB, and Composer Installations[](#linux-5)

Ensure that PHP, MariaDB, and Composer are installed correctly by checking their versions with the following commands:

    php -v mysql --version composer -V

### 6\. Install Laravel Using Composer[](#linux-6)

Now, install Laravel by running the following command in the Terminal:

    composer create-project --prefer-dist laravel/laravel app-name

Replace **app-name** above with whatever you wish.

Then go to the newly created project directory:

cd app-name

### 7\. Run the Laravel Server[](#linux-7)

To launch the development server for the project, go to the project directory and run the specified command.

    php artisan serve

To access your Laravel application, run this command to launch a local development server on port 8000. Then, open your web browser and navigate to:

http://127.0.0.1:8000

If everything has been set up correctly, you will be able to view the default Laravel welcome page which confirms that your application is up and running. Now Laravel is installed on your Linux system!

Summary[](#summary)
-------------------

In this article, we’ve covered the process of installing Laravel on Windows, macOS, and Linux. Now that you have successfully installed Laravel on your chosen operating system, you’re ready to start building powerful and elegant web applications using this popular PHP framework.

As you dive deeper into Laravel, be sure to explore the wealth of resources available to help you learn and get the most out of this powerful tool. The [Laravel community](https://laracasts.com) is known for its strong support and [comprehensive documentation](https://laravel.com/docs/10.x), so don’t hesitate to reach out if you need assistance.
