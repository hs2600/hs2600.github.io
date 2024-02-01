---
layout: post
title:  Linux Commands
date:   2024-01-26 00:01:00 -0800
description: Some of the most common Linux commands
author: horacio 
image:  '/images/linux.webp'
tags:   [technology, linux]
tags_color: '#477690'
---

As of writing this, Linux has a [worldwide market share of 2.68%](https://gs.statcounter.com/os-market-share/desktop/worldwide) on desktops, but over 90% of all cloud infrastructure and hosting services run in this operating system. For this reason alone, it is crucial to be familiar with popular Linux commands.

According to a [StackOverflow survey](https://insights.stackoverflow.com/survey/2020#technology-platforms), Linux is the most-used operating system by professional developers, with an impressive 55.9% of the market share. It isn’t just a coincidence. Linux is free and open-source, has better security than its competitors, and boasts a powerful command line that makes developers and power users more effective. You also have access to a powerful package manager and a bunch of development tools.

Whether you’re an experienced Sysadmin or a Linux newcomer, you can take advantage of this guide.

Let’s begin!

### Table of Contents

1.  [What Is a Linux Command?](#what-is-a-linux-command)
2.  [The 40 Most-Used Linux Commands](#mostused-linux-commands)
3.  [Linux Commands Cheat Sheet](#linux-commands-cheat-sheet)
4.  [Linux Commands FAQ](#linux-commands-faq)

What Is a Linux Command?[](#what-is-a-linux-command)
----------------------------------------------------

A Linux command is a program or utility that runs on the command line. A command line is an interface that accepts lines of text and processes them into instructions for your computer.

Any graphical user interface (GUI) is just an abstraction of command-line programs. For example, when you close a window by clicking on the “X,” there’s a command running behind that action.

A **flag** is a way we can pass options to the command you run. Most Linux commands have a help page that we can call with the flag `-h`. Most of the time, flags are optional.

An **argument** or parameter is the **input** we give to a command so it can run properly. In most cases, the argument is a file path, but it can be anything you type in the terminal.

You can invoke flags using hyphens (`-`) and double hyphens (`--`), while argument execution depends on the order in which you pass them to the function.

The 40 Most-Used Linux Commands[](#mostused-linux-commands)
------------------------------------------------------------------

Before jumping into the most-used Linux commands, make sure to fire up a **terminal**. In most Linux distributions, you would use Ctrl + Alt + T to do so. If this isn’t working, search in your application panel for “terminal.”

```bash
[horacio@fedora ~]$ 
```
> <cite>The Linux terminal emulator.<cite>

Now let’s dive into the 40 most-used Linux commands. Many of these have multiple options you can string to them, so make sure to [check out the commands’ manual](https://linux.die.net/man/1/cp).

### 1\. **`ls`** Command[](#1-ls-command)

`ls` is probably the first command every Linux user typed in their terminal. It allows you to list the contents of the directory you want (the current directory by default), including files and other nested directories.

    ls

It has many options, so it might be good to get some help by using the `--help` flag. This flag returns all the flags you can use with ls.

For example, to colorize the output of the `ls` command, you can use the following:

    ls --color=auto

```bash
[horacio@fedora ~]$ ls --color=auto
 anaconda3                                    intelephense
 anaconda3.old                                linescore.json
 bin                                         'Linux commands cheat sheet.pdf'
 Commands.txt                                 Music
```

> <cite>The colorized ls command.</cite>

Now the `ls` command output is colorized, and you can appreciate the difference between a directory and a file.

But typing `ls` with the color flag would be inefficient; that’s why we use the `alias` command.

### 2\. **`alias`** Command[](#2-alias-command)

The `alias` command lets you define temporary aliases in your shell session. When creating an alias, you instruct your shell to replace a word with a series of commands.

For example, to set `ls` to have color without typing the `--color` flag every time, you would use:

    alias ls="ls --color=auto"

As you can see, the `alias` command takes one key-value pair parameter: `alias NAME="VALUE"`. Note that the value must be inside quotes.

If you want to list all the aliases you have in your shell session, you can run the `alias` command without argument.

    alias

```bash
[horacio@fedora ~]$ alias
alias egrep='grep -E --color=auto'
alias fgrep='grep -F --color=auto'
alias grep='grep --color=auto'
alias l.='ls -d .* --color=auto'
alias ll='ls -l --color=auto'
```

> <cite>The alias command.</cite>

### 3\. **`unalias`** Command[](#3-unalias-command)

As the name suggests, the `unalias` command aims to remove an `alias` from the already defined aliases. To remove the previous `ls` alias, you can use:

    unalias ls

### 4\. **`pwd`** Command[](#4-pwd-command)

The `pwd` command stands for “print working directory,” and it outputs the absolute path of the directory you’re in. For example, if your username is “john” and you’re in your Documents directory, its absolute path would be: `/home/john/Documents`.

To use it, simply type `pwd` in the terminal:

    pwd
    
    # My result: /home/horacio/Documents/linux-commands

### 5\. **`cd`** Command[](#5-cd-command)

The `cd` command is highly popular, along with `ls`. It refers to “**c**hange **d**irectory” and, as its name suggests, switches you to the directory you’re trying to access.

For instance, if you’re inside your Documents directory and you’re trying to access one of its subfolders called **Videos**, you can enter it by typing:

    cd Videos

You can also supply the absolute path of the folder:

    cd /home/horacio/Documents/Videos

There are some tricks with the `cd` command that can save you a lot of time when playing around with it:

#### 1) Go to the home folder[](#1-go-to-the-home-folder)

    cd

#### 2) Move a level up[](#2-move-a-level-up)

    cd ..

#### 3) Return to the previous directory[](#3-return-to-the-previous-directory)

    cd -

### 6\. **`cp`** Command[](#6-cp-command)

It’s so easy to copy files and folders directly in the Linux terminal that sometimes it can replace conventional file managers.

To use the `cp` command, just type it along with the source and destination files:

    cp file_to_copy.txt new_file.txt

You can also copy entire directories by using the recursive flag:

    cp -r dir_to_copy/ new_copy_dir/

Remember that in Linux, folders end with a forward slash (`/`).

### 7\. **`rm`** Command[](#7-rm-command)

Now that you know how to copy files, it’ll be helpful to know how to remove them.

You can use the `rm` command to remove files and directories. Be careful while using it, though, because it’s very difficult (yet not impossible) to recover files deleted this way.

To delete a regular file, you’d type:

    rm file_to_copy.txt

If you want to delete an empty directory, you can use the recursive (`-r`) flag:

    rm -r dir_to_remove/

On the other hand, to remove a directory with content inside of it, you need to use the force (-f) and recursive flags:

    rm -rf dir_with_content_to_remove/

### Info[](#info)

Be careful with this — you can erase a whole day of work by misusing these two flags!

### 8\. **`mv`** Command[](#8-mv-command)

You use the `mv` command to move (or rename) files and directories through your file system.

To use this command, you’d type its name with the source and destination files:

    mv source_file destination_folder/
    
    mv command_list.txt commands/

To utilize absolute paths, you’d use:

    mv /home/horacio/BestMoviesOfAllTime ./

…where `./` is the directory you’re currently in.

You also can use `mv` to rename files while keeping them in the same directory:

    mv old_file.txt new_named_file.txt

### 9\. **`mkdir`** Command[](#9-mkdir-command)

To create folders in the shell, you use the `mkdir` command. Just specify the new folder’s name, ensure it doesn’t exist, and you’re ready to go.

For example, to make a directory to keep all of your images, just type:

    mkdir images/

To create subdirectories with a simple command, use the parent (`-p`) flag:

    mkdir -p movies/2004/

### 10\. **`man`** Command[](#10-man-command)

Another essential Linux command is `man`. It displays the manual page of any other command (as long as it has one).

To see the manual page of the `mkdir` command, type:

    man mkdir

You could even refer to the `man` manual page:

    man man

### 11\. **`touch`** Command[](#11-touch-command)

The `touch` command allows you to update the access and modification times of the specified files.

To change a file modification date to the current time, we need to use the `-m` flag:

    touch -m old_file

Nonetheless, most of the time, you won’t use `touch` to modify file dates, but rather to create new empty files:

    touch new_file_name

### 12\. **`chmod`** Command[](#12-chmod-command)

The `chmod` command lets you change the [mode of a file](https://wiki.archlinux.org/title/File_permissions_and_attributes) (permissions) quickly. It has a lot of options available with it.

The basic permissions a file can have are:

*   r (read)
*   w (write)
*   x (execute)

One of the most common use cases for `chmod` is to make a file executable by the user. To do this, type `chmod` and the flag `+x`, followed by the file you want to modify permissions on:

    chmod +x script

You use this to make scripts executable, allowing you to run them directly by using the `./` notation.

### 13\. **`./`** Command[](#13--command)

Maybe the `./` notation isn’t a command itself, but it’s worth mentioning in this list. It lets your shell run an executable file with any interpreter installed in your system directly from the terminal. No more double-clicking a file in a graphical file manager!

For instance, with this command, you can run a [Python script](/blog/python-object-oriented-programming) or a program only available in .run format. When running an executable, make sure it has executable (x) permissions, which you can modify with the `chmod` command.

Here’s a simple Python script and how we would run it with the `./` notation:

    
    #! /usr/bin/python3
    
    # filename: script
    
    for i in range(20):
    
    print(f"This is a cool script {i}")

Here’s how we’d convert the script into an executable and run it:

    chmod +x script
    
    ./script

### 14\. **`exit`** Command[](#14-exit-command)

The `exit` command does exactly what its name suggests: With it, you can end a shell session and, in most cases, automatically close the terminal you’re using:

    exit

### 15\. **`sudo`** Command[](#15-sudo-command)

This command stands for “superuser do,” and it lets you act as a superuser or root user while you’re running a specific command. It’s how Linux protects itself and prevents users from accidentally modifying the machine’s filesystem or installing inappropriate packages.

Sudo is commonly used to install software or to edit files outside the user’s home directory:

    sudo apt install gimp
    
    sudo cd /root/ 

It’ll ask you for the administrator’s password before running the command you typed after it.

### 16\. **`shutdown`** Command[](#16-shutdown-command)

As you may guess, the `shutdown` command lets you power off your machine. However, it also can be used to halt and reboot it.

To power off your computer immediately (the default is one minute), type:

    shutdown now

You can also schedule to turn off your system in a 24-hour format:

    shutdown 20:40

To cancel a previous `shutdown` call, you can use the `-c` flag:

    shutdown -c

### 17\. **`htop`** Command[](#17-htop-command)

`htop` is an interactive process viewer that lets you manage your machine’s resources directly from the terminal. In most cases, it isn’t installed d by default, so make sure to read more about it [on its download page](https://htop.dev/downloads.html).

    htop

### 18\. **`unzip`** Command[](#18-unzip-command)

The unzip command allows you to extract the content of a **.zip** file from the terminal. Once again, this package may not be installed by default, so make sure you install it with your package manager.

Here, we’re unpacking a .zip file full of images:

    unzip images.zip

### 19\. `apt`, `yum`, `pacman` commands[](#19-apt-yum-pacman-commands)

No matter which Linux distribution you’re using, it’s likely that you use package managers to install, update, and remove the software you use every day.

You can access these package managers through the command line, and you’d use one or another depending on the distro your machine is running.

The following examples will install [GIMP](https://www.gimp.org), a free and open source software usually available in most package managers:

#### Debian-based (Ubuntu, Linux Mint)[](#debianbased-ubuntu-linux-mint)

    sudo apt install gimp

#### Red Hat-based (Fedora, CentOS)[](#red-hatbased-fedora-centos)

    sudo yum install gimp

#### Arch-based (Manjaro, Arco Linux)[](#archbased-manjaro-arco-linux)

    sudo pacman -S gimp

### 20\. **`echo`** Command[](#20-echo-command)

The `echo` command displays defined text in the terminal — it’s that simple:

    echo "Cool message"

Its primary usage is to print environmental variables inside those messages:

    echo "Hey $USER"
    
    # Hey horacio

### 21\. **`cat`** Command[](#21-cat-command)

`Cat`, short for “concatenate,” lets you create, view, and concatenate files directly from the terminal. It’s mainly used to preview a file without opening a graphical text editor:

    cat long_text_file.txt

### 22\. **`ps`** Command[](#22-ps-command)

With `ps`, you can take a look at the processes your current shell session is running. It prints useful information about the programs you’re running, like process ID, TTY (TeleTYpewriter), time, and command name.

    ps

In case you want something more interactive, you can use `htop`.

### 23\. **`kill`** Command[](#23-kill-command)

It’s annoying when a program is unresponsive, and you can’t close it by any means. Fortunately, the `kill` command solves this kind of problem.

Simply put, `kill` sends a TERM or kill signal to a process that terminates it.

You can kill processes by entering either the PID (processes ID) or the program’s binary name:

    kill 533494
    
    kill firefox

Be careful with this command — with `kill`, you run the risk of accidentally deleting the work you’ve been doing.

### 24\. **`ping`** Command[](#24-ping-command)

`ping` is the most popular networking terminal utility used to test network connectivity. `ping` has a ton of options, but in most cases, you’ll use it to request a domain or IP address:

    ping google.com
    
    ping 8.8.8.8

### 25\. **`vim`** Command[](#25-vim-command)

`vim` is a free and open source terminal text editor that’s in used since the ’90s. It lets you edit plain text files using efficient keybindings.

Some people consider it difficult to use — [exiting Vim](https://stackoverflow.com/questions/11828270/how-do-i-exit-vim) is one of the most-viewed StackOverflow questions — but once you get used to it, it becomes your best ally in the command line.

To fire up Vim, just type:

    vim

### 26\. **`history`** Command[](#26-history-command)

If you’re struggling to remember a command, `history` comes in handy. This command displays an enumerated list with the commands you’ve used in the past:

    history

### 27\. **`passwd`** Command[](#27-passwd-command)

`passwd` allows you to change the passwords of user accounts. First, it prompts you to enter your current password, then asks you for a new password and confirmation.

It’s similar to any other change of password you’ve seen elsewhere, but in this case, it’s directly in your terminal:

    passwd

Be careful while using it — you don’t want to mess up your user password!

### 28\. **`which`** Command[](#28-which-command)

The `which` command outputs the full path of shell commands. If it can’t recognize the given command, it’ll throw an error.

For example, we can use this to check the binary path for [Python](/blog/python-tutorials) and the Brave web browser:

    which python
    
    # /usr/bin/python
    
    which brave
    
    # /usr/bin/brave

### 29\. **`shred`** Command[](#29-shred-command)

If you ever wanted a file to be almost impossible to recover, `shred` can help you with this task. This command overrides the contents of a file repeatedly, and as a result, the given file becomes extremely difficult to recover.

Here’s a file with little content in it:

Now, let’s have `shred` do its thing by typing the following command:

    shred file_to_shred.txt

If you want to delete the file right away, you can use the `-u` flag:

    shred -u file_to_shred.txt

### 30\. **`less`** Command[](#30-less-command)

`less` (opposite of [more](https://man7.org/linux/man-pages/man1/more.1.html)) is a program that lets you inspect files backward and forward:

    less large_text_file.txt

The neat thing about `less` is that it includes more and `vim` commands in its interface. If you need something more interactive than `cat`, `less` is a good option.

### 31\. **`tail`** Command[](#31-tail-command)

Similar to `cat`, `tail` prints the contents of a file with one major caveat: It only outputs the last lines. By default, it prints the last 10 lines, but you can modify that number with `-n`.

For example, to print the last lines of a large text file, you’d use:

    tail long.txt

To view only the last four lines:

    tail -n 4 long.txt

### 32\. **`head`** Command[](#32-head-command)

This one is complementary to the `tail` command. `head` outputs the first 10 lines of a text file, but you can set any number of lines you want to display with the `-n` flag:

    head long.txt
    
    head -n 5 long.txt

### 33\. **`grep`** Command[](#33-grep-command)

Grep is one of the most powerful utilities for working with text files. It searches for lines that match a [regular expression](https://regex101.com) and print them:

    grep "linux" long.txt

You can count the number of times the pattern repeats by using the `-c` flag:

    grep -c "linux" long.txt
    
    # 2

### 34\. **`whoami`** Command[](#34-whoami-command)

The `whoami` command (short for “who am i”) displays the username currently in use:

    whoami
    
    # horacio

You would get the same result by using `echo` and the environmental variable $USER:

    echo $USER
    
    # horacio

### 35\. **`whatis`** Command[](#35-whatis-command)

`whatis` prints a single-line description of any other command, making it a helpful reference:

    whatis python
    
    # python (1) - an interpreted, interactive, object-oriented programming language
    
    whatis whatis
    
    # whatis (1) - display one-line manual page descriptions

### 36\. **`wc`** Command[](#36-wc-command)

Wc stands for “word count,” and as the name suggests, it returns the number of words in a text file:

    wc long.txt
    
    # 37 207 1000 long.txt

Let’s breakdown the output of this command:

*   37 lines
*   207 words
*   1000 byte-size
*   The name of the file (long.txt)

If you only need the number of words, use the `-w` flag:

    wc -w long.txt
    
    207 long.txt

### 37\. **`uname`** Command[](#37-uname-command)

`uname`(short for “Unix name”) prints the operative system information, which comes in handy when you know your current Linux version.

Most of the time, you’ll be using the `-a` (–all) flag, since the default output isn’t that useful:

    uname
    
    # Linux
    
    uname -a
    
    # Linux horaciomanjaro 5.4.138-1-MANJARO #1 SMP PREEMPT Thu Aug 5 12:15:21 UTC 2021 x86_64 GNU/Linux

### 38\. **`neofetch`** Command[](#38-neofetch-command)

[Neofetch](https://github.com/dylanaraps/neofetch) is a CLI (command-line interface) tool that displays information about your system — like kernel version, shell, and hardware — next to an ASCII logo of your Linux distro:

    neofetch

In most machines, this command isn’t available by default, so make sure to install it with your package manager first.

### 39\. **`find`** Command[](#39-find-command)

The `find` command searches for files in a directory hierarchy based on a regex expression. To use it, follow the syntax below:

    find [flags] [path] -name [expression]

To search for a file named **long.txt** in the current directory, enter this:

    find ./ -name "long.txt" # ./long.txt 

To search for files that end with a **.py** (Python) extension, you can use the following command:

    find ./ -type f -name "*.py" ./get_keys.py ./github_automation.py ./binarysearch.py 

### 40\. **`wget`** Command[](#40-wget-command)

`wget` (World Wide Web get) is a utility to retrieve content from the internet. It has one of the largest collections of flags out there.

Here’s how you would download a Python file from a [GitHub](/kba/what-is-github) repo:

    wget https://example.com/test.py

Linux Commands Cheat Sheet[](#linux-commands-cheat-sheet)
---------------------------------------------------------

Whenever you want a quick reference, just review the below table:

Command

Usage

`ls`

Lists the content of a directory

`alias`

Define or display aliases

`unalias`

Remove `alias` definitions

`pwd`

Prints the working directory

`cd`

Changes directory

`cp`

Copies files and directories

`rm`

Remove files and directories

`mv`

Moves (renames) files and directories

`mkdir`

Creates directories

`man`

Displays manual page of other commands

`touch`

Creates empty files

`chmod`

Changes file permissions

`./`

Runs an executable

`exit`

Exits the current shell session

`sudo`

Executes commands as superuser

`shutdown`

Shutdowns your machine

`htop`

Displays processes and resources information

`unzip`

Extracts compressed ZIP files

`apt`, `yum`, `pacman`

Package managers

`echo`

Displays lines of text

`cat`

Prints file contents

`ps`

Reports shell processes status

`kill`

Terminates programs

`ping`

Tests network connectivity

`vim`

Efficient text editing

`history`

Shows a list of previous commands

`passwd`

Changes user password

`which`

Returns the full binary path of a program

`shred`

Overwrites a file to hide its contents

`less`

Inspects files interactively

`tail`

Displays last lines of a file

`head`

Displays first lines of a file

`grep`

Prints lines that match patterns

`whoami`

Outputs username

`whatis`

Shows single-line descriptions

`wc`

Word count files

`uname`

Displays OS information

`neofetch`

Displays OS and hardware information

`find`

Searches for files that follow a pattern

`wget`

Retrieves files from the internet

Linux Commands FAQ[](#linux-commands-faq)
-----------------------------------------

### What Is the Basic Command of Linux?[](#what-is-a-502-bad-gateway-error)

There’s actually a series of basic commands that are perfect for anyone who is getting started with Linux:

*   **pwd** (Prints the working directory)
*   **cat** (Prints file contents)
*   **cp** (Copies files and directories)
*   **mv** (Moves and renames files and directories)
*   **rm** (Remove files and directories)
*   **touch** (Creates empty files)
*   **mkdir** (Creates directories)

### How Many Commands Does Linux Have?[](#how-many-commands-does-linux-have)

There are thousands of commands (and new ones are being written daily). But don’t worry: there’s no need to remember any of them. You can always search for them online.

### Can You Teach Yourself Linux?[](#can-you-teach-yourself-linux)

It’s possible. You can find solid resources online to help you get started. But if you feel in need of a hand, here are some well-recommended courses:

*   [Linux Mastery](https://www.udemy.com/course/linux-mastery)
*   [The Linux Command Line Bootcamp](https://www.udemy.com/course/the-linux-command-line-bootcamp)
*   [Learn The Linux Command Line](https://www.udemy.com/course/command-line) (free)

Summary[](#summary)
-------------------

It can take some time to learn Linux, but once you master some of its tools, it becomes your best ally, and you won’t regret choosing it as your daily driver.

One of the remarkable things about Linux is that even if you’re an experienced user, you’ll never stop learning to be more productive using it.

_There are a lot more helpful Linux commands. If we’ve left something out, please share your favorite Linux commands in the comments below!_

