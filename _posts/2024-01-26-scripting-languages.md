---
layout: post
title:  Scripting Languages
date:   2024-01-26 00:00:00 -0800
description: 13 of the most popular Scripting Languages
author: horacio 
image:  '/images/code.jpg'
tags:   [technology, coding]
tags_color: '#477690'
---

Scripting languages make coding simpler and faster, so it’s not surprising that they are widely used in web development.

However, that’s not their only field of application. There are also scripting languages for operating systems, statistical analysis software, office applications, game engines, and many other kinds of platforms.

In this post, learn what they mean exactly and get to know the best examples of scripting languages.

### Table of Contents

1.  [Scripting Languages vs Programming Languages](#scripting-languages-vs-programming-languages)
2.  [Confusions About Scripting Languages](#confusions-about-scripting-languages)
3.  [What Are the 13 Best Scripting Languages?](#what-are-the-13-best-scripting-languages)

What Are Scripting Languages?
-----------------------------

Scripting languages are a specific kind of computer languages that you can use to give instructions to other software, such as a web browser, server, or standalone application. Many of today’s most popular coding languages are scripting languages, such as JavaScript, PHP, Ruby, and Python.

Scripting languages can perform different actions within a particular runtime environment, such as automating task execution, enhancing the functionality of the parent software, performing configurations, extracting data from data sets, and others.

Scripting languages can come about in two ways:

1.  A runtime environment can introduce its own scripting language, such as Bash for the GNU operating system or VBA for Microsoft Office applications.
2.  A runtime environment can adopt an existing scripting language, for instance, [MongoDB](/kba/what-is-mongodb)’s `mongo` shell has been [built around JavaScript](https://www.mongodb.com/docs/v5.0/tutorial/write-scripts-for-the-mongo-shell).

On the other hand, sometimes it’s the scripting language that exists first and it gives birth to its own parent platform — however strange that may sound.

This is what happened in the case of **Node.js**, a backend runtime environment that was created to allow web developers to use JavaScript not just on the frontend but also on the backend, following the ‘JavaScript everywhere’ paradigm.

### What Does Scripting Mean in Programming?[](#what-does-scripting-mean-in-programming)

The action of scripting is essentially writing a [series of commands](/blog/40-linux-commands) that are interpreted one by one by an application or scripting engine. Even though the script guides the platform through what to do (gives it a script to read and interpret), the execution is performed by the runtime environment and not by the scripting language itself.

This is how scripting languages are different from programming languages such as Java that you can ‘write once, run anywhere’ (official Java slogan meaning Java programs can run as standalone applications in any environment; since being coined it has also become the [WORA principle](https://en.wikipedia.org/wiki/Write_once,_run_anywhere) that refers to cross-platform capabilities).

Scripting Languages vs Programming Languages[](#scripting-languages-vs-programming-languages)
---------------------------------------------------------------------------------------------

Although the terms ‘scripting language’ and ‘programming language’ are frequently used interchangeably, they are not the same thing.

### Platform-Specific vs Platform-Agnostic[](#platformspecific-vs-platformagnostic)

Scripting languages are platform-specific, while programming languages are platform-agnostic (cross-platform) as they have the ability to execute themselves. For instance, you can run a Java program on any operating system.

### (Mostly) Interpreted vs Compiled[](#mostly-interpreted-vs-compiled)

While programming languages are compiled, scripting languages are mostly interpreted — even though there are some scripting languages that are both compiled and interpreted, such as Python and Groovy.

‘Compiled’ means that a programming language has its own compiler that translates the syntax into machine code before runtime. In contrast, scripting languages are interpreted line by line during runtime by the interpreter of the platform they are running on.

### Faster vs Slower at Runtime[](#faster-vs-slower-at-runtime)

Because of this difference in implementation, programming languages run faster than scripting languages as they don’t have to be compiled in real-time. Compilers also perform collective error handling before execution, while interpreters evaluate code line by line, so they pause (or completely stop) every time they encounter an error.

This also adds to the total execution time of scripting languages, even though on modern and faster hardware, this is less of an issue than it was before.

### More vs Less Code-Intensive[](#more-vs-less-codeintensive)

Programming languages are more code-intensive as you have to do many things manually that are handled by the platform in the case of scripting languages. If you use a scripting language you have to write much less code.

### Standalone Apps vs Apps as Part of a Stack[](#standalone-apps-vs-apps-as-part-of-a-stack)

There are some things that you simply can’t do with a scripting language. Most importantly, you can’t create standalone desktop and mobile applications with a scripting language, as there’s no runtime environment that interprets them.

For instance, you can use PHP frameworks such as WordPress and [Laravel](/tutorial/laravel-tutorial) only for websites and web applications because they use the web browser as their runtime environment. Similarly, WordPress mobile apps run within mobile runtime environments, such as [Capacitor](https://capacitorjs.com), that incorporate web views.

### Scripting vs Programming Languages — Differences Overview[](#scripting-vs-programming-languages--differences-overview)

So the main differences between scripting vs programming languages are as follows:

|**Scripting languages**| **Programming languages**|
|Platform-specific|Platform-agnostic (cross-platform)|
|(Mostly) interpreted|Compiled|
|Slower at runtime|Faster at runtime|
|Less code-intensive|More code-intensive|
|Creates apps as part of a stack|Creates standalone apps|

Confusions About Scripting Languages[](#confusions-about-scripting-languages)
-----------------------------------------------------------------------------

There are some confusions about scripting languages that you’ll frequently run into, so let’s have a look at them before getting into the best scripting languages.

Most importantly, it doesn’t make much sense to speak about frontend vs backend scripting languages, even though many articles you’ll find all over the web use this kind of grouping.

There’s actually just one frontend scripting language currently in use, and that’s JavaScript (there existed other ones before, such as ActionScript and JScript, but now all are deprecated).

It’s not frontend vs backend that’s important in the context of scripting languages but the runtime environment(s) where a scripting language can run.

Note that ‘frontend’ just means something (image, font, markup, stylesheet, script, another type of static file) that a web browser can interpret. For instance, try to open a PHP file directly from the web browser: you can’t, because a PHP application server has to interpret it — so [PHP](/blog/php-tutorials) is a backend scripting language in the context of web development, while the application layer of a server stack (e.g. LAMP) in the context of scripting languages.

Besides web development (frontend and backend scripting), scripting languages can also be used for multiple things such as programming and configuring operating systems and specific applications/environments, manipulating data sets, automating tasks, and many others.

A scripting language can run in multiple environments, too.

### What Are Not Scripting Languages?[](#what-are-not-scripting-languages)

Before getting into the best scripting languages, let’s see the **coding languages that are sometimes falsely called scripting languages**, but you can’t script with them:

*   Markup languages, such as HTML and XML. In HTML, there are [attributes for event handling](https://developer.mozilla.org/en-US/docs/Web/Events/Event_handlers) such as onclick and onmouseover, but these are still JavaScript callbacks.
*   Stylesheet languages, such as CSS, Sass, and LESS.
*   Any kind of library or framework built on top of any scripting language, such as jQuery, PostCSS, React, Vue, Angular, Rails, Grails, Django, Laravel, WordPress, and others.
*   Languages that are compiled into a scripting language, such as TypeScript and CoffeeScript.
*   SQL as it’s for managing data in relational database management systems (RDBMS) such as MySQL and MariaDB. They don’t let you write dynamic functionality. However, many RDBMSs have shells that let you use a scripting language (e.g. JavaScript or Python in the [MySQL Shell](https://dev.mysql.com/doc/mysql-shell/8.0/en)).
*   Runtime environments for one or more scripting languages, such as NodeJS.

What Are the 13 Best Scripting Languages?[](#what-are-the-13-best-scripting-languages)
--------------------------------------------------------------------------------------

There are many great scripting languages that would deserve a mention in this guide, but they are not in active development anymore. However, the following 13 scripting languages are **regularly updated and also being used in production**.

So if you are thinking about learning a new scripting language as a new professional path, they are all worth a shot.

1.  [JavaScript/ECMAScript](#1-javascriptecmascript)
2.  [PHP](#2-php)
3.  [Python](#3-python)
4.  [Ruby](#4-ruby)
5.  [Groovy](#5-groovy)
6.  [Perl](#6-perl)
7.  [Lua](#7-lua)
8.  [Bash](#8-bash)
9.  [PowerShell](#9-powershell)
10.  [R](#10-r)
11.  [VBA](#11-vba)
12.  [Emacs Lisp](#12-emacs-lisp)
13.  [GML](#13-gml)

### 1\. JavaScript/ECMAScript[](#1-javascriptecmascript)

JavaScript is an implementation of the [ECMA-262 standard](https://www.ecma-international.org/publications-and-standards/standards/ecma-262) that defines the ECMAScript (ES) general-purpose scripting language. In other words, JavaScript is a dialect of the ECMAScript language, therefore it doesn’t have a standalone specification but uses the [same syntax](https://262.ecma-international.org/11.0) as ECMAScript.

JavaScript has first-class functions (functions are treated as variables) and supports prototype-based object-oriented programming (existing objects are reused as prototypes).

#### Code Example[](#code-example)

ECMAScript uses a curly bracket syntax. The following JavaScript code example adds numbers from 1 to 10 together and outputs the result into the console (you can test it in your web browser’s JavaScript console by hitting F12):

    let total = 0, count = 1;
    
    while (count <= 10) {
        total += count;
        count += 1;
    }
    
    console.log(total);
    // 55
    

Source: [Eloquent JavaScript by Marijn Haverbeke: Introduction](https://eloquentjavascript.net/00_intro.html)

#### Use Cases and Environments[](#use-cases-and-environments)

JavaScript is the scripting language used by modern web browsers, such as Chrome’s [V8 engine](https://v8.dev) and Mozilla’s [SpiderMonkey engine](https://spidermonkey.dev). Besides, frontend web development, it can be used in non-browser environments as well. The [NodeJS](https://nodejs.org/en) runtime environment has been created to enable web developers to use it on the backend.

The shells of some NoSQL database management systems, such as [MongoDB](https://www.mongodb.com) and [Apache CouchDB](https://couchdb.apache.org), and some relational database management systems, such as the aforementioned MySQL Shell, also use it as a scripting language.

### 2\. PHP[](#2-php)

[PHP](/kba/what-is-php) is a general-purpose, open source scripting language used in backend web development. The acronym originally stood for ‘Personal Home Page’, as PHP was first created to add dynamic functionalities to static HTML pages.

Since then, PHP has evolved into a standalone language, so now the acronym is used in the sense of ‘Hypertext Preprocessor’. PHP is loosely typed (you don’t have to declare the data types of variables), can be embedded into HTML documents, and has object-oriented features too.

#### Code Example[](#code-example-1)

PHP has a C-like syntax. The following PHP code example creates a numeric array with four elements, loops through them, multiples each item by two, and unsets the `$value` variable when the loop is over.

    <?php
    $arr = array(1, 2, 3, 4);
    
    foreach ($arr as &$value) {
       $value = $value * 2;
    }
    // $arr is now array(2, 4, 6, 8)
    
    unset($value);
    ?>
    

Source: [PHP documentation: Control Structures](https://www.php.net/manual/en/control-structures.foreach.php)

#### Use Cases and Environments[](#use-cases-and-environments-1)

PHP can be executed on different HTTP servers, with Apache and Nginx being the most popular ones.

The most common PHP server stacks are LAMP (Linux, Apache, MySQL, PHP), LEMP (Linux, Nginx, MySQL, PHP), and WAMP (Windows, Apache, MySQL, PHP), and MAMP (macOS, Apache, MySQL, PHP).

It’s also used by many popular content management systems (CMS) such as WordPress, Drupal, and Joomla, and web application frameworks such as Laravel, Symfony, and CodeIgniter, that are all built on top of the PHP language and enhance it with extra functionalities.

You can use PHP for local WordPress development, too. Check out our in-depth guide on the main differences between Javascript and PHP.

### 3\. Python[](#3-python)

[Python](https://www.python.org) is currently the [second most popular coding language](https://madnight.github.io/githut/#/pull_requests/2020/3) on GitHub (after JavaScript). It’s loved for its clear and concise syntax — when coding in Python, you have to type much less than in most languages.

Python is a free and open source project, managed by the Python Software Foundation. It supports the structured, object-oriented, and functional programming paradigms, and has an extensive [Standard Library](https://docs.python.org/3/library/index.html#library-index) that is a collection of commonly used Python modules.

#### Code Example[](#code-example-2)

Python doesn’t use curly brackets and semicolons are optional, so the code is easy to read and write. The following Python code example loops through integers between 0 and 4, and prints them out:

    count = 0
    while count < 5:
       print(count)
          count += 1
    

Source: [Learn Python: Loops](https://www.learnpython.org/en/Loops)

#### Use Cases and Environments[](#use-cases-and-environments-2)

The most popular Python implementation is [CPython](https://github.com/python/cpython), written in the C language. It’s also the reference implementation that you download together with the Python language. Even though Python is an interpreted language, CPython uses both a compilation and interpretation step. First, it compiles the source code into bytecode (not the same as machine code) that it interprets at runtime.

Besides CPython, Python has other runtime environments as well, most importantly [PyPy](https://www.pypy.org) that omits the compilation step and only does JIT (just-in-time) interpretation. Python implementations are cross-platform, meaning they run on multiple operating systems, including Linux, Windows, and macOS.

The Python language is frequently used in machine learning, backend web development ([Django](https://www.djangoproject.com) being the most popular web framework), data analytics, automation, scientific computing, and web scraping.

To find out the best way to learn Python, check out our blog post on [Python tutorials](/blog/python-tutorials).

### 4\. Ruby[](#4-ruby)

[Ruby](https://www.ruby-lang.org/en) is an open source, general-purpose scripting language with a compact and easy-to-read syntax. It follows the principles of object-oriented programming and lets you write clean and logical code, making it one of the [easiest programming language to learn](/blog/best-programming-language-to-learn). In Ruby, everything is an object — even types that are primitives in most languages, such as booleans and integers.

Object-oriented concepts such as inheritance, mixins, and metaclasses are also heavily used.

Although Ruby has a purely object-oriented design, it also supports procedural programming (functions and variables defined outside of classes belong to the `Self` object) and functional programming (through anonymous functions, closures, and continuations).

#### Code Example[](#code-example-3)

Ruby has a concise syntax similar to Python. The following Ruby code example defines the `KaraokeSong` class as a subclass of the `Song` class:

    class KaraokeSong < Song
       def initialize(name, artist, duration, lyrics)
          super(name, artist, duration)
          @lyrics = lyrics
       end
    end
    

Source: [Programming Ruby reference guide: Classes, Objects, and Variables](http://ruby-doc.com/docs/ProgrammingRuby)

#### Use Cases and Environments[](#use-cases-and-environments-3)

Ruby is mainly used in backend web development, powering some robust web application frameworks such as [Ruby on Rails](https://rubyonrails.org). Many popular websites and applications run on Ruby on Rails, such as Airbnb, Shopify, [GitHub](/kba/what-is-github), and Hulu.

Ruby is also the language many popular web development tools are written in, most notably the [Sass](https://sass-lang.com) CSS preprocessor, the [Jekyll](https://jekyllrb.com) static website generator, and the [Vagrant](https://www.vagrantup.com) virtual machine environment.

The default implementation of Ruby is YARV (Yet Another Ruby Virtual Machine). It changed Ruby’s original interpreter [Matz’s Ruby Interpreter](https://www.ruby-lang.org/en/about) (also Ruby MRI or CRuby) that had been criticized for issues with speed and scalability.

There are also several competing runtime environments for Ruby, such as [JRuby](https://www.jruby.org) (lets you run Ruby on the Java Virtual Machine), [mruby](https://github.com/mruby/mruby) (a lightweight implementation that you can embed within your application), [TruffleRuby](https://github.com/oracle/truffleruby) (Oracle’s Ruby interpreter built on GraalVM), [Rubinius](https://github.com/rubinius/rubinius) (a cloud-native virtual machine for Ruby), and [others](https://github.com/codicoscepticos/ruby-implementations#active).

### 5\. Groovy[](#5-groovy)

[Groovy](https://groovy-lang.org) is an incredible flexible language written for the Java Virtual Machine (JVM) that can be used both as a scripting and programming language. It’s an open source project maintained by the Apache Software Foundation. Groovy is an object-oriented language that extends the [`java.lang.Object`](https://docs.oracle.com/javase/10/docs/api/java/lang/Object.html) superclass.

It supports both static and dynamic typing (type checking can be performed both at compile time and runtime) and has native support for lists, associative arrays, regular expressions, and markup languages such as HTML and XML.

You can use Groovy together with existing Java libraries.

#### Code Example[](#code-example-4)

Groovy has a Java-compatible syntax, using curly brackets. The following Groovy code example defines the `Coordinates` class with the latitude and longitude properties and the `getAt()` method:

    @Immutable
    class Coordinates {
       double latitude
       double longitude
    
       double getAt(int idx) {
          if (idx == 0) latitude
          else if (idx == 1) longitude
          else throw new Exception("Wrong coordinate index, use 0 or 1")
       }
    }
    

Source: [Groovy Documentation: Semantics](https://groovy-lang.org/semantics.html)

#### Use Cases and Environments[](#use-cases-and-environments-4)

As Groovy compiles into Java byte code, you can use it as a general-purpose programming language similar to Java. In this case, you can compile the source code into byte code before runtime using the [groovyc](http://www.groovy-lang.org/groovyc.html) compiler (the equivalent to javac).

However, there are also many Groovy implementations that let you use it as a scripting language. The most popular ones are the [Grails](https://grails.org) web application framework (formerly known as Groovy on Grails) and the [Gradle](https://gradle.org) build automation tool, but there are [several others](https://groovy-lang.org/ecosystem.html) too.

### 6\. Perl[](#6-perl)

[Perl](https://www.perl.org) is a general-purpose scripting language that’s been around for more than thirty years (since 1987). Originally, it was created as a UNIX scripting language for report processing. That’s also where its name comes from, as the Perl acronym standing for ‘Practical Extraction and Reporting Language’.

The Perl language became popular in the 1990s when programmers began to widely use it for CGI (Common Gateway Interface) scripting, which is an older interface specification for web servers (currently, it’s mainly used by legacy sites).

Despite being a relatively early player, Perl is still the 11th on the [TIOBE index](https://www.tiobe.com/tiobe-index) and the [21st most popular language on GitHub](https://madnight.github.io/githut/#/pull_requests/2020/3).

#### Code Example[](#code-example-5)

Perl’s syntax is similar to the C language. The Perl code example below first defines the `square()` subroutine that calculates and returns the square of a number, then passes the value 8 as an argument, runs the subroutine, and saves the result into the `$sq` variable:

    sub square {
       my $num = shift;
       my $result = $num * $num;
       return $result;
    }
    
    $sq = square(8);
    

Source: [Perl docs: Perl Intro](https://perldoc.perl.org/perlintro)

#### Use Cases and Environments[](#use-cases-and-environments-5)

Even though these days it’s not the most frequent choice of web developers, Perl can be successfully used in backend development. Besides the CGI runtime environment, it also executes on the Apache and Nginx web servers — the LAMP stack is actually LAMPP, standing for Linux, Apache, MySQL, PHP, and Perl.

There also exist some Perl web development frameworks, with [Catalyst](http://catalyst.perl.org), [Mojolicious](https://metacpan.org/dist/Mojolicious), and [Dancer](https://perldancer.org) being the most popular ones.

Perl is used by several notable websites and applications such as Amazon, IMDB, Booking.com, and the BBC iPlayer. It’s used in other areas, too, such as network programming and system administration. You can also check out the [Comprehensive Perl Archive Network (CPAN)](https://www.perl.org/cpan.html) where 25,000+ open-source Perl projects are available for you to download.

### 7\. Lua[](#7-lua)

[Lua](http://www.lua.org) is a fast and lightweight scripting language. The word ‘lua’ means ‘moon’ in Portuguese, as the language is developed and maintained by the Pontifical Catholic University of Rio de Janeiro in Brazil. Lua supports the procedural, object-oriented, and functional programming paradigms.

As Lua’s interpreter is written in C, it can be easily embedded into applications using its C API. That being said, you can use Lua to extend existing applications written in C-based languages such as C, C++, C#, Java, Perl, Ruby, and others.

#### Code Example[](#code-example-6)

Lua has a concise and easy-to-read syntax, similar to Python and Ruby. The following Lua code example shows how to use the `if-then-else` statement. First, it evaluates the `op` variable, then performs basic arithmetic operations depending on its value:

    if op == "+" then
       r = a + b
    elseif op == "-" then
       r = a - b
    elseif op == "*" then
       r = a * b
    elseif op == "/" then
       r = a / b
    else
       error("invalid operation")
    end
    

Source: [Programming in Lua reference guide: Statements](https://www.lua.org/pil/4.3.1.html)

#### Use Cases and Environments[](#use-cases-and-environments-6)

The default Lua implementation doesn’t interpret source code directly but first compiles it into byte code that it later executes on the Lua virtual machine. As all this happens at runtime, there’s no manual compilation step you need to perform (even though you can opt for compiling Lua before runtime to improve performance).

There are other Lua implementations as well, such as [LuaJIT](https://github.com/LuaJIT/LuaJIT), [LuaVela](https://github.com/luavela/luavela), and [many others](http://lua-users.org/wiki/LuaImplementations).

Lua is frequently used to develop video games, such as Angry Birds, World of Warcraft, and Grim Fandango. As it’s easy to embed, it’s also a frequent choice for embedded devices such as set-top boxes, instrument panels of cars (e.g. Volvo), IP cameras (e.g. Cisco), and others.

It can also be used in web development, as both Apache and Nginx servers have a Lua module (here’s Apache’s [mod\_lua](https://httpd.apache.org/docs/trunk/mod/mod_lua.html), and here’s Nginx’s [ngx\_http\_lua\_module](https://github.com/openresty/lua-nginx-module)). Wikipedia [chose Lua](https://en.wikipedia.org/wiki/Wikipedia:Wikipedia_Signpost/2012-01-30/Technology_report) as its template scripting language, and the UI of Adobe Photoshop Lightroom is written in Lua as well.

### 8\. Bash[](#8-bash)

[Bash](https://www.gnu.org/software/bash) is the name of both a command-line interpreter (shell) for the GNU operating system and the belonging scripting language. ‘Linux’ is, in fact, the [GNU operating system using the Linux kernel](https://www.gnu.org/gnu/gnu-linux-faq.html#what) (a kernel is the core part of the OS, it’s the first program that the operating system loads).

It’s a replacement for the original [UNIX Bourne shell (sh)](https://steve-parker.org/sh/bourne.shtml) — the Bash acronym stands for ‘Bourne Again SHell’ (a pun on ‘born again shell’).

Besides being the superset to the Bourne shell syntax, Bash also includes features from other shell scripting languages such as [KornShell (ksh)](https://github.com/att/ast) and [C shell (csh)](http://bxr.su/NetBSD/bin/csh) — for example, command-line editing and command history. You can use Bash in an interactive mode (executing one command at a time and waiting for the machine’s reply) and scripting mode (running a set of commands — a Bash script — at once).

#### Code Example[](#code-example-7)

Like most CLI scripting languages, Bash has a simple and descriptive syntax. The following Bash code example selects a file from the current folder and outputs a message containing the name and index of the file:

    select fname in *;
    do
       echo you picked $fname \($REPLY\)
       break;
    done
    

Source: [Bash Reference Manual: Conditional Constructs](https://www.gnu.org/software/bash/manual/bash.html)

#### Use Cases and Environments[](#use-cases-and-environments-7)

You can use Bash to make changes and perform different actions related to your operating system, such as executing commands, carrying out tasks that most people would do using a graphical user interface (e.g. creating, moving, or deleting folders and files), customizing and automating administrative tasks, connecting to a remote server, and many others.

Bash is the default shell for many Unix-based operating systems, including most Linux distros and all macOS releases up to [macOS Catalina](https://apps.apple.com/us/app/macos-catalina/id1466841314?mt=12) that replaced Bash with [Z shell (Zsh)](https://www.zsh.org) in 2019. You can also run Bash scripts on Windows 10, using the [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl) compatibility layer developed by Microsoft.

### 9\. PowerShell[](#9-powershell)

Originally, [PowerShell](https://learn.microsoft.com/en-us/powershell) was a command-line shell and scripting language solely for the Windows operating system. Since then, Microsoft open sourced and moved it from the [.NET Framework](https://dotnet.microsoft.com), which can create only Windows applications, to [.NET Core](https://github.com/dotnet/core), which can create applications for Windows, Linux, and macOS. This means PowerShell is now cross-platform.

It has also been renamed from Windows PowerShell to PowerShell Core, corresponding to the underlying framework. Unlike most command-line shells, PowerShell accepts and returns .NET objects instead of plain text, which gives way to new opportunities in task automation.

#### Code Example[](#code-example-8)

PowerShell has a compact syntax that makes working in the command line faster. The PowerShell code example below creates a backup of the boot.ini file and saves it to the boot.bak file:

    Copy-Item -Path C:\boot.ini -Destination C:\boot.bak

Source: [PowerShell Documentation: Working with Files and Folders](https://learn.microsoft.com/en-us/powershell/scripting/samples/working-with-files-and-folders?view=powershell-7.3&viewFallbackFrom=powershell-7)

#### Use Cases and Environments[](#use-cases-and-environments-8)

You can use PowerShell on the Windows, Linux, macOS operating systems, and some ARM devices (e.g. wearables, multimedia players, tablets, and other consumer electronic devices).

You can use PowerShell for system administration, task automation, and configuration management. To find PowerShell modules and scripts, you can check out the [PowerShell Gallery](https://www.powershellgallery.com) and Microsoft’s [official sample script collection](https://learn.microsoft.com/en-us/powershell/scripting/samples/sample-scripts-for-administration?view=powershell-7.3&viewFallbackFrom=powershell-7), too.

### 10\. R[](#10-r)

[R](https://www.r-project.org) is both a software environment and scripting language that you can use for statistical computing, data analysis, and graphical display. It’s a free and open source GNU project and an implementation of the [S](https://web.archive.org/web/20181014111802/http://ect.bell-labs.com/sl/S) statistical computing language (not in active development anymore).

R allows you to use many different statistical techniques such as classical statistical tests, clustering, time series analysis, linear and non-linear modeling, and others.

#### Code Example[](#code-example-9)

R’s syntax is different from most scripting languages and has some unusual elements, too — for instance, the primary assignment operator is `<-` instead of the `=` equals sign and it has loopless loops — see more about the quirks of the R syntax in this [beginner’s guide to R](https://www.computerworld.com/article/2497319/business-intelligence-beginner-s-guide-to-r-syntax-quirks-you-ll-want-to-know.html) by Sharon Machlis.

The following R code example defines a `names` attribute for the `fruit` vector (basic data structure in R that contains elements of the same type) that uses alphanumeric names (`orange`, `banana`, `apple`, `peach`) to help identify its components. Later, the `lunch` (or another) subvector can access each component using its alias name:

    > fruit <- c(5, 10, 1, 20)
    > names(fruit) <- c("orange", "banana", "apple", "peach")
    > lunch <- fruit[c("apple","orange")]
    

Source: [An Introduction to R: Index vectors; selecting and modifying subsets of a data set](https://cran.r-project.org/doc/manuals/r-release/R-intro.html#Index-vectors)

#### Use Cases and Environments[](#use-cases-and-environments-9)

The R software environment is cross-platform; you can run it on Windows, Linux, and macOS operating systems. The default R implementation is also available from some other scripting languages such as [Python](https://rpy2.github.io) and [Perl](https://metacpan.org/pod/Statistics::R). This means that you can access all the statistical functionality of R using these scripting languages.

Besides the default R environment, you can use the R scripting language in other environments as well, such as [pqR](http://www.pqr-project.org) (stands for ‘a pretty quick version of R’) and [Renjin](https://www.renjin.org) (an R implementation on top of the Java Virtual Machine).

### 11\. VBA[](#11-vba)

[VBA](https://learn.microsoft.com/en-us/office/vba/api/overview/library-reference) stands for Visual Basic for Applications and it’s an implementation of the [Visual Basic 6](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-basic-6/visual-basic-6.0-documentation?redirectedfrom=MSDN) programming language (not in active development since 2008). It has been created for Microsoft Office applications to enable developers to automate repetitive tasks, add new functionalities, and interact with the end users of documents.

Similar to Visual Basic, VBA follows the event-driven programming paradigm that puts events such as user actions into the center that drive the flow of the program.

As Microsoft Office applications have a graphical user interface, you can attach VBA scripts to menu buttons, keyboard shortcuts, macros (programmable patterns), and [OLE](https://learn.microsoft.com/en-us/cpp/mfc/ole-background?view=msvc-170&viewFallbackFrom=vs-2019) events (Object Linking and Embedding that lets you control one application from another; it’s a proprietary Microsoft technology).

#### Code Example[](#code-example-10)

As VBA is based on Visual Basic (which is an augmentation of BASIC), it uses a syntax similar to the languages of the BASIC (Beginners’ All-purpose Symbolic Instruction Code) family — which means it’s very beginner-friendly.

The VBA code example below uses the [`GetCertificateDetail()`](https://learn.microsoft.com/en-us/office/vba/api/office.signatureinfo.getcertificatedetail) method of the `SignatureInfo` object to get the expiration date of a digital certificate:

    Sub GetCertDetails()
    Dim objSignatureInfo As SignatureInfo
    Dim varDetail As Variant
    
    strDetail = objSignatureInfo.GetCertificateDetail(certdetExpirationDate)
    
    End Sub
    

Source: [Office VBA Reference: SignatureInfo object](https://learn.microsoft.com/en-us/office/vba/api/office.signatureinfo)

#### Use Cases and Environments[](#use-cases-and-environments-10)

The VBA scripting language is embedded into most Microsoft Office applications, respectively Access, Excel, Office for Mac, Outlook, PowerPoint, Project, Publisher, Visio, and Word — each having a [separate reference guide](https://learn.microsoft.com/en-us/office/vba/api/overview) on Microsoft’s documentation site while general VBA concepts are detailed in the [library reference](https://learn.microsoft.com/en-us/office/vba/api/overview/library-reference).

Besides Microsoft Office applications, there are other apps that also support VBA, such as [AutoCAD](https://www.autodesk.com/products/autocad/overview) and [CorelDRAW](https://www.coreldraw.com/en).

### 12\. Emacs Lisp[](#12-emacs-lisp)

[Emacs Lisp](https://www.gnu.org/software/emacs/manual/html_node/elisp) is a domain-specific scripting language designed for the [GNU Emacs](https://www.gnu.org/software/emacs) text editor. It’s a dialect of the Lisp programming language family (the name comes from LISt Processor).

As Emacs Lisp has been designed to be used within a code editor, it comes with a feature set specific to that environment, such as text scanning and parsing, buffer (objects with editable text) and display management, and others.

The Emacs Lisp scripting language is closely integrated with the editor interface itself, so every command is also a Lisp function that you can call from your script, and customization parameters are Lisp variables as well.

#### Code Example[](#code-example-11)

The syntax of Emacs Lisp is based on a fully parenthesized prefix notation that can be a bit hard to read at first if you haven’t worked with any Lisp language before.

The following Emacs Lisp code example defines two variables (symbols) and assigns a list of values to each — a list of trees (`pine`, `fir`, `oak`, `maple`) to the symbol `trees` and a list of herbivores (`gazelle`, `antelope`, `zebra`) to the symbol `herbivores`:

    (setq trees '(pine fir oak maple)
       herbivores '(gazelle antelope zebra))
    

Source: [An Introduction to Programming in Emacs Lisp: Setting the Value of a Variable](https://www.gnu.org/software/emacs/manual/html_node/eintr/Using-setq.html#Using-setq)

#### Use Cases and Environments[](#use-cases-and-environments-11)

The Emacs text editor is a cross-platform application that you can install on Windows, Linux, and macOS machines.

Using the Emacs Lisp scripting language, you can extend and customize the code editor, repeat and automate processes, create graphs, restrict focus to specific areas (for security), search regular expressions, store text, define modes and keymaps, ask questions from users, and perform many other actions.

There are also some configuration frameworks for Emacs Lisp — [Doom Emacs](https://github.com/doomemacs/doomemacs) and [Spacemacs](https://www.spacemacs.org) being the most well-known ones.

### 13\. GML[](#13-gml)

The acronym [GML](https://manual.yoyogames.com/#t=Content.htm) stands for GameMaker Language. It’s a good example of a domain-specific scripting language used in game development. GML is a proprietary scripting language belonging to [GameMaker Studio 2](https://gamemaker.io/en), a cross-platform game engine and development platform owned and maintained by YoYo Games.

Even though GML is mainly used for controlling game objects, it’s not an object-oriented language but a procedural one. It allows you to call custom scripts from any game object.

Besides the GML scripting language, GameMaker Studio 2 also has a visual scripting tool called [Drag and Drop (DnD)](https://docs2.yoyogames.com/source/_build/3_scripting/1_drag_and_drop_overview/index.html). Due to the flexible nature of GameMaker Studio 2, you can mix DnD with your GML scripts, too.

#### Code Example[](#code-example-12)

The syntax of GML is similar to JavaScript and other C-like languages.

The following GML code example makes a game object move horizontally towards the mouse pointer on the screen at a speed of 5 pixels per step. Once it reaches the current position of the pointer, the script creates an explosion effect layer, runs it (there’s an explosion effect on the screen), then destroys the instance (the explosion effect gets removed):

    if mp_linear_step(mouse_x, mouse_y, 5, 0) {
       instance_create_layer(x, y, "Effects", obj_Explosion);
       instance_destroy();
    }
    

Source: [GameMaker Studio 2 Docs – Scripting – GML Reference – Movement and Collisions – Motion Planning](https://manual.yoyogames.com/#t=Content.htm)

#### Use Cases and Environments[](#use-cases-and-environments-12)

GML is interpreted by GameMaker Studio 2 that you need to purchase if you want to develop games in this scripting language.

Pricing depends on the [platform](https://gamemaker.io/en/get) you want to create games for — Mac and Windows games being the cheapest ones; cross-platform (Windows, macOS, Ubuntu) desktop games, HTML5 web games, UWP (Universal Windows Platform) games, and cross-platform (Android, Fire, iOS) mobile games being in the mid-tier; and PS4, Xbox One, and Nintendo Switch being the most expensive ones.

Some examples of video games created with GML include [Blackhole](https://www.blackhole-game.com/en/about), [10 Second Ninja X](http://www.10second.ninja), [Death’s Gambit](http://www.deathsgambit.com), [Deltarune](https://deltarune.com), and several others.

Summary[](#summary)
-------------------

There’s no doubt that scripting languages are fascinating. They have many different variations, syntaxes, and implementations, and can be used for plenty of things.

From building dynamic websites, to automating system administration, to creating video games, and so forth.

The three most important things to remember about scripting languages are:

They can’t run on their own but always need an environment (implementation, runtime) with an interpreter for that scripting language.

Sometimes you can use general-purpose scripting languages to access environments and platforms primarily created for other programming or scripting languages. Think of JRuby (lets you run Ruby on the Java Virtual Machine), Renjin (R implementation also on the JVM), Rpy2 (R interface that you can use from Python), as good examples.

Finally, before learning a new scripting language, it’s always a good idea to check out its current popularity using the [TIOBE index](https://www.tiobe.com/tiobe-index) or [GitHut](https://madnight.github.io/githut).

Depending on it, you will also find more or fewer sample scripts, GitHub repositories, module libraries, reference guides, detailed manuals, and app showcases that will help you get started with the language… and get better-paid projects and jobs!

