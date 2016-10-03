---
title: "Mobile First Design"
published: true
morea_id: read-mobile-first
morea_summary: "More information on Mobile First Design and how CSS using media queries can be structured."
morea_type: reading
morea_sort_order: 2

---
# {{ page.title }}

Mobile First is a design principle in which you intentionally make design decisions for mobile devices first. Until recently, the focus for web designers was the presentation of the web site on a computer monitor. As the spread of smart phones and mobile devices with internet access grew, people began to consider how websites might be viewed on these smaller devices, but that was historically secondary to the desktop view.

Today, the mobile phone is increasingly the main (or in some parts of the world only) way people access the internet. Some people do not have access to a desktop or laptop computer at all, but do have and use a smart phone to access the web.  This growing trend to use a mobile device as the primary path to access the internet is resulting in a shift to focus on designing <em>first</em> for mobile devices and then secondarily enhancing that design for larger displays.

In this session, we will begin to explore responsive design which allows a website to flex and change its display based on the available display size. We will first learn how to implement this type of responsive design using media queries. Later in the semester we will explore a web framework that provides a library of CSS styles to manage the responsive layout for us.

Responsive websites are only one way to design and target a site for mobile device users. It is also possible to build an independent web site that mobile users are directed to, based on information sent about the client that is included in the web page request. A mobile phone apps might also be developed for mobile users, replacing the need for them to view a website through the device's web browser.

Responsive sites have the advantage of keeping everything in one place. There is only one copy of the web site that adjusts to various device sizes.  However, designing a responsive site can pose challenges as well, and might result in design compromises that would not have to be made for a mobile only site or a mobile application.

### Media Query Design
In the textbook, the examples show desktop first development, where the CSS is first written for a desktop display and then altered using media queries for tablet and mobile.  An alternate approach is to design the CSS "mobile first" for the display on smaller devices and then use media queries to alter that display for larger devices.  Both approaches are supported by the CSS media queries, so be careful to look at the screen sizes that the media queries apply to.  Don't just assume that the CSS that is not inside a media query must be for the desktop display of a site.

Another alternate style for media queries is to organize everything by element, not device size.  So while the textbook shows many different rules inside one media query, the same design could be accomplished by having separate media queries for each selector.  This allows you to group all the CSS for a specific selector together.  

An example follows:

{% highlight css %}
footer { margin-left: 190px; }

@ media only screen and (max-width: 64em) {
   footer { margin-left: 0; }
}

@ media only screen and (max-width: 37.5em) {
   footer { font-size: 90% }
}

nav {
  float: left;
}

@ media only screen and (max-width: 64em) {
  nav {
    float: none;
  }
}
{% endhighlight %}
