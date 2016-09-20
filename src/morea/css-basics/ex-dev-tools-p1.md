---
title: "Developer Tools Lab 1"
published: true
morea_id: ex-dev-tools-p1
morea_type: experience
morea_summary: "A first experience using the Developer Tools to explore a web page."
morea_sort_order: 2
morea_labels:
 - dev-tools
---

# {{ page.title }}
{{ page.morea_summary}}

## Prerequisites
The following topics were covered earlier:

- [Browser Developer Tools]( {{ site.baseurl }}/morea/css-basics/read-dev-tools.html ): To complete this assignment you should be familiar with what browser Developer Tools are and how to use the Dev Tools in the Chrome browser.

## Instructions
For this lab, you will be using the Chrome Developer Tools to peek at the HTML and CSS applied to a web page.  To begin, you'll need to open the page in the Chrome browser:
[Click here to open the lab's web page](http://htc-ccis1301.github.io/dev-tools-lab/).

Create a MS Word document to show that you have completed the tasks below. Please clearly label each task. If you are unclear on how to complete a task, I encourage you to ask as opposed to not completing the task. Learning to use the Developer Tools is an important skill for fixing issues with your web pages and analyzing their structure.

As you go through the tasks below, you will need to:

1. Answer all questions included in the task. and provide a screenshot showing how you got the answer. Be sure to clearly label each screenshots with the task that it corresponds to.
2. Include a screenshot that shows clearly how you have used the Dev Tools to complete that task. The screenshots _must_ show *both* the page content in the browser and the same content in the developer tools.

{% include alert.html
    type="danger"
    content="Solutions that do not include both a screenshot and the answers to each question in the MS Word document will not receive credit for the task."
%}


### Task 1
Open the Developer Tools and have them docked in the lower portion of the screen.  Make sure the Elements panel is visible.


### Task 2
Locate the head element in the DOM and expand the tree to show all of its child elements.  

How many stylesheets are used on this page?


### Task 3
Locate the header element in the DOM and expand the tree to show all of its child elements.

Select the header and look at the applied CSS.  What CSS is used to add the image to the header?


### Task 4
Locate the element that contains all of the Weekly Specials content in the DOM. Make sure that you are locating the element that contains all of that *yellow* content, not just the header that says "Weekly Specials".  When you select this element, you should see the highlight stretch across the full width of the page, covering all of that *yellow* content.

Select that element and expand the tree to show its children.
- What is the name of element used?
- What attributes are on the element?  
- How many child elements does it contain?


### Task 5
Locate an h3 element in the DOM and select it. Scroll down so that the heading is visible in the browser as well as the Developer Tools.  Note that when you hover over the h3 element in the Developer Tools, the element on the page is colored in blue and orange.

What does the blue and orange coloring represent?


### Task 6
In the Developer Tools, locate the diagram of the _CSS box model_ for the h3 that you selected above.

- What is the size of the h3 content?
- Is there padding applied to the element? If so how much and on which sides?
- Is there a border on the element?  If so what size?
- Is there margin applied to the element? If so how much and on which sides?

### Task 7
What colors are used for the background and the text in the "Our Team" section of the page?


### Task 8
Using the Developer Tools, modify the “Our Team” header to say “Awesome People” and change the text color for only this heading  to black using __an inline style__.  (To add an inline style you must edit the HTML element.)

Note: Two very handy hex color codes to know by heart are black and white.  If you don’t know them (and you probably don’t yet), look them up.

### Task 9
Show the JavaScript console.  

Did any errors occur while loading the page?  

### Task 10
How would you find out how long it took to load a resource that this web page required?

How long did it take to load the Bootstrap stylesheet?

## Submit Assignment
Make sure that you have clearly labeled and completed each task in your document and saved it as a MS Word file.  

Upload the file to the Assignment box on D2L.
