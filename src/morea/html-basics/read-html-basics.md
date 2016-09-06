---
title: "Basic HTML"
published: true
morea_id: read-html-basics
morea_summary: "An introduction to basic HTML tags for outlining content and creating links."
morea_type: reading
morea_sort_order: 2
morea_labels:
 - textbook
---

# {{ page.title }}
Read Chapter 2 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers an introduction to some common HTML tags.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## New HTML Tags
Much of Chapter 2 in the textbook is devoted to introducing new HTML tags.  The tags that I recommend that you focus on are those for:

- headings
- paragraphs
- line break
- the phrase elements for strong, emphasis, & small
- ordered & unordered lists
- structural elements for div, header, nav, main and footer
- anchor tags (hyperlinks)

An important note on the line break tag:   
You should not use this to break paragraph text so that it matches the images shown in the textbook or website examples.  Paragraph text is intended to wrap naturally at the edge of the browser, so depending on the size of your window, that text will wrap in a different spot. This is expected behavior and you should not alter it without good reason - for example, breaking lines of an address.

### Semantic HTML
I'm a little disappointed by some of the things that are *taught* by the examples for the phrase elements and the description list.  Remember that it is our goal to write *__semantic__* HTML.  We should use elements for their intended purpose, not because their default display is a particular way.  Semantic HTML greatly benefits accessibility.

You should use tags like `<b>` or `<strong>` and `<i>` or `<em>` and `<small>` only when there is a semantic reason to do so, not just a visual preference for the text to appear that way. They use these throughout the chapter and end of chapter case study they show these elements being used for *display* purposes and then re-teach you to correctly use CSS for this in Chapter 4.  I encourage you not to develop this habit only to break it.

What is the difference you might ask?  A bad example (in my opinion) of using `<small>` and `<i>` would be the footer text on a web page such as that shown in Hands on Practice 2.11.  This should be done using CSS, and you'll learn to do exactly this in Chapter 4.

A good example of using `<em>`, which is more semantic than `<i>`, would be text like:
<div class="row" style="margin: 20px">
  <div class="col-sm-6">
    <h4>HTML</h4>
    It is &lt;em&gt;really&lt;/em&gt; important that you learn to write semantic HTML.
  </div><div class="col-sm-6">
    <h4>Display</h4>
    It is <em>really</em> important that you learn to write semantic HTML.
  </div>
</div>

A good example of using `<small>` might be for a sub-title of a book or article.  
<div class="row" style="margin: 20px">
  <div class="col-sm-6">
    <h4>HTML</h4>
    Kendo &lt;small&gt;The definitive guide&lt;small&gt;
    <br>&lt;br&gt; by Hiroshi Ozawa and Tamiko Yamaguchi  
  </div><div class="col-sm-6">
    <h4>Display</h4>
    Kendo <small>The definitive guide</small>
    <br> by Hiroshi Ozawa and Tamiko Yamaguchi
  </div>
</div>

Likewise you should use the description list for just that, terms and descriptions.  The example that is initially presented in Hands on Practice 2.8 is a great example.  On the other hand, the example in Hands on Practice 2.14, #3 (Figure 2.24) where the description list is shown more for business services becomes more questionable.  I can see an argument to be made that it *is* describing those services. However, it's also likely that page would be expanded later to include more information on those services, and as that content grows subheadings with paragraphs is probably more appropriate.  

This illustrates that there are differences in opinion on what *proper* semantic use of these tags might be.  I suspect that here, the description list is used more to have an excuse to use it than because it is a good example of its use.

## Special Entity Characters
The special entity characters are discussed on pages 44 & 45 of the textbook.

The copyright, ampersand, non-breaking space, the emdash (long dash), and the greater than and less than symbols are used fairly often.

### Non-breaking Space
The non-breaking space is not explained well in your text.  While it can be used with a line break to indent text, this is really not encouraged.  The actual intent of the tag is to avoid having line wrapping in the browser break words in a way that might be confusing.  For example if you were including measurements on a page, it might be confusing to have the number and the unit of measure split, for example "10 cm".  You can avoid this by using a non-breaking space between the 10 and the cm like this:  

<div class="row"  style="margin: 20px">
  <div class="col-sm-6">
    <h4>HTML</h4>
    &lt;p&gt;The sample was found to be 10&amp;nbsp;cm in length.&lt;/p&gt;  
  </div><div class="col-sm-6">
    <h4>Display</h4>
    <p>The sample was found to be 10&nbsp;cm in length.</p>
  </div>
</div>

When doing this, it is important __not__ to also include a normal space, as that would allow the line to break or wrap on that space.

Instead of using non-breaking spaces for formatting or indenting text, a better option would be to use the `<pre>` tag, which is for pre-formatted text, or to use CSS.  We'll look at CSS later, but here is an example of how you might use the `<pre>` tag.

<div class="row"  style="margin: 20px">
  <div class="col-sm-6">
    <h4>HTML</h4>
    &lt;pre&gt;
<br>def isGreen(Shape s):
<br>&nbsp;&nbsp;if s.getColor() == "green":
<br>&nbsp;&nbsp;&nbsp;&nbsp;return true
<br>&nbsp;&nbsp;else
<br>&nbsp;&nbsp;&nbsp;&nbsp;return false
<br>&lt;/pre&gt;  
  </div><div class="col-sm-6">
    <h4>Display</h4>
    <pre>
def isGreen(Shape s):
  if s.getColor() == "green":
    return true
  else
    return false
    </pre>
  </div>
</div>

## Validation
One of the most important topics in this chapter is the information on HTML Syntax Validation (pages 46-47).  Every assignment that you turn in going forward will be validated as part of grading that assignment.  Any validation error on your pages will result in a lower grade on the assignment.  For project assignments, you will lose an entire letter grade for a single validation error.  

Learning how to validate your page and fix any errors is critical to your success in this course.

You should use the [W3C HTML Validator Nu](https://html5.validator.nu/) to validate your pages.  It is more up to date than the old validator used in the textbook.  The display is a bit different, but the options and output are essentially the same.

Additional information on validation can be found on the [W3C website](https://www.w3.org/wiki/Validating_your_HTML).

## Review Questions

 - How many levels of headings does HTML support?  
 - Which heading is larger by default, h1 or h4?
 - What tag is used to split text into multiple lines?
 - How should you code the copyright symbol on a page?
 - How could you ensure that a phrase like "10 PM" would not be broken by the browser's line wrapping such that 10 appeared on one line and PM on the next?  
 - How would you describe semantic HTML?
 - Which of the structural tags can only occur once on a page?
 - What is the difference between a relative hyperlink and an absolute hyperlink?
 - What is a relative hyperlink relative to?
 - How do you make a link to send an email?
 - Where do you go to validate your web pages?  
