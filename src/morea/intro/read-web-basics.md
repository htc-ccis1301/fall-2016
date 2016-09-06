---
title: "Internet & Web Basics"
published: true
morea_id: web-basics
morea_summary: "An introduction to web standards, architecture, and an overview of HTML."
morea_type: reading
morea_sort_order: 4
morea_labels:
 - textbook

---

# {{ page.title }}
Read Chapter 1 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers an introduction to web standards and architecture followed by an overview of HTML.

## Part 1 - Standards and Architecture
As you read through the first part of the chapter (pages 1-14), pay attention to the various standards and technologies that allow the internet to function.  You will need to be able to identify them and explain how they are used.  It is also important that you understand at a high-level the client/server architecture of the internet and how a web browser displays a web page.

<div style="padding:20px">
<div class="row">
<div class="col-xs-12 col-md-8">
  {%  include youtube.html  id="5o8CwafCxnU" %}
  Thanks to <a href="https://code.org">Code.org</a> for sharing the video!
</div>
</div>
</div>

<div style="padding:20px">
<div class="row">
<div class="col-xs-12 col-md-8">
  {%  include youtube.html  id="kBXQZMmiA4s" %}
  Thanks to <a href="https://code.org">Code.org</a> for sharing the video!
</div>
</div>
</div>

### Review Questions

 - What is the W3C and why is it important?
 - What is accessibility?  Why it is important?  
 - What is universal design?  How is it different from accessibility?
 - What is a client/server architecture?  Explain how it is applied to the internet.
 - Explain the process that takes place for your web browser to show you a page on the internet.
 - What are SMTP, POP, and IMAP used for?
 - What are HTTP and FTP?
 - What is TCP/IP?
 - Explain the relationship between IP addresses and domain names and URIs/URLs.


## Part 2 - HTML Overview
The end of the first chapter gives you an overview of HTML and has you create your first web page.  It is important that you actually sit at a computer and work through the example.  This not only ensures that you understand what you have read, it also ensures that you can put it into practice on your own computer.  If you have problems with getting, installing or using the software necessary for this course, it is important that you get these issues resolved right away.  You do not want to be struggling with the tools two or three weeks into the course.

As you work through the example, be very careful with your typing.  It is good *style* to use lowercase letters for your HTML tags, except for the `<!DOCTYPE html>`.  Make sure that you are correctly using the open and closing tags and placing quotes "" around your attributes.  I recommend that you use Brackets to work through this exercise and get into the habit of using Beautify to format your file.  Information on getting and installing Brackets as well as how to use it for this exercise is found in [Install, Configure and Use Brackets]({{ site.baseurl }}/morea/intro/ex-install-brackets.html).

It can also be helpful to save the HTML5 template as a gist on GitHub so that you can easily copy/paste that as needed no matter where you are or what computer you happen to be working on.

This is a gist that I have setup for the Basic HTML5 Template:
{% gist mbMosman/5785c6e9534e956b79d7 basicHTML5.html %}

<div class="well">
:dizzy: You can view and bookmark the above template gist on GitHub by clicking the link at the bottom of the <em>gist</em>.  If you are logged into GitHub, <em>star</em> the gist to bookmark it or <em>fork</em> the gist if you want to copy it to your account.  Gists are snippets of code you want to keep handy.  You can create you own from the + button next to your profile in the upper right.
</div>

### HTML Structure
It is important to understand that the structure of HTML is a tree or branching hierarchy - much like a family tree or a file system's folder structure.  The `<html>` tag is the root of this structure. Looking at our template it has two children - `<head>` and `<body>`.  These children are between (or inside) the opening and closing tags. You could also say they are *wrapped* (or surrounded) by the `<html>` tag.  Because they have the same parent tag, they are siblings.

Using the Chrome Browser Developer tools, we can view the structure of the HTML similar the the way you might see a file tree shown on your computer.  
<img src="{{ "/morea/intro/basic-html-tree1.png" | prepend:site.baseurl }}"
    alt="Image illustrating the tree structure of the template above. The html tag contains the head and body.">

By clicking the arrow next to a tag name, you can see what is inside of it.  
<img src="{{ "/morea/intro/basic-html-tree2.png" | prepend:site.baseurl }}"
    alt="Image illustrating the tree structure of the template above. The html tag contains the head and body.">


### Review Questions

- What is the purpose of the `<!DOCTYPE html>` tag?
- What is the difference between an opening tag and a closing tag?
- What are the two main sections of an HTML document?  What is each used for?
- What is an attribute?  Give an example of a tag that requires and attribute.
- What is the purpose of the `<title>` element? Can it be seen when viewing a page in the browser?
- What is a charset?  How do you tell the browser which charset it should use?
- What name should you use for the main or "home" page of a website?
- Walk through the HTML5 Template HTML and identify which tags are parents and which are children.  Recognize that some are both.  Identify tags which are siblings.
