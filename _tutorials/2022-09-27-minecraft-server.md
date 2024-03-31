---
layout: post
title: Hosting a Minecraft Server on Linux
description: A step by step guide
date:   2022-09-27 00:00:00 -0800
author: horacio 
image:  '/images/minecraft.jpg'
tags:   [technology]
tags_color: '#cc7690'
featured: true
---
Key steps we’ll cover in this guide:

1. Installing Java
2. Installing the Minecraft server
3. Launching the server

## Install Java
### Install Java on AWS Linux

{% highlight bash %}
sudo rpm --import https://yum.corretto.aws/corretto.key
sudo curl -L -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo
sudo yum install -y java-17-amazon-corretto-devel
{% endhighlight %}

## Install Java on Ubuntu
Update the repository to ensure you download the latest version of OpenJDK

{% highlight bash %}
sudo apt update
{% endhighlight %}

Install the latest Java Development Kit

{% highlight bash %}
sudo apt install default-jdk
{% endhighlight %}

## Install Java on CentOS
Start by updating the package repository

{% highlight bash %}
sudo yum update
{% endhighlight %}

Install the Java Development Kit with

{% highlight bash %}
sudo yum install java-11-openjdk-devel
{% endhighlight %}

Verify Java is installed by running:

{% highlight bash %}
java -version
{% endhighlight %}

The output should respond with the version of OpenJDK installed on the system.

## Installing the Minecraft server

The steps to install and launch the server are much the same as any other install — download the file, put it somewhere permanent and run it. We'll do that through the command line.

We’ll also create a dedicated user for the server on the instance

{% highlight bash %}
sudo adduser minecraft
{% endhighlight %}

After the user is created, we’ll make directories and download the latest version of the Minecraft server into them, then provide access to the "minecraft" user.

{% highlight bash %}
sudo mkdir /opt/minecraft/
sudo mkdir /opt/minecraft/server/
cd /opt/minecraft/server
wget https://piston-data.mojang.com/v1/objects/f69c284232d7c7580bd89a5a4931c3581eae1378/server.jar
sudo chown -R minecraft:minecraft /opt/minecraft/
{% endhighlight %}

The URL for the latest version of the server can be found on the official Minecraft server page. Minecraft has now been downloaded on the machine and is almost ready to run.

## Launching the Minecraft Server
A little trick with running the Minecraft server for the first time is that you have to run it once, edit a eula.txt file to agree with the license and then start it again before it will run. The next steps show how to do this using vi.

We’ll swap to the user and move to the server directory.

{% highlight bash %}
sudo su minecraft
cd /opt/minecraft/server/
{% endhighlight %}

Run the following command to start the server. If you are using a different Minecraft server filename, update the command accordingly.

{% highlight bash %}
java -Xmx1024M -Xms1024M -jar server.jar nogui
{% endhighlight %}

The command will error and say you need to agree to the eula. Do so by running the following command

{% highlight bash %}
vi eula.txt
{% endhighlight %}

Navigate to the “eula=false” statement, press i and edit it to say “eula=true”. Press escape and type :x to save and exit. Any Minecraft server specific settings can be modified in a similar way using vi in the server.properties file.

Start the server again using the same command as above. Minecraft server is running and will be available to log in after world generation is complete.

## Install Screen
Screen is a console application that keeps your server running when you’re not connected.

Install Screen on Ubuntu with:

{% highlight bash %}
sudo apt install screen
{% endhighlight %}

To install Screen on CentOS, run:

{% highlight bash %}
sudo yum install screen
{% endhighlight %}

## Run Screen
Start a Screen session using the screen command and add the -S option to name the session:

{% highlight bash %}
screen -S "Minecraft server"
{% endhighlight %}

## Run Your Minecraft Server
Start the Minecraft server by running the java command to execute the jar file

{% highlight bash %}
java -Xmx1024M -Xms1024M -jar server.jar nogui
{% endhighlight %}

Wait for the system to finish executing. You should get a message when the process is done, at this point the Minecraft server is up and running.

You can now detach from the Minecraft screen by pressing Ctrl+a+d.

To reattach to the screen, press Ctrl+r.

