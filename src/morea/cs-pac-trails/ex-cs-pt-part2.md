---
title: "Case Study: Pacific Trails Resort - Part 2"
published: true
morea_id: ex-cs-pt-part2
morea_summary: "Second iteration of work for the Pacific Trails Resort Case Study. This work utilizes the material learned in Modules 1-5."
morea_type: experience
morea_sort_order: 3
---

# {{ page.title }}
This assignment includes the case study work from both Chapter 5 & 6 in your textbook.

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different in places. Please use these instructions to direct your work.
</div>

Make sure to check the feedback for your previous assignment on GitHub. Note that errors that are not fixed will continue to have points deducted each week.

## Introduction
In our second meeting with Melanie Bowie from the Pacific Trails Resort, we go over the work that was completed in the first iteration.  We then talk about the changes she would like to see for the next round of work.  This includes some layout changes and the addition of some images to make the site more attractive.

<div style="padding:20px">
<div class="row">
<div class="col-xs-12 col-md-8 col-md-push-2">
  {%  include youtube.html  id="rzLERO-hzHE" %}
</div>
</div>
</div>

## GitHub
Continue working with your forked copy of the [cs-pacific-trails](https://github.com/htc-ccis1301/cs-pacific-trails) repository from part 1. There is no need to fork the repository again.

<div class="alert alert-warning" role="alert">
:warning: <strong>Do NOT make a new folder for each chapter or part of the assignment.  You want each version to update and add to the same directory and files.</strong><br>
GitHub will track versions of your files at each commit, so you can always go back to any previous committed version. If you would like (this is not required) you may create a release for each part of the assignment.  See this <a href="https://help.github.com/articles/creating-releases/">GitHub Release</a> article for information on how to do this.
</div>


## Chapter 5
For this part of the assignment you can follow the textbook instructions exactly. There are no changes for this assignment.  

One of the main parts of the work for this iteration of work is the addition of the new activities.html page.  Remember case-sensitivity and make sure to verify that all of the links to and from this new page work correctly.

Another chunk of work for this part is to add text styling to alter the appearance of the text.  This makes the links bold, the footer small and italic, etc.  All of those things I told you not to do in Chapter 2 because it was not good semantic HTML. Remember that you should only use `<b>` and `<i>` (or the equivalent `<strong>` and `<em>` tags) when needed to mark or highlight specific text for semantic reasons, not just for visual display or design.

Double and triple check your spelling, punctuation, and layout. You might think that these are not important, but imagine if you were the business owner who found their name, address or phone number on the page was incorrect.  Would you hire that person again to do work for you?


## Late Breaking Update!
Melanie was so excited by our web project that she had a new photographer out to their site to take some new images that we can feature on the web site.  

<div style="padding:20px">
<div class="row">
<div class="col-xs-12 col-md-8 col-md-push-2">
  {%  include youtube.html  id="eBh4ioaJvQM" %}
</div>
</div>
</div>

<div class="alert alert-danger" role="alert">
Before making the updates for Chapter 6 to the HTML & CSS, make sure to <strong>commit your changes</strong> so that we can revert this work if needed.  Please use a clear commit message so that we can easily find this revision if needed.  This will be handy if she changes her mind again or if she would like to see the before and after.
</div>

## Chapter 6
Make sure you have versioned your work before beginning the work for Chapter 6.  I will look for your revision showing the previous layout as part of the grading for this assignment.  Don't skip that in between step.  Make sure it has a clearly labeled commit message so that I can identify it. Think business purpose, not "chapter 5".

The work in Chapter 6 has you make some pretty dramatic visual changes to the layout of the Pacific Trails pages.  There is a lot of CSS work here.  Take your time and pay attention to the details, and remember to think about what you are doing.  Consider how the CSS you are writing lines up with the HTML you have written or the changes to the HTML you are making in the later steps.

The new CSS depends on adding a new wrapper div to the page that *wraps* all of the page content inside of the body - everything from the header to the footer. Adding this div incorrectly in the HTML can result in the page not looking correct, as can not selecting it properly by id in the CSS file.  

<div class="alert alert-warning" role="alert">
:warning: As you add the new CSS be aware of when you are selecting items by tag name, by id, and by style.
</div>

I strongly encourage you to write a little CSS, then test your page before continuing on. Students who have the most trouble with this assignment (as well as the next) tend to write all of the CSS then test. Then when something does not appear correct, they struggle to know what part to fix.  By working in smaller pieces, it is easier to know what to change when something doesn't work or look right.

An important skill you should be developing is understanding how you expect the CSS you are writing to change the look of your page. Ideally, the textbook would have integrated these steps so that you could see that better.  But you can work to overcome the books shortfall. As you write each of the CSS rules, think about exactly what that rule should do and watch the live preview in Brackets to see if you are correct.

Being able to do this is a key part of doing the reverse - knowing what you want the page to look like and knowing what CSS to write to make that happen. There will not always be a book there to tell you.  You'll need to create all the CSS for your final project from scratch.

## Testing and Clean-up
I will not be reminding you in the remaining assignments to Beautify your files, validate them, and to test your pages thoroughly.  This is just an assumed thing that you will do to all of your work, both here in class and on the job.  If you're unsure what to do, look back at the tips in the introduction and the detailed instructions in [Part 1]({{ site.baseurl }}/morea/cs-pac-trails/ex-cs-pt-part1.html)

## Submit the Assignment
When everything looks good, create the pull request to have your work graded.

Remember that while you can continue working on the case study locally, it is helpful if you do not push any additional changes to GitHub until the assignment has been graded. I will aim to have feedback to you within a few days of your submission, so you won't have to wait long.
