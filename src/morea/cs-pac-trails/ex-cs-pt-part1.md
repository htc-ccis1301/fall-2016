---
title: "Case Study: Pacific Trails Resort - Part 1"
published: true
morea_id: ex-cs-pt-part1
morea_summary: "First iteration of work for the Pacific Trails Resort Case Study. This work utilizes the material learned in Modules 1-3."
morea_type: experience
morea_sort_order: 2
---

# {{ page.title }}

This assignment includes the case study work from both Chapter 2 & 4 in your textbook.

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different in places. Please be sure to read the notes within this module to direct your work for each part of the assignment.
</div>

## Introduction
In our first meeting with our business client Melanie Bowie from the Pacific Trails Resort, we go over the page layout and expectations for the first round of work.

<div style="padding:20px">
<div class="row">
<div class="col-xs-12 col-md-8 col-md-push-2">
  {%  include youtube.html  id="U43K9TkswDw" %}
</div>
</div>
</div>


## GitHub
The initial repository for this project can be found on our class organization page:

[cs-pacific-trails](https://github.com/htc-ccis1301/cs-pacific-trails)

You will only need to fork and clone this project once.  Then for each part of the assignment you will make changes, add, commit, and push them.  You'll want to be sure to test your site running on the GitHub web site (find the URL under Settings), validate your page, then create the pull-request for grading.

Once you clone this to your computer, open the project folder in Brackets and look through it.  It contains all of the images and multi-media files you will need to complete the project. You just need to add the HTML & CSS.  

<div class="alert alert-warning" role="alert">
:warning: Do not create a new folder as indicated at the start of each chapter's Case Study instructions in the textbook!  You should place your HTML files directly into the cloned repository folder.  Do not add a sub-folder for your HTML pages.
</div>

## Chapter 2
The case study instructions from the end of Chapter 2 have you create the home page and the yurts page.  

### Semantic HTML
The instruction will ask you to add `<b>`, `<small>`, `<i>`, and `<strong>` tags to the HTML for both the Home and the Yurts page.  Don't do this.  It's not semantically correct, and they are just going to have you take it out when you start the work for Chapter 4. You will lose points for not removing all of these, so it helps to just not put them in.

### Home Page
Make sure to call the Home page index.html.  This is an important file name, as it is used by most web servers as the default page when a specific HTML page is not requested.  Also remember to treat all file names as case sensitive. If you work on a Windows computer, your local computer will not care if you call the file Index.html in one place and index.html in another. However the GitHub web server will care and you will get a broken link resulting in a lower score on the assignment.

Make sure to note the layout of the contact information on the home page. There should be a blank line between the address and phone number. Also note the company name is considered part of the contact information and should be inside that div.

I recommend that you validate each page as you are finished with it.  It can be easier to fix any errors while the changes you make are fresh in your mind.

### Yurts Page
For the Yurts page, the book asks you to use the `<dl>`, `<dd>`, and `<dt>` tags.  These don't make for a very nice display and aren't very semantically correct.  Instead you should use  `<h3>` and `<p>` tags.  The questions go in the h3 elements, and the text below should go inside a paragraph element.  I will look for this as I am grading, so don't forget to make this change.  

### Links
Test your links!  The link from the Home to the Yurts page should work, and the link from Yurts to the Home page should work.  Make sure to test both ways!  

You should also verify that these are __relative links__.  They must not include any drive letters from your local computer.  Your file system will not match the web server's and that will result in broken links when you publish your site.

### Add & Commit Incrementally
Once you have a part of the assignment done and tested, I recommend you add and commit those files locally to your git repository.  You can also push and test them on GitHub if you like, but at least doing the add/commit, means that you could come back to this working state later if you "break" something and want to go back.


## Chapter 4
Remember - Do not create a new folder as indicated at the start of the Case Study instructions in each chapter of the textbook!

In Chapter 4, you learn about CSS, so in this part of the Case Study we will add CSS to improve the look of the pages you created in Chapter 2.

Be careful with adding the `<link>` tag.  If this is not correct, you will not see any results from adding the CSS.  A relative path should be used. Again, no drive letters should be present in the path.

The only change here from the textbook instructions is in Task 2.  You should code a style for the h3 element instead of the dt element, to match the change we made above in the HTML.  Use the same color as indicated in the text, #000033.

### Resort Style Class
A common error on this part of the case study occurs with the resort style class that displays the Pacific Trails Resort name in blue.  Pay attention to the instructions for this.  It requires HTML tags be added to the html file in addition to the changes in the CSS. This style class should be applied each time the company name is used in paragraph text or in the address block.    

### CSS Validation
The validator for CSS files is different than the validator for the HTML files.  Students often forget this as they do the validation for this assignment.  Make sure to use the [W3C "Jigsaw" validator](https://jigsaw.w3.org/css-validator/) for CSS - note the word jigsaw in the URL.


## Local Testing
When you've worked through all the steps, do some testing on your site locally before pushing your files to GitHub.  Check that all your links work, and remember that even though the header and navigation look the same on all pages, the HTML for this is coded separately on each page.  This means the link to the Home page may work from one page and be broken on another.  You need to test all the links on all the pages individually.

Double check your page layout and display. There are images in the book, but remember that you may have differences in appearance due to the changes I have you make in *my* instructions.  The videos include mockups of the site layout and may be a better reference. Think about any differences you see before just making changes, and when in doubt ask.  It's better to ask and find out early if there is an issue.  All employers would be happy to have you ask instead of delivering the wrong thing to a client.

I also encourage you to save your files and close Bracket and then re-validate your HTML and CSS files.  Many times students will validate and have no errors, but find later that's because they didn't save their changes.  

## Code Cleanup
Please use Beautify to help format your code for readability before turning it in. Clear and consistent use of indentation helps prevent errors in development and allows me to give better feedback on your work.  Points for assignments may be reduced if I find your files too hard to read or comment on.  

## Push to GitHub & Test Again
When everything looks good, add & commit your changes then push your files up to GitHub.  Verify your changes have been pushed, then test your updated site on the web by clicking on the URL under settings.  I strongly recommend that you copy this URL and edit your repository description to include this link so that you can open your page again easily.  You will be testing it many times over the semester, so this small effort now will payoff long term.

Retest your page on the web, checking page layout and verifying links again. (Case-sensitivity can break links here that work when you test on locally on Windows!)  

Paste the URL from your live page (not the GitHub view of the text) into the W3C Validators to validate your page on the web by URI instead of file upload.  This is what I will do to grade your work, so it's an extra precaution that you don't lose a large chunk of points due to validation errors.

## Submit the Assignment
When everything looks good, create the pull request to have your work graded.

While you can continue working on the case study locally, I encourage you not to push any additional changes to GitHub until the assignment has been graded.  Your pull request will automatically update to include any additional commits that are pushed to GitHub.  Local commits stay local, but pushed commits will update the pull request.

I will aim to have feedback to you within a few days of your submission, so you won't have to wait long.

Pushing new changes before I have graded will not "break" my ability to grade your work, so if you do really need to do this for some reason, that's totally fine.  However it may make it more difficult for you to get detailed feedback on any issues. You'll still get feedback, it just might have to come through general comments not line-level comments.  It's generally not a big deal, but if you can hold off for a bit I'll appreciate it.
