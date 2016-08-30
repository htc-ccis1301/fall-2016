---
title: "Developer Tools Lab 3"
published: true
morea_id: ex-dev-tools-p3
morea_type: experience
morea_summary: "In this exercise will will use the Developer Tools to explore a responsive web page containing media queries."
morea_sort_order: 2
---

# {{ page.title }}
{{ page.morea_summary}}

## Prerequisites
The following topics were covered earlier:

- [Browser Developer Tools]( {{ site.baseurl }}/morea/css-basics/read-dev-tools.html ): To complete this assignment you should be familiar with what browser Developer Tools are and how to use the Dev Tools in the Chrome browser.

## Introduction
For this lab, you will use the browser developer tools to analyze your case study web pages.  To complete this lab, you must have your [Pacific Trails Case Study Part 4]({{ site.baseurl }}/morea/cs-pac-trails/ex-cs-pt-part4.html) work completed and published on GitHub.  You should use your live web site for this lab, not a file or live preview on your computer.

Create a MS Word document to show that you have completed the tasks below. Please clearly label each task. If you are unclear on how to complete a task, I encourage you to ask your classmates in our group chat.

As you go through the tasks below, you will need to:

1. Answer all questions included in the task. and provide a screenshot showing how you got the answer. Be sure to clearly label each screenshots with the task that it corresponds to.
2. Include a screenshot that shows clearly how you have used the Dev Tools to complete that task. The screenshots _must_ show *both* the page content in the browser and the same content in the developer tools.

Solutions that do not include both the above will not receive credit for the task.


### Task 1
Open the home page in the browser and open the Developer Tools. Dock the tools at the right side of the screen.  

If your page is not displayed in tablet size, reduce the width of the page until it is small enough to show the tablet view of the web site.


### Task 2
Locate the HTML element for the wrapper div in the DOM.  Locate the styles that are explicitly applied to this element by your pacific.css file when the page width is tablet sized.  


### Task 3
While still looking at the wrapper div, locate the styles for the desktop sized page.  How many styles are overridden by the tablet CSS?  List the original CSS values and next to them show the overridden values.

It is important to realize that the CSS in the media queries alters the CSS already applied to the element. This is just another part of the *cascade* in the Cascading Style Sheet rules.


### Task 4
While still looking at the wrapper div, adjust the width of the page so that it transforms into the mobile display.  Is any new CSS applied to the wrapper div for the mobile display?


### Task 5
Adjust the page width back to the tablet size and select the nav element. Locate the styles that are explicitly applied to this element by your pacific.css file when the page width is tablet sized.


### Task 6
While still looking at the nav, locate the styles for the desktop sized page.  How many styles are overridden by the tablet CSS?  List the original CSS values and next to them show the overridden values.


### Task 7
While still looking at the nav, adjust the width of the page so that it transforms into the mobile display.  Is any new CSS applied to the nav for the mobile display?


### Task 8
While still looking at the nav in the mobile view, locate the styles for the tablet and desktop sized page.  List the desktop CSS values and next to them show the overridden values first for tablet, then for mobile.


### Task 9
If you uncheck any of the overridden styles, you'll notice that it does not affect the display of the page.  Why not?


### Task 10
Which of the elements contained in the nav do not have overrides for tablet or mobile display?


## Submit Assignment
Make sure that you have clearly labeled and completed each task in your document and saved it as a MS Word file.  

Upload the file to the Assignment box on D2L.
