---
title: "Bootstrap Componenets"
published: true
morea_id: read-bstrp-cmp
morea_summary: "An introduction to some of the user interface (UI) components provided in the Bootstrap framework."
morea_type: reading
morea_sort_order: 1
---

# {{ page.title }}

Bootstrap includes many helpful [components](http://getbootstrap.com/components/) to aid in the creation of a nice user interface for your page.  We'll discuss a few below.  This should be enough for you to get a feel for how to read the docs and use the examples.  This should help you to gain confidence that you can then read about and use the other components on the Bootstrap site on your own.

{% include alert.html type="tip"
   content="When looking at the examples in the docs, remember to resize your display to view their responsive behavior."
%}

## Navigation & Navbar
There are several different options for setting up and organizing a site's links and navigation.  The most commonly used is a navbar that sits along the top of the web page.  

### Navbar Examples
The Bootstrap Getting Started page examples illustrate some options for using the bootstrap navbar.

- [Regular Navbar](http://getbootstrap.com/examples/navbar/) - use links for positioning options: default, static and fixed
- [Carousel using Inverted Navbar](http://getbootstrap.com/examples/carousel/) with default positioning - inverted refers to the flipped colors (darker background) vs the default
- [Jumbotron using Inverted Navbar](http://getbootstrap.com/examples/jumbotron/) - inverted navbar with fixed positioning and a form

If you view the source for these pages and look at the navbar, you might notice much of the differences in appearance and behavior come from which style classes are applied.  Want the navbar to be fixed at the top, then apply the `navbar-fixed-top` class.  Want to swap (invert) colors, then apply the `navbar-inverse` class.  As we learned earlier, you can add multiple style classes to the same element to build a custom look and behavior.


### Navbar Functionality
There is a lot packed into Bootstrap's [Default Navbar Example](http://getbootstrap.com/components/#navbar).  This is meant to show a lot of variety in what you can do with the navbar, but all those options will not make sense for every site.  You should feel free to add and remove items as needed for your site.

Let's look at a simpler example. Note the HTML comments with notes on individual pieces.

{% highlight html %}
<!-- This makes a default light navbar -->
<nav class="navbar navbar-default">

  <!-- The container-fluid makes the nav adjust to always be full width -->
  <div class="container-fluid">

    <!-- Brand and toggle are grouped as navbar-header.  Only this is initially shown on mobile -->
    <div class="navbar-header">

      <!-- Note this button has 3 bars in it, often called hamburger nav. -->
      <!-- This is shown when the navbar is collapsed. -->
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse"
              data-target="#bs-ex-nav-collapse" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>

      <!-- This is the "brand" or name/icon representing your site.  Should link to your home page. -->
      <a class="navbar-brand" href="index.html">My BS Site</a>

    </div><!-- /.navbar-header -->

    <!-- Collect the nav links, forms, and other content for toggling -->
    <!-- This is shown when the navbar is not collapsed. -->
    <div class="collapse navbar-collapse" id="bs-ex-nav-collapse">

      <!-- These are the links shown in the nav -->
      <ul class="nav navbar-nav">
        <li class="active"><a href="#">Active Link <span class="sr-only">(current)</span></a></li>
        <li><a href="#">Another link</a></li>
        <li><a href="#">Something else here</a></li>
        <li><a href="#">Last link</a></li>
      </ul>

    </div><!-- /.navbar-collapse -->

  </div><!-- /.container-fluid -->
</nav>
{% endhighlight %}

#### Toggle Behavior
The Bootstrap navbar will collapse into a button to conserve space on smaller devices. Click the button and the navbar will show/hide at the top of the screen. By default this is configured to occur only for xs (or phone sized) devices, but the size where the collapse occurs is customizable.  

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-8">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/default-navbar.png" | prepend:site.baseurl }}" alt="Screenshot of Bootstrap navbar.">
</div>
<div class="col-xs-12 col-md-4">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/default-navbar-collapsed.png" | prepend:site.baseurl }}" alt="Screenshot of Bootstrap navbar collapsed.">
</div>
</div>
</div>

One key to how the collapse/expand functionality works is the `data-toggle` attribute on the `navbar-toggle` button ties to the `id` attribute on the `navbar-collapse` div.  This is important for the javascript that manages the toggle behavior to work correctly.  That value does not need to be `bs-ex-nav-collapse`, but the two values need to be the same.

{% include alert.html type="warning"
   content = "The Bootstrap Navbar component requires JavaScript in order for the responsive *collapse* behavior to function correctly on mobile devices, but it will still function at full-size without JavaScript."
%}

#### Active Link
Another thing worth noting in the navbar example is the `active` link.  It is highlighted in grey (for the default nav style) and also includes an invisible <em>helper</em> style for <code>sr-only</code> (screen readers only). This aids in accessibility and you will see it throughout many of the Bootstrap examples.  The idea is that the `active` style class is moved to show the current page when adding the nav to each page on your site.

### Other Navigation Options
While you can customize the Navbar look to some extent, many *fancier* Bootstrap sites choose to use other components for the navigation.  I assume that a big reason is to avoid a certain *standard* Bootstrap look.  Just because everyone wants the benefits of using a great component library doesn't mean they all want the site to look the same as the next guys.  

The following examples from the Getting Started page show other ways to support navigation on your site:

- [Blog Template](http://getbootstrap.com/examples/blog/) - shows a customized nav that is not using the Navbar component
- [Justified Links](http://getbootstrap.com/examples/justified-nav/) - another customized nav that uses [justified links](http://getbootstrap.com/components/#nav-justified)

Don't be afraid to think out of the box.  There are no *rules* that say you must use a particular Bootstrap component for a certain thing.  It's just a library of options. Check out some of these [real world examples](http://expo.getbootstrap.com/) and count how many you see with a Navbar.  None of them look anything like the examples.


## Image Components

### Jumbotron
The [Jumbotron](http://getbootstrap.com/components/#jumbotron) component is intended for displaying a large marketing message, often with a nice big background image, to catch the attention of visitors right away.  It's pretty straightforward component, but it's appearance will change based on whether it is inside of a Bootstrap container or has a Bootstrap container inside of it.  (Remember not to nest containers!)

#### Full Width
In this [Jumbotron Example](http://getbootstrap.com/examples/jumbotron/), notice that the jumbotron extends the full width of the page. The jumbotron is not inside of a container, but has inside of it a child container to support any other Bootstrap components & styles.

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight html %}
    <!-- Main jumbotron for a primary marketing message -->
    <div class="jumbotron">
      <div class="container">
        <h1>Hello, world!</h1>
        <p>This is a template for a simple marketing or
           informational website. It includes a large callout
           called a jumbotron and three supporting pieces of
           content. Use it as a starting point to create
           something more unique.</p>
        <p><a class="btn btn-primary btn-lg" href="#"
              role="button">Learn more &raquo;</a></p>
      </div>
    </div>
  {% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/full-jumbotron.png" | prepend:site.baseurl }}" alt="Screenshot of Bootstrap full-width jumbotron.">
</div>
</div>
</div>

#### Narrow Jumbotron
In the [Narrow Jumbotron Example](http://getbootstrap.com/examples/jumbotron-narrow/), the jumbotron is placed inside of a container.  This causes it to be displayed padded with rounded corners, instead of extending the full width of the display.

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
{% highlight html %}
<div class="container">
  ...
  <div class="jumbotron">
    <h1>Jumbotron heading</h1>
    <p class="lead">Cras justo odio, dapibus ac facilisis
      in, egestas eget quam. Fusce dapibus, tellus ac
      cursus commodo, tortor mauris condimentum nibh, ut
      fermentum massa justo sit amet risus.
    </p>
    <p>
      <a class="btn btn-lg btn-success" href="#"
          role="button">Sign up today</a>
    </p>
  </div>
  ...
</div>
{% endhighlight %}
</div>
<div class="col-xs-12 col-md-6">
  <img class="img-responsive" src="{{ "/morea/bootstrap-intro/images/narrow-jumbotron.png" | prepend:site.baseurl }}" alt="Screenshot of Bootstrap narrow jumbotron.">
</div>
</div>
</div>

### Carousel
The [Carousel](http://getbootstrap.com/javascript/#carousel) component is another option for displaying a prominent, eye catching marketing message.  It is similar to the Jumbotron, but it allows you to rotate through a series of different images or messages.  

{% include alert.html type="tip"
   content="Notice that you don't see the [Carousel](http://getbootstrap.com/javascript/#carousel) component in the list of CSS components with the Jumbotron.  That is because it is one of the JavaScript components.  The components that rely on [jQuery](https://jquery.com/) and JavaScript to function are on the [Bootstrap JavaScript](http://getbootstrap.com/javascript/) page."
%}

Let's look at an example:

{% highlight html %}
<div id="myCarousel" class="carousel slide" data-ride="carousel">
<!-- Indicators: One must be active or will not display. -->
<ol class="carousel-indicators">
  <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
  <li data-target="#myCarousel" data-slide-to="1"></li>
  <li data-target="#myCarousel" data-slide-to="2"></li>
</ol>

<!-- Slide contents -->
<div class="carousel-inner" role="listbox">
  <div class="item active">
    <div class="container" style="height: 300px; background-size: cover;
         background-image: url(img/city-glitter.png);">
      <div class="carousel-caption">
        Glitter Style!
      </div>
    </div>
  </div>
  <div class="item">
    <div class="container" style="height: 300px; background-size: cover;
         background-image: url(img/flowers.png);">
      <div class="carousel-caption">
        Flower Style!
      </div>
    </div>
  </div>
  <div class="item">
    <div class="container" style="height: 300px; background-size: cover;
         background-image: url(img/shatter.png);">
      <div class="carousel-caption">
        Shatter Style!
      </div>
    </div>
  </div>
</div>

<!-- Controls -->
<a class="left carousel-control" href="#myCarousel" role="button" data-slide="prev">
  <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
  <span class="sr-only">Previous</span>
</a>
<a class="right carousel-control" href="#myCarousel" role="button" data-slide="next">
  <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
  <span class="sr-only">Next</span>
</a>
</div>
<!-- /.carousel -->
{% endhighlight %}

<img class="img-responsive" src="/morea/bootstrap-intro/images/carousel.png" alt="Screenshot of Bootstrap carousel.">
