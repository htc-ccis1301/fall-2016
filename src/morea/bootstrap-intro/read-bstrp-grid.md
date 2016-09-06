---
title: "Bootstrap Grid"
published: true
morea_id: read-bstrp-grid
morea_summary: "An introduction to using the Bootstrap grid framework to layout a responsive web site."
morea_type: reading
morea_sort_order: 1
---

# {{ page.title }}
Bootstrap's responsive [Grid System](http://getbootstrap.com/css/#grid) is one of its best features.  The grid allows you to layout your content in rows of up to 12 columns.  These columns can vary in size from 1 column width to 12 columns widths.  The grid utilizes CSS style classes to allow you to control the layout and positioning for various display sizes.

The key thing you need to know to use the grid is that you specify how many of the 12 columns you want your information to span.  Don't think of this as a table where each bit of data goes into one column and you have 12 of them.  These columns are meant to be spanned and their width will vary based on the display size.

Look at the demo [Grid Example Basics](http://getbootstrap.com/css/#grid-example-basic) and adjust the width of your display, noticing how the columns shift based on the display width.  

{% include alert.html type="warning"
   content = "__Pay attention to how the device sizes correspond to the [grid media queries](http://getbootstrap.com/css/#grid-media-queries).__
   A *small* device is tablet sized, while a phone is considered *extra small*. A *medium* device is a desktop, while a *large* device is a desktop with a larger display."
%}

## Mobile First
If you do not specify a specific `col-xs-*` class, then on a mobile device that column will use the full display width and the other columns will stack underneath.  If this is the behavior you want for a mobile (or xs) device, then you do not need to add a `col-xs-12` class for your column because that is the default.  

To alter this behavior as the display size gets larger, you add col classes for the devices where you do not want the column to take the full width of the display.  Remember these classes are additive, meaning you can (and almost always will) add many to one class attribute.

As you start to consider the larger displays, decide at what device size you want more than one column in a row.  Then add the appropriate class specifying the size and number of columns to span.  You can add more than one class to a column to change the display for different device sizes.  

Let's look at an example.  Put the code below into a template Bootstrap page so that you can experiment with it.  (You can also see this example and the examples below from GitHub [bootstrap-grid-ex](https://github.com/htc-ccis1301/bootstrap-grid-ex).)

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight html %}
  <div class="container">
    <div class="row">
      <div class="col-sm-6 col-md-4"> Col 1 </div>
      <div class="col-sm-6 col-md-4"> Col 2 </div>
      <div class="col-sm-6 col-md-4"> Col 3 </div>
      <div class="col-sm-6 col-md-4"> Col 1 </div>
      <div class="col-sm-6 col-md-4"> Col 2 </div>
      <div class="col-sm-6 col-md-4"> Col 3 </div>
    </div>
  </div>
  {% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/ex-grid-shoelace.png" | prepend:site.baseurl }}" alt="Layout of this example in Shoelace.">
</div>
</div>
</div>

In this example, we see the following:

 - on a mobile phone: all 6 columns stack, each taking up the full display width
 - on a tablet: there are __three rows__ each with __two columns__ side by side
 - on a desktop: there are __two rows__ each with __three columns__ side by side


## Adding Rows
When the columns are not added into rows, the columns can flow from row to row as needed to fill the width of the display.  This is often, but not always a desirable behavior.  To keep column content in distinct rows, you can add div tags with the `row` class.

Notice how the code below behaves differently now that the columns are separated into two rows.

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight html %}
  <div class="container">
    <div class="row">
      <div class="col-sm-6 col-md-4"> Col 1 </div>
      <div class="col-sm-6 col-md-4"> Col 2 </div>
      <div class="col-sm-6 col-md-4"> Col 3 </div>
    </div>
    <div class="row">
      <div class="col-sm-6 col-md-4"> Col 1 </div>
      <div class="col-sm-6 col-md-4"> Col 2 </div>
      <div class="col-sm-6 col-md-4"> Col 3 </div>
    </div>
  </div>
  {% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/ex-grid-rows-shoelace.png" | prepend:site.baseurl }}" alt="Layout of this example in Shoelace.">
</div>
</div>
</div>


In this example, with two separate rows:

- on a mobile phone: all 6 columns stack, with each taking up the full display width
- on a tablet: there are __four rows__, the first and third with __two columns__ side by side, the second and fourth with __one column__ at half the display width
- on a desktop: I would see __two rows__ each with __three columns__ side by side

## Column Ordering
The last thing I want to call out about the table is one of the most awesome features, modifying the [column ordering](http://getbootstrap.com/css/#grid-column-ordering).  The push and pull modifier classes can be used to shuffle columns around for different display sizes.  This is great when focusing on not just shrinking content for mobile, but ensuring that it is displayed appropriately based on importance.

For example, let's imagine that I've got a main paragraph of crucial information that I obviously want right in front of my mobile users.  But I'd also like to have two smaller ads or images (less important information) follow this information stacked on mobile, but on tablet where there is a little more width I want them to follow side-by-side in one row.  Then when there is even more width on a desktop, I want to have a 3-column layout where these ads/images flank the main content one on each side.  

I really don't want to try to write those media queries myself, but with Bootstrap this is simple to set up.  Check out the demo code below and make sure that you understand how it is working.

{% highlight html %}
<div class="container">
  <div class="row">
    <div class="col-sm-12 col-md-push-3 col-md-6">
      <b>Crucial information</b>
    </div>
    <div class="col-sm-6 col-md-pull-6 col-md-3">
      Not important 1
    </div>
    <div class="col-sm-6 col-md-3">
      Not important 2
    </div>
  </div>
</div>
{% endhighlight %}

## Visual Tool
If you need some help visualizing your Grid Layouts, you can use a visualizer like [Shoelace.io](http://shoelace.io/) to help you visualize your grid on different sized devices and write the HTML/CSS outline for you. Once you become more comfortable with how the grid works, this is probably more effort than it is worth, but many students have commented that tools like this help them to *learn* how the grid works.

{% include img-small.html
    url="/morea/bootstrap-intro/images/shoelace-visualizer.png"
    alt="A screenshot of using Shoelace to visualize a Bootstrap grid layout."
%}
