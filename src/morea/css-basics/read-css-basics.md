---
title: "Basic CSS"
published: true
morea_id: read-css-basics
morea_summary: "An introduction to styling web page content using Cascading Style Sheets (CSS)."
morea_type: reading
morea_sort_order: 1
morea_labels:
 - textbook
---

# {{ page.title }}
Read Chapter 4 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers an introduction to CSS.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## Introduction to CSS
Chapter 4 is dedicated to introducing Cascading Style Sheets (CSS).  We will learn what CSS is, what it is used for, how it works, and how to apply it on our web pages to make them look more attractive.  

<div class="alert alert-info" role="alert">
:notebook: This is a very, <em>very</em>, important chapter.  Don't skim or just glance over any of it.  Pay close attention to how the CSS is used and applied, and how the *cascade* rules work.  
</div>

## What is CSS
CSS allows us to apply different fonts and font styles, colors, and layout to our web pages. This can cause the exact same HTML markup to be rendered (or displayed) in the browser in many different ways.  This is a very powerful feature!

To see how powerful, let's look at some examples from the [CSS Zen Garden](http://www.csszengarden.com/) website.  All four images below represent the exact same HTML, just with different CSS applied.

<div class="row" style="margin: 15px;">
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
    <a href="http://www.csszengarden.com/">
    <img class="img-responsive" src="{{ "/morea/css-basics/zen-garden/basic-css-zengarden-main.png" | prepend:site.baseurl }}"
        alt="A light green watercolor view of the CSS Zen Garden website.">  
    </a>
</div>
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
<a href="http://www.csszengarden.com/216/">
<img class="img-responsive" src="{{ "/morea/css-basics/zen-garden/basic-css-zengarden-fk.png" | prepend:site.baseurl }}"
    alt="A sunset colored vintage look for the CSS Zen Garden website.">  
</a>
</div>
</div><div class="row" style="margin: 15px;">
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
<a href="http://www.csszengarden.com/221/">
<img class="img-responsive" src="{{ "/morea/css-basics/zen-garden/basic-css-zengarden-midcent.png" | prepend:site.baseurl }}"
    alt="A bold retro style for the CSS Zen Garden website.">  
</a>
</div>
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
<a href="http://www.csszengarden.com/215/">
<img class="img-responsive" src="{{ "/morea/css-basics/zen-garden/basic-css-zengarden-robot.png" | prepend:site.baseurl }}"
    alt="A light colored style of the CSS Zen Garden website featuring a robot.">  
</a>
</div>
</div>

This illustrates some very dramatic formatting and layout changes that can be applied through the use of CSS.  It is almost unbelievable to think that all of this pages use the exact same HTML! In addition to formatting and layout, CSS also supports gradients, transparencies, animations and transitions.  

You'll get the hang of HTML in no time, but becoming a true master of CSS will take much longer.  There is a lot to learn; so don't let that discourage you.


## Style Declaration
A stylesheet is made up of one or more rules, and each rule has two parts - a selector and declaration.  The selector is placed before the curly braces { }, and the declaration is placed inside.  The declaration is make up of one or more property/value pairs.

Some examples:
{% highlight css %}
body {
    background-color: blue;
    color: white;
}

h1 { color: lime; }

div { background-color: lightYellow;  color: red; }
{% endhighlight %}

In the examples above, all of the selectors should be recognizable as HTML tag names.  Selectors can also be class or id selectors.  You can also combine one or more to make a descendant selector.


|  `#content`   | &nbsp;&nbsp;  an ID selector  &nbsp;&nbsp; |  &nbsp;&nbsp; selects the item with the `id="content"`
|  `.myClass`   | &nbsp;&nbsp;  a class selector &nbsp;&nbsp; | &nbsp;&nbsp; selects all elements that have `class="myClass"`
| `#content p`  | &nbsp;&nbsp;  a descendant selector &nbsp;&nbsp; | &nbsp;&nbsp; selects all p elements *inside* the element with `id="content"`


## The Span Element
Just like `<div>` tags are used all over the place to identify and style *blocks* of content,  `<span>` tags are used to identify and style *inline* content.

In the simplest terms, a block of content is content that uses the entire width of the browser display with a space or break before and after it. Inline content *flows* in a line, usually a line of text, but it may be a line of images, or buttons, or anything.  

There will only be one block in a row of content, there may be many pieces of inline content in a row and as they overflow one row, they will wrap to the next.


## Validation
The W3C provides an online validation service for CSS similar to the one that it provides for HTML - [W3C CSS Validator](http://jigsaw.w3.org/css-validator/).  Links to both validation sites are included in the Links and Resources in the sidebar.

They work basically the same way, however they are both specific in regards to the type of files that they validate.  The CSS Validator will not validate HTML and likewise the HTML validator will not validate CSS.  This may seem obvious now, but things can get blurry at the end of a long day.  I have reminded people of this numerous times.

Validation errors in your CSS file will also result in points being deducted from your assignment grades.  However, they also tend to result more frequently in the page not appearing correctly, and thus are more often caught before being submitted.  If you are not getting the results that you expect from your CSS, run in through the validator.  It just might save you a lot of trial and error in trying to resolve the problem.


## Review Questions

 - Where can you put styles to override those in an external style sheet?
 - What is the difference between an embedded style and an inline style?
 - Explain the syntax of a CSS rule.
 - What does the CSS color property alter?
 - What is the HTML `style` attribute used for?
 - How do you add embedded CSS to a web page?
 - How do you add an external style sheet to a web page?
 - Name four types of CSS selectors.
 - What is the HTML `span` element used for?  In what ways is it similar to a `div` element?  How is it different?
 - What effect does the CSS applied to a parent element have on its children?  
 - How do we validate our CSS?  How is this process similar to the process for validating HTML?  How is it different?
