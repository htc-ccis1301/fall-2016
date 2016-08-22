---
title: "Install Git"
published: true
morea_id: install-git
morea_type: experience
morea_summary: "How to install git on Windows through GitHub Desktop, and check for and install git (if needed) on a Mac."
morea_sort_order: 2
---

# Install Git
The install process for git is different based on the type of computer you are using.  Install information is provided here for Windows & Mac OS.  If you are using Linux, it is likely that you already have git and if not can use the package manager to easily install it.

## Windows Users
If you are a Windows user, typically you will use PowerShell as your command shell.  However, Windows PowerShell does not include git by default.  The easiest way to get access to git on Windows is to use GitShell which is part of [GitHub Desktop](https://desktop.github.com/).

GitShell is PowerShell plus git commands, and since we will mainly be using the shell for git commands, you will want to use GitShell for your work in this course.  Because GitShell is built on top of PowerShell all other commands that you would use in PowerShell should also work in GitShell.

## Mac Users
If you are using a Mac, open up a [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) window and type git.  You may find that it is already installed, or if not that it will prompt you to install the XCode Command Line Developer Tools.  If it does not, you likely have an older version of the Mac OS and should download and install the tools from the [Apple Developer Site](https://developer.apple.com/downloads/index.action).  You can also install the full XCode suite from the Apple App Store, but this will take additional space.  

GitHub Desktop is not required, we only need the underlying git command, and actually I encourage you not to use the application itself, but there is also now a [GitHub Desktop for Mac](https://desktop.github.com/)

## Configure Git
Before you dive in, you'll want to configure git with your user information. In the commands below, fill in your name and the email you used with your GitHub account.  This email is what will tie your activity to your account.  **Make sure that you are using the same email and check for typos.**

{% highlight bash %}
$ git config --global user.name "User Name"
$ git config --global user.email "user@email"
{% endhighlight %}

I also recommend saving your git config as a Gist on GitHub so that it is easily available for you to use on any computer.
