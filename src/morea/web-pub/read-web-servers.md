---
title: "Install a Web Server"
published: true
morea_id: read-web-servers
morea_summary: "How to install and run a web server for desktop testing."
morea_type: reading
morea_sort_order: 1
---


# {{ page.title }}
{{ page.morea_summary}}


## Web Server on your Desktop
Throughout the course, we've been using GitHub Pages to host our web pages. The text book discusses hosting your newly created site with a traditional web hosting company. Hosting companies use web servers to share your web sites with the world.  Often it is beneficial to setup a similar web server locally on your computer so that you can mimic their behavior for testing.  

<div class="well well-sm">
:memo: Actually installing Apache and working through the steps below is optional, but you should read through and understand the concepts presented.  (Brackets includes a built in web server.  More info below.)
</div>


### XAMPP Install
A common and very simple way to install the Apache Web Server is by installing XAMPP.  Information on installing XAMPP on various systems can be found on the [Apache Friends](https://www.apachefriends.org/download.html) website.  Follow the default install instructions.  If prompted, you should include both the Core and Developer files.

For the purposes of this class, you do not need anything but the Apache Server, but unless you are short on space, just running the default installation which includes Apache, MySql database, PHP, and Perl is fine and a little less effort.

### Verify Apache Starts
Once the install is complete, you'll want to test to make sure that the Apache server will start.

1. Launch the XAMPP application.  You should get a Welcome application window and it may launch the XAMPP page in your default browser.

2. In the application window, select the Manage Servers tab.

3. If it does not indicate that Apache is running, select it and click Start.

4. If you get errors when starting Apache, check the Apache Friends FAQ page for your system for troubleshooting tips:   [Windows](https://www.apachefriends.org/faq_windows.html), [Mac](https://www.apachefriends.org/faq_osx.html), or  [Linux](https://www.apachefriends.org/faq_linux.html).

5. Additional help can be found on their [forums](https://community.apachefriends.org/) or [Stack Overflow](http://stackoverflow.com/search?q=xampp).

<div class="alert alert-warning" role="alert">
:warning: While Apache can be configured to launch and start running at startup, for a development setup, it is probably best to only start Apache when you need it to test your site. Make a habit of stopping the server when you are done with your testing.
</div>


### Publish your content
When publishing your site to an Apache server, you place your web project folder in the server's `htdocs` directory.  On Windows, go to the location where you installed xampp.  Under the xampp folder, you should see `htdocs`. On the Mac, look for XAMPP under Applications and you will see the `htdocs` folder there as well.

<div class="well well-sm">
:memo: Typically you don't edit the files in the htdocs directory.  You will move your files from the location where you edit and version them to the server each time you want to begin testing.  Since this can be tedious to do repeatedly, many developers will write a script to do this.
</div>

#### View your Content
Open a web browser and in the address area, enter `localhost:80`. (The 80 is the port number that the web server listens on. This can be changed in the configuration.)  Unless you have modified the defaults, this should bring up a page that shows XAMPP.
{% include img-small.html
    url="/morea/web-pub/images/deployment-xampp.png"
    alt="Image of the XAMPP welcome page in the browser at localhost:80."
%}

To get to your content, you need to add your folder name onto the end.  So if you've published your Pacific Trails files under htdocs in a ptCaseStudy folder, access it by entering `localhost:80/ptCaseStudy`.
{% include img-small.html
    url="/morea/web-pub/images/deployment-ptCaseStudy.png"
    alt="Image of the Pacific Trails home page in the browser at localhost:80/ptCaseStudy."
%}

Just entering the folder name in the address bar relies on having an `index.html` page in that directory.  The web server will look for that index.html file specifically and show it when the folder path is requested.  If you do not have an index.html page, then you will get an error.

#### Why do I need a server to test?
For the purposes of this class, you really don't *need* one.  All of the work that we do can easily be tested just by opening files in the browser.  By using a web server though, you can check that you didn't use any file system links accidentally, and by moving your files from your development location to a different spot for testing, you can ensure that you have identified and moved all the important files.

Once you start making dynamic web pages that use JavaScript to pull data interactively from a server, testing with an actual web server becomes more important.  Browsers have security features built in that will not allow them to get content from different locations, or cross sites.  This means if you get a page initially from your file system, you'll get an error if it tries to get say weather data from some server on the web. However if that page is loaded from a web server, like Apache, different security restrictions apply that can allow that data to be loaded.

#### Brackets includes a web server
You may not realize it, but you've actually been testing your files all along with the [Node.js](https://nodejs.org/) web server built into Brackets.  This web server is what gets cranky if you don't open the entire project folder in the editor instead of just individual files.

Did you notice that when you use the *Live Preview* feature, the address in the browser begins with `http://127.0.0.1` followed by : and a number?  The 127.0.0.1 is the same as localhost (*usually*).  The number following the : is a port number.  Brackets uses a different port number than the default of 80 in order to avoid conflicts.
