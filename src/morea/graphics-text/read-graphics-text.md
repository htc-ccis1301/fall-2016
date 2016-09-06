---
title: "Graphics & Text Styling"
published: true
morea_id: read-graphics-text
morea_summary: "Add interest to your web pages using graphics and text styling."
morea_type: reading
morea_sort_order: 1
morea_labels:
 - texbook
---

# {{ page.title }}
Read Chapter 5 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers images and text styling.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## Overview
Chapter 5 expands your HTML & CSS skills into fonts and images to make your web pages more interesting.  We will learn to add images to our page using HTML & CSS, and use CSS to make the text on our pages more visually appealing.  


## Images
Let's start with a bit of background information on how images are created, stored and displayed.

{%  include youtube-small.html  id="15aqFQQVBWU"
    caption="Thanks to [Code.org](https://code.org) for sharing the video!" %}


### Image File Types
As you read through the introductory text, pay attention the various image file types, what each file type is best used for, and what they can and cannot do. Understanding this is very helpful when designing webpages and getting image files from others.  For example, if you need an icon that will look good on different colored backgrounds, it is helpful to have an image with a transparency layer.  So a GIF or PNG would be appropriate, but not a JPEG.  

### HTML Image Element
The image element, the `<img>` tag, is the main method of including graphics on your web site.  To give images a fixed size, use the `height` and `width` attributes, but be careful not to make visitors download a large photo quality image if you are only showing it at 300 x 300.  You should always edit your images to reflect a reasonable size and image quality for their purpose.

Providing multiple images in different sizes and qualities is a good way to support this.  If you have an image gallery that displays thumbnails and users can click on an image to go to a larger view, make separate images for each.  The thumbnails should be thumbnail sized and lower quality for faster download.  Only if a visitor wants to see the larger more detailed image do they need to download the larger file.

It is easy to make an image a link by wrapping it with an anchor tag.  Again, if you are using these images for navigation, be sure to consider alternative options for accessibility. Use the `alt` attribute to hold the text displayed in the image, and consider adding a set of nav items to the footer where the will be unobtrusive for most users, but provide critical information for screen readers.

### Background Images
It is important to remember that background images should only be used for decorative elements on your page.  Any images with *meaning* should be added using the `<img>` tag with `alt` text.

Background images can be applied to any HTML element using CSS.  For example, you might configure a background image for the body tag to make the entire web page background look like a piece of aged paper.  You might also put just a small image in the background in a particular position, like the bottom right.  

Key properties are:

- background-image
- background-repeat
- background-position


{% include alert.html type="warning"
   content="__Remember to use relative paths for your images.__  
   Images are often kept in a folder just for images. See the note at the bottom of page 149 in your textbook for examples of how to support this."
%}


### Fav Icon & Image Maps
The end of Chapter 5 discusses the favorites icon, which is shown in the browser window or tab next to the title, and image maps, which are images with clickable locations in the image.

Setting up a favorites icon for your web page can help it to stand out.  If you are like me, and often have 10 or more tabs open, then you'll appreciate those that have a little icon indicating what page it is for.  The favorites icon is configured with the `<link>` tag.  

{% highlight html %}
<link rel="icon" href="myFav.ico" type="image/x-icon">
{% endhighlight %}

The information about image maps is good to be aware of, however we will not use or focus on image maps in this course.  When using image maps for a site, it is important to ensure that their use and purpose is obvious to website visitors.  An image with multiple links hidden in it might seem cool, but if people don't realize they can click on different parts of the image, they may be stuck on your home page.  Accessibility is also something to pay special attention to with image maps, especially if they are providing your sites main navigation.

## Review Questions

 - Which image file types support transparency?  Which types support animation?
 - What attribute is required on the image element for accessibility?
 - When using images for navigation, what alternatives are recommended to support accessibility?
 - How do you add a background image to an element when using CSS?
 - How would you repeat a background image down the left side of an element?  Across the top?
 - Can you add more than one background image for the same element?  
 - Explain the term *progressive enhancement*.


## Text Styling

### Fonts
One of the most common things that you'll do to style a website is choose specific fonts to match the look that is desired for the page.  Remember that most fonts fall into 2 main categories: serif and sans-serif. Serif fonts have little marks at the tips of the letters and tend to look more formal and are often used for headings.  Sans-serif fonts tend to be used when a lot of text content is displayed for reading.  Sans-serif content is generally considered easier to read.

There are also monospace, cursive and fantasy font categories, but those are less commonly used.  They are also typically used only for small sections of text, such as headings or perhaps code snippets in an IT related page.  [CSS Font Stack](http://www.cssfontstack.com/) is a great common font reference.  It will show you font availability for different operating systems and provides good fall back options for when a font is unavailable.

{% include alert.html type="danger"
   content="When adding `font-family` CSS to your web pages, I will expect that you have specified either a proper web safe font stack from [CSS Font Stack](http://www.cssfontstack.com/) or a [Web Font](http://www.cssfontstack.com/Web-Fonts) with appropriate fall-back fonts."
%}

#### Web Safe Fonts
Most websites rely on fonts that are already installed on the client computers.  However, there is no common set of fonts available on all computers; the fonts available vary based on the operating system of the computer.  To aid with web site design, lists of __web safe fonts__ have been created that include fonts that are pre-installed by *many* operating systems. These lists group those fonts into *font stacks* which are a set of fonts that look similar and cover the major operating systems.


#### Web Fonts
Unlike web safe fonts, __web fonts__ are not pre-installed on the user's system. These fonts are downloaded by the browser from the internet when rendering the webpage.  Because they require a download, these fonts will slow down the initial display of your website.  These fonts are also not supported in older browsers which do not support CSS3.  To avoid issues with older browsers, the best practice is to use a web safe font stack with a web font added as the first font in the list. If a browser is unable to use the web font it will fall back on the web safe fonts in the stack.

#### Tools Demo
A quick video introducing you to using both [CSS Font Stack](http://www.cssfontstack.com/) & [Lorem ipsum](http://www.lipsum.com/) - a site to get fancy dummy text.

{%  include youtube-small.html  id="7gz4_ZWFVFo" %}

### Additional CSS properties for text
In addition to using CSS to determine which font to use, you can also configure the size, weight, style, alignment, and even convert to upper or lowercase all using CSS.  Some important properties to remember are:

- font-family
- font-size
- font-weight
- font-style
- text-align
- text-decoration
- text-transform

Pay attention to the various ways to set the font size. While older websites tend to set font sizes in pixels, the trend toward responsive design has put more focus on relative font sizes using either em or percentages. Using this type of sizing also helps when visitors zoom in or out on the web page using the browser.  (Try doing either CTR + or - (or CMD + or - on a Mac) when looking at a web page.)

### List Markers
It is also fairly common to use images for list markers or bullets. (Custom fonts, which we will discuss later are also frequently used for this.)   These are configured using the `list-style-image` property.

Sometimes we don't want to see the markers for our list.  For example if we have a list of `nav` links.  To disable the list markers (bullets or numbers), sets `list-style-type: none`.


## Review Questions

 - What is the difference between a serif and sans-serif font?
 - What is meant by a font stack?
 - What is the difference between web safe fonts and web fonts?
 - What are the CSS properties used to bold, underline, and italicize text?
 - How do you center text using CSS?
 - How do you change the marker used in an unordered list?
 - How do you change an ordered list to use Roman numerals?
