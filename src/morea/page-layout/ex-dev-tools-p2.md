---
title: "Developer Tools Lab 2"
published: true
morea_id: ex-dev-tools-p2
morea_type: experience
morea_summary: "In this exercise we will use the Developer Tools to explore the Pacific Trails Resort website."
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
For this lab, you will use the browser developer tools to analyze your case study web pages.  To complete this lab, you must have your [Pacific Trails Case Study Part 2]({{ site.baseurl }}/morea/cs-pac-trails/ex-cs-pt-part2.html) work completed and published on GitHub.  You should use your live web site for this lab, not a file or live preview on your computer.

Create a MS Word document to show that you have completed the tasks below. Please clearly label each task. If you are unclear on how to complete a task, I encourage you to ask your classmates in our group chat.

As you go through the tasks below, you will need to:

1. Answer all questions included in the task. and provide a screenshot showing how you got the answer. Be sure to clearly label each screenshots with the task that it corresponds to.
2. Include a screenshot that shows clearly how you have used the Dev Tools to complete that task. The screenshots _must_ show *both* the page content in the browser and the same content in the developer tools.

Solutions that do not include both the above will not receive credit for the task.

### Task 1
Open the home page in the browser and open the Developer Tools. Dock the tools at the bottom of the  screen.  

Using the Elements panel, locate the header element in the DOM and show how you can use the dev tools to temporarily toggle the display of the sunset.jpg image in the header.


### Task 2
Locate the HTML element that contains the hero image in the DOM.  Show the styles that are explicitly applied to this element by your pacific.css file.


### Task 3
While still looking at the hero image element, show the styles that are applied to that element because they are inherited from the body style in your pacific.css file.


### Task 4
While still looking at the hero image element, show the developer tools can be used to identify the exact size of the image shown in pixels.  (Note this is not the size of the actual image, it is the size of the image as it is displayed on the web page.)


### Task 5
Identify and select the element that contains the address.  Use the developer tools to reduce the font size used for the contact information to 80%.

Notice that you can use the up and down arrows while editing the size to increase and decrease the value. Is there a point where the font size no longer becomes smaller?  If so, what is that value?


### Task 6
How many file requests were made to load the home page?  Which file took the longest to get?  What was the overall load time for the page?


### Task 7
Locate the `<h2>` tag in the DOM. Use the developer tools to change the text-shadow color to black.


### Task 8
Use the developer tools to increase the horizontal offset (1st number) of the text shadow by 3px.  How would you describe that effect of altering this value?  Reset this property to its original value.


### Task 9
Use the developer tools to increase the vertical offset (2nd number) of the text shadow by 3px.  How would you describe that effect of altering this value?  Reset this property to its original value.


### Task 10
Use the developer tools to increase the blur radius (3rd number) of the text shadow by 3px.  How would you describe that effect of altering this value?  What is the result if you remove this value entirely?  Reset this property to its original value.


## Submit Assignment
Make sure that you have clearly labeled and completed each task in your document and saved it as a MS Word file.  

Upload the file to the Assignment box on D2L.
