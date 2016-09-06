---
title: "Bootstrap Introduction"
published: true
morea_id: read-bstrp-intro
morea_summary: "An introduction to using the Bootstrap framework to design and develop web sites."
morea_type: reading
morea_sort_order: 1
---

# {{ page.title }}
[Bootstrap](http://getbootstrap.com/) is one of the most popular front end web framework libraries. It is a collection of commonly used, responsive CSS and JavaScript components that can be easily incorporated into any website.  This allows you to create a stylish new website quickly and easily.

The main resource for learning to work with [Bootstrap](http://getbootstrap.com/) is their website documentation.  You should read through the [Getting Started](http://getbootstrap.com/getting-started/) page and look at the [Example Pages](http://getbootstrap.com/getting-started/#examples).  We will use the Bootstrap [CSS](http://getbootstrap.com/css/), [Standard Components](http://getbootstrap.com/components/), and [JavaScript Components](http://getbootstrap.com/javascript/) for our projects.  

{% include alert.html type="note"
   content = "There are notes here to guide you, but you are expected to use the [Bootstrap](http://getbootstrap.com/) documentation as your main learning tool & reference.  This will give you practical experience learning to work with a new web framework, which is an important job skill."
%}

## Getting Started

### Bootstrap CDN
To get started, you need to get the [Bootstrap](http://getbootstrap.com/) files into your website.  It is generally considered a best practice to use a CDN to get the files. By using a CDN, the files needed may already be cached in the users browser from a previous site, which means they don't need to download the files again to view your site. This can reduce the overall load time for your site.

[Bootstrap CDN Information](http://getbootstrap.com/getting-started/#download-cdn)

When using the CDN links, make sure to place them in the correct spots in your HTML.  The stylesheet link tags go in your head.  You need to place them __*before*__ any of your own CSS so that you can override their styles if needed.  The JavaScript `<script>` tag goes at the end of your HTML content, just before you close the body tag.  

Note that they do not provide the required information here in the CDN information for adding the [jQuery](http://jquery.com/download/#using-jquery-with-a-cdn) script that the Bootstrap JS depends on.  They expect you will know how to do that.  See my template below for an example.

### Basic Template
Scroll down the getting started page and note the basic template that is provided. This is a great starting point for a new website. This might make a great Gist for your collection on GitHub.  (For mine, I've filled in the CDN information into the `<link>` and `<script>` tags.)

{% gist mbMosman/5785c6e9534e956b79d7 basicBootstrap.html %}

Looking at the template, you might note that it is an HTML5 document, and that it includes some basic setup for you.

- meta tags for the charset and viewport
- [HTML5 Shim](https://github.com/afarkas/html5shiv) & [Respond.js](https://github.com/scottjehl/Respond)
- setup for the Bootstrap CSS from the CDN
- setup for both [jQuery](https://jquery.com/) and the Bootstrap JavaScript files from a CDN


### Examples
The [Bootstrap Getting Started](http://getbootstrap.com/getting-started/) page contains a series of basic [Example Pages](http://getbootstrap.com/getting-started/#examples) that use [Bootstrap](http://getbootstrap.com/) to illustrate different options for page layout.  Take a look at some of these by clicking on the images/links to open the page in the browser and then viewing the page source and/or using the developer tools to inspect elements.  With the example page open, resize the browser window to the see how the responsive layout is adjusted.

We'll be looking at the different components in more detail, so you don't need to try and figure everything out right now.  Just explore a bit just to get a feel for what the framework can do.
