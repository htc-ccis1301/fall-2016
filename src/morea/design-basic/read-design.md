---
title: "Intro to Web Design"
published: true
morea_id: read-design
morea_summary: "An introduction to the basics of web design."
morea_type: reading
morea_sort_order: 1
morea_labels:
 - texbook
---
# {{ page.title }}
Read Chapter 3 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers page layout with HTML & CSS.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## Design Principles
This is a high-level overview of the key principles that I expect you will recognize and understand from Chapter 3 of your textbook.  The information on colors and wireframes is pulled out into separate reading pages with additional information included.

### Target Audience
What works for one site, may not work for another.  The reason behind that is often that the target audience and/or purpose of the site are different.  A site geared towards children is likely to be more colorful and bright, while one focused on adults is likely to be a bit more monochrome and subdued. An information heavy site like wikipedia will focus more on text, while a site advertising a movie is going to focus more on media, graphics and sound.

Understanding the target audience and purpose also leads to some technical considerations.  If you compare your average computer across age groups and demographics, the device they use (home computer, tablet, phone), the size of their display, web browser, and the version of that browser will vary.  I am fairly certain that they have never looked at a website on their phone. For that matter, I'm not even sure they have a phone that views websites...  My 3 and 5 year old nieces on the other hand are already quite adept at using their parents mobile phone apps.  As an IT professional, I wonder how I'd function without two big widescreen displays, while my father-in-law is more than content with his old square 15 inch monitor.

Keep in mind that a discussion on target audience can have wide-ranging implications.


### Organization & Presentation
Web site maps generally fall into two groups, hierarchical and linear.  Larger websites - like an online storefront - may incorporate both.  (Products are hierarchical, while checkout is linear.)  Rare sites are set up more randomly, but these are generally not commercial sites and may be more focused on exploration and discovery - perhaps through a social network, game or story telling.

A web site's organization has a huge affect on usability.  There is a generally accepted *3-click* rule that says you shouldn't have to click more than 3 times to get to what you want. Likewise, they say that your average person can only keep about 3 or 4 items or chunks of information in memory at a time.  Keep in mind the 4 principles of visual design - proximity, contrast, repetition, and alignment.  


### Text and Multimedia
Keep text on the web to the minimum needed to communicate the idea, concept or information needed by the site.  When using larger amounts of text, use an easy to read, sans-serif, font such as Arial and keep the line length to around 50-80 characters per line.  Left-align paragraphs of text.  Center-alignment can make image captions, headings or small bits of text (1-3 lines) stand out, but it is hard to read large amounts of text formatted this way.  

Use multimedia - images, sound, and video - judiciously.  Don't add things just because you can.  Ensure they are relevant, important, and add benefit to your site.  Ensure that any meaning is communicated in other ways - a text script for a video, alternate text for images and sound files.  Even for those who are not prevented from seeing or hearing these things due to disabilities, providing alternatives is friendly to those on mobile devices as well as those in a quiet setting.

And *please* don't have any website you make just randomly start blaring music or videos.  This is one area that it is safer to "opt-in" versus having to figure out how to stop the sound when you don't want it. This is particularly true for business or informational sites.  The quickest way to not have me come to buy your product or visit your restaurant is to have it start playing music when I sneak a peek at work!

We will talk more about images and multimedia in later chapters as well.


### Above the Fold
The term *above the fold* comes from newspapers, where what you see "above the fold" is what will sell the paper, or catch your eye as you look at a stack of papers.  The concept though is just as applicable to the web.  If you have a lot of content, what the visitor sees when they first land on your page is important.  It *sells* them on staying on your site.    

What was "above the fold" was historically more important than it is now.  This is due to both responsive design which can move elements to ensure they are seen, and the popularity of mobile devices where scrolling is assumed. It is now common for the *above the fold* content to focus on eye-catching expression more than communication of all the key and crucial information.

A common site design today uses scrolling to have different *pages* all on one page.  A welcome with minimal information is visible when you land on the site, and as you scroll down the page, you are presented with screen size *chunks* of content.  In some cases this is done with the scrollbar visible, and you just see nicely framed content that matches your page size.  In other examples, the content of the page itself changes with scrolling (this requires JavaScript), and the content appears to flip, just like turning a page in a book.

There are many examples of this.  Let's look at one, the welcome page for [Tumblr](https://www.tumblr.com/)

Notice the typical banner and navigation are missing from the top of the page.

{% include img-small.html
    url="/morea/design-basic/images/design-tumblr1.png"
    alt="Screen capture of the Tumblr welcome page."
%}

Scrolling down is like flipping a page.  Notice the dots down the left side that indicate where you are, and can be clicked to move forward and back.  

{% include img-small.html
    url="/morea/design-basic/images/design-tumblr2.png"
    alt="Screen capture of the next Tumblr page, obtained by scrolling down."
%}


### Mobile & Responsive Design
There are a few different approaches to addressing mobile design.  Initially, sites provided a separate mobile site that was hosted at a different URL. Those accessing the site on a mobile device were redirected to the mobile site. While this approach allows a very tailored mobile view, it also involves a lot of overhead to create and maintain two separate versions of your web site.

Today a website that is *responsive* to your display is a much more common trend.  It allows you to main a single version of your site while at the same time allowing you to provide a tailored experience for the viewer.  Creating a site like this requires a different design and implementation approach, and perhaps even more work up front, but is easier to maintain and support going forward.  

Key considerations for mobile include:

- bandwidth and load time
- page layout due to the smaller view area
- touch controls and click area
- color, text, and contrast may vary significantly by device

Mobile designs tend to feature a single column layout, and limit or hide non-essential information, graphics, and media.  

It is also important to remember that responsive design addresses more than just mobile phones.  It also addresses tablet which come in various sizes and may be rotated for portrait or landscape view, as well as older square monitors and super big widescreen displays.  A responsive website will look different - but good - on all of these devices.

We will explore responsive design more in the next module.


## Design Best Practices
There is a web design best practices checklist in your textbook.  In the 2nd edition, it is pages 94-95, and in the 3rd edition, it is pages 102-103.  This is a handy checklist to review as you are working on a site's design.  It is also nice to use to evaluate your site are working on it.  
