---
layout: post
title: Please Linux 
date:   2022-09-24 00:00:00 -0800
categories: jekyll 
description: Forgot to use 'sudo'?
author: horacio 
image:  '/images/sudo_please.jpg'
tags:   [technology]
tags_color: '#477690'
---
How many times do we forget to include 'sudo' while typing an important command just to manually type the whole command all over again after getting an 'access denied' error? Too many times to count. Well, thanks to aliases in linux, we can have a bit of fun by creating an alias to help us repeat the command with sudo.

The easiest way to repeat the command is by doing


{% highlight bash %}
  sudo !!
{% endhighlight %}

Linux keeps a history of any commands you type. If you type the command 'history', you'll see a list of previously ran commands. Each command is assigned a number.

{% highlight bash %}
  bash-3.2$ history 5
    14  whoami
    15  pwd
    16  ls -la
    17  vi .bashrc 
    18  history 5
  bash-3.2$
{% endhighlight %}

You can repeat any of the previous commands by typing an exclamation mark followed by the command number from the history list. By typing two exclamations marks, you can run the very last command.

An alias is just a name we can use to assign any command. For example we could assign 'sudo !!' to an alias called please (alias please = 'sudo !!'). An issue with this is that the exclamation marks included with the alias are not interpreted correctly. One way to correct this is to use a command that uses the history log ('$(fc -ln -1)').

***Note: *** fc is a built-in command in the bash shell that lists, edits and executes commands previously entered to an interactive shell. This is the final command:


{% highlight bash %}
  alias please = 'sudo $(fc -ln -1)'
{% endhighlight %}

Follow these quick steps to add the alias permanently in your linux system.

Edit the ~/.bash_aliases or ~/.bashrc (recommended) file using a text editor:

{% highlight bash %}
  vi ~/.bash_aliases
# or #
  nano ~/.bashrc
{% endhighlight %}

Append your bash alias

{% highlight bash %}
  alias please = 'sudo $(fc -ln -1)'
{% endhighlight %}

Save and close the file.

Activate alias by typing the following source command:

{% highlight bash %}
  source ~/.bashrc
{% endhighlight %}

Note: Please note that ~/.bash_aliases file only works if the following line exists in the ~/.bashrc file:

{% highlight bash %}
  if [ -f ~/.bash_aliases ]; then
  . ~/.bash_aliases
  fi
{% endhighlight %}

And that's it. Next time you forget to run a command with sudo, just type 'please' and linux will re-run your previous command appended with sudo.

