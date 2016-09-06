---
title: "Bootstrap CSS"
published: true
morea_id: read-bstrp-css
morea_summary: "An introduction to some of the CSS provided in the Bootstrap framework."
morea_type: reading
morea_sort_order: 1
---

# {{ page.title }}

Most of what Bootstrap provides is a responsive, mobile first CSS framework to use when building your site.  The [Bootstrap CSS](http://getbootstrap.com/css/) page introduces the main CSS classes. Read through the Overview section for an introduction.  (We'll get into the Grid more after we setup our new site.)

## Containers
For Bootstrap to work properly, you need to first have a [Container](http://getbootstrap.com/css/#overview-container).  They offer two choices, a responsive, fixed width `container`  or a fluid - full display width `container-fluid`.  Both are *responsive*, but they respond in different ways.  The fixed width container does not fill the entire display on larger devices.  It has a max-width and is centered.  The fluid container will always fill the entire display.

Regardless of the option you choose, the container is generally setup either on a `div` by adding the appropriate style class: `<div class="container">` or `<div class="container-fluid">`.  However, it isn't necessary to use a `div`, you might also add the container style to your `main` element or any other block element that might be appropriate.

{% include alert.html type="warning"
   content="You can have more than one container on a page, but you should not nest one container inside of another."
%}

## Helpful Classes

### Typography
Bootstrap includes many CSS classes that are pre-built to apply single CSS properties to an element.  For example, you're learned how to use the `text-align` and `text-transform` CSS properties to align and modify text.  Bootstrap include style classes for each optional value of these properties: [Bootstrap Alignment Classes](http://getbootstrap.com/css/#type-alignment) & [Bootstrap Transformation Classes](http://getbootstrap.com/css/#type-transformation)

### Tables
Bootstrap also provides CSS classes to add a default style to [tables](http://getbootstrap.com/css/#type-transformation).  These classes can be combined to add individual features to the table styling.

For example, just adding the `table` style class to the table tag gives you a basic table with a border separating the rows.

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight html %}
    <table class="table">
      ...
    <table>
  {% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/basic-table.png" | prepend:site.baseurl }}" alt="A basic, borderless Bootstrap table">
</div>
</div>
</div>

If you add the `table-bordered` style, the table gets an outer border and column borders in addition to the border between rows found in the basic table.

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight html %}
    <table class="table table-bordered">
      ...
    <table>
  {% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/bordered-table.png" | prepend:site.baseurl }}" alt="A bordered Bootstrap table">
</div>
</div>
</div>

If you add the `table-striped` style, the table also gets alternate row striping.

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight html %}
    <table class="table table-bordered table-striped">
      ...
    <table>
  {% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/bordered-striped-table.png" | prepend:site.baseurl }}" alt="A bordered and row striped Bootstrap table">
</div>
</div>
</div>

All of the Bootstrap styles work in this additive fashion.  You combine multiple style classes on the same element to build the exact look you want for that element.  This makes their CSS library very flexible.

### Images
The Bootstrap CSS classes for [images](http://getbootstrap.com/css/#images) are also very handy.

Applying the `img-responsive` class will auto adjust your image sizes to fit in responsive containers, such as the Bootstrap Grid.  There are also classes to round the corners or put the image in a circle.


{% include alert.html type="tip"
   content="Bootstrap treats responsive images as block elements, so to center an image you would use the `.center-block` style, not the inline `.text-center` style."
%}

### More
There are many other built in CSS classes included in the Bootstrap library.  It's worth taking a look through the entire list just to be familiar with what they already have built for you.  

For example, when I first learned Bootstrap, I didn't have any need of multi-colored [alert](http://getbootstrap.com/components/#alerts) boxes, but since I've started making websites for my classes, calling out common errors, warnings and info tips in different colors has been quite handy. While I didn't remember the actual CSS class names, I recalled seeing them in the Bootstrap docs years later and looked them up.  Because I recalled seeing these, I avoided writing my own CSS to do the same thing.
