---
title: "Graduation Plan Table"
published: true
morea_id: ex-grad-plan
morea_type: experience
morea_summary: "Design a web page with a table to plan out the path to your degree."
morea_sort_order: 2
---

# {{ page.title }}
{{ page.morea_summary }}

## Prerequisites
To successfully complete this assignment, you should be familiar with basic concepts of responsive design and how to make in page links to content.  This is reviewed in the reading for this module: [Tables]( {{ site.baseurl }}/morea/tables/read-tables.html ).

## Overview
For this assignment, you will make a web page that outlines the courses you plan to take for graduation. If you are not in a program for a degree or certificate, you can borrow any of our programs and make things up.  While I'd like this information to be useful, the real intent is to build an HTML table.


## GitHub
The GitHub repository for this assignment is [grad-plan-table](https://github.com/htc-ccis1301/grad-plan-table).

The repository contains the standard Readme.md and .gitignore files and empty index.html & style.css files.  Remember that you need to begin by forking and then cloning this repository.


## Requirements
Create a web page to outline your plans for graduation.  The page should include the following:

- Nav links that include a link to your GitHub profile page, information about this program on the web, and anything else you would like to highlight
- A page header titled something like "My Graduation Plan"
- A section heading calling out the program you are working toward
- A short paragraph with a description of the program and why you are interested in it
- A table with your graduation plan as outlined below
- A footer with your copyright and contact info - it is fine to do a fake mailto like in the case study.

{% include alert.html type="tip"
    content="If you are not currently enrolled in a degree program, here or at another school, humor me by either looking up one of our programs such as the [.Net Developer](https://www.hennepintech.edu/program/awards/411) or making up similar content."
%}

As we near the end of the semester, it doesn't hurt to think about what you might enroll in next semester.  However, please note that I'm not grading your *plan*, I'm grading whether or not you can structure and style this type of information in a table on the web.

### HTML
Build an HTML table to outline the courses required for graduation from your program and when you plan to take them.

Organize the table so that there is a row for each course and they are ordered by semester. Each course should have a semester (when you intend to take the course), the course number, name and number of credits.  These should be reflected as column headings.  Instead of repeating the same semester across multiple rows, have the cell span multiple rows so that information appears only once.

At the bottom of the table, add a summary row showing the total number of credits. Structure the summary row so that it contains only two cells: one with the word "total" and the other with a sum of all the credits from the rows above. Add a table caption with the title and make sure to use the table structure element for the head and footer.

### CSS
Style the table so that:

- the title is in large text similar to a page heading
- the column headings have a different background color and bold text
- there is an alternate background color on every other row (use CSS3 Structural Pseudo-classes)
- the text in the Semester column (use a style class) has a different text color and background color
- apply a different background color to the summary information

Apply CSS to the rest of the page to establish a good margins, padding and layout. You may apply other styles as you see fit, so long as the above requirements are met.

### Sample Page
{% include img-small.html
    url="/morea/tables/images/sample-grad-table.png"
    alt="Sample Table"
%}


## Testing
Once you are happy with your work, push it up to GitHub.  Make sure to check the display of your page live on GitHub Pages and re-validate your page by URL.


## Submit
Create a pull-request and submit the following screenshots to the Assignment box on D2L:

- Open-pull request
- Actual web page as published on GitHub (URL in Settings)
- Validation of HTML file
- Validation of CSS file

You __must__ capture both the validator URL and the validator output in the validation screenshots.