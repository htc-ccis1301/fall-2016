---
title: "CSS Box Model & More"
published: true
morea_id: read-more-css
morea_summary: "An introduction to the CSS box model and additional CSS features to add color to your pages."
morea_type: reading
morea_sort_order: 1
---

# {{ page.title }}
Read Chapter 6 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers the CSS box model and additional features for adding color.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## Overview
Chapter 6 introduces the CSS box model which is used to size and add spacing around various elements on the page. The addition of margins, padding and borders can make a huge difference to the look of your page, allowing you to group and space content for better clarity and presentation.  This chapter also covers various methods for adding color and transparencies with CSS.   

{% include alert.html type="note" content="Understanding the CSS box model is *very* important to making web pages look good.  Margins and padding are perhaps the two most commonly used styles.  Make sure that you understand the difference between the two, and when using each is more appropriate." %}


## Box Model
The CSS box model shows an element's size, padding, border, and margin.  Remember that the browser developer tools will illustrate the box model for you for a selected element.  In the image below, you can see the element's size (in the blue area in the center), the padding (the inner green area), the border (the yellow area separating the padding and margin), and the margin (the orange outer area).

{% include img-small.html url="/morea/more-css/images/css-box-model-ex.png"  alt="Image of the CSS box model diagram from the Chrome developer tools." %}

Remember that padding picks up the element's background color, while the margin is transparent and thus shows the color of the parent or containing element.

Key properties:
- width and height
- margin (note both the shorthand and individual properties)
- padding (note both the shorthand and individual properties)
- border (note both the shorthand and individual properties)

Understanding the box model and how it affects the layout of HTML elements is important to the layout of your web site.  It controls the size and spacing of elements. Correct use of the opaque (padding) and transparent (margin) can make a big difference in how elements appear on the page.

## More CSS
These are all topics you should be aware of, but may not want or need to memorize.  They're easy to look up if you need them, and aren't used as frequently as others.

Keep in mind that this is all relatively new stuff and you'll want to pay attention to browser support for these features.  Ensure that an acceptable fall-back is in place when these properties are unsupported.

### Rounded Corners
Rounded corners were a *thing* a few years ago, but the trend more recently has leaned back towards square.  The current *buzz* style varies year-by-year and individual style varies site-by-site. Rounded corners used to be a more difficult thing to achieve.  You needed to actual set them up with images for the corners, with the right background color and position.  It was tricky and made sites stand out a bit more if they could pull it off.  (If you bump into this old-style stuff, be sure to speak up about the newer, better way.)

Today it's simple to set up in minutes using CSS.  Perhaps that's why it's less of a trend?  Who knows.  But if you like the look and it works for your site, use it.  If you (or your customer) prefer the sharp, square corners, use those. Worry more about what works for your site's style than the latest *buzz* trends.


### Box and Text Shadow
A good application of these styles can really make a website *pop* or stand out.  However don't get too carried away with them.  If you start applying it to everything, you just might get dizzy looking at your page.  If everything starts floating off the screen, it can get a little disconcerting.  Use it sparingly for the best effect.


### Opacity & Colors
Using semi-transparent `<div>` or headings over a photographic background can make for a really lovely look for a web page, especially one that might be travel or art focused.  Just like with the shadows though, this is probably best applied in smaller amounts.  Large areas of text for example will be much harder to read if there's an image in the background. You can achieve this semi-transparent look by using either the opacity property or the background and color properties with RGBA or HSLA colors.  


### Gradients
Being able to configure gradients in CSS is awesome!  This is another one of those things that we used to do using images.  Applying gradients through CSS is much more flexible.  The radial gradient provides a nice spot-light effect that is pretty neat, while the linear gradient makes for a simple but interesting background.  Often we will use a gradient background for the body, and place a solid white (or light-colored) content area over top of it.  That light, solid color makes it easier to read any text.  


## Review Questions

 - Explain the CSS Box Model.
 - What is the difference between margin and padding?
 - Does the margin show the background-color of the property it is applied to?  Does the padding?
 - What options are available when configuring a border for an element?
 - How do you use margins to center block content?
 - How do you make rounded corners for the border of an element?  Is this supported on all browsers?
 - How do you set up a text shadow for an element?  
 - Explain the five properties that can be used to set up a box shadow.  Are all required?
 - Explain the use of the background-clip, background-origin, and background-size properties.
 - Discuss how you might use the opacity property on a web page.
 - How are RGBA colors different than specifying a color with a hex code?
 - How are HSLA colors different than specifying a color with a hex code?
 - What CSS property is used to make a background gradient?
 - Why should you provide a fall-back background-color when using a CSS gradient?
