---
title: "Simple Web Form"
published: true
morea_id: ex-simple-form
morea_type: experience
morea_summary: "Design a simple web form to allow users to subscribe to a newsletter."
morea_sort_order: 1
---

# {{ page.title }}
{{ page.morea_summary }}


## Prerequisites
To successfully complete this assignment, you should be familiar with basic concepts of responsive design and how to make in page links to content.  This is reviewed in the reading for this module: [Forms]( {{ site.baseurl }}/morea/forms/read-forms.html ).


## Overview
For this assignment, you will make a web page for a simple newsletter subscription form.

*Important*: There is no "back-end" for this form page, so you should set up a dummy URL for the form tag, but understand that it will not function when you click submit.


## GitHub
The GitHub repository for this assignment is [simple-form](https://github.com/htc-ccis1301/simple-form).

The repository contains the standard Readme.md and .gitignore files and an empty index.html file.


## Requirements
Create a web page for the Moonflower's Coffee Newsletter.  The web page should include the following:

- A header/h1 for Moonflower's Coffee
- A heading "Newsletter", followed by the text: "Register for our weekly or monthly newsletter by submitting the following form."
- A heading for the subscription form "Newsletter Subscription" followed by text that indicates required fields are marked with an asterisk
- The subscription form as described below


### Form Details
Form fields:

- A fieldset with radio buttons for Weekly (selected by default), Monthly, or Specials Only
- Required textfields for the first name, last name and email address
- A text area for any comments
- A submit button

Use the following id and names exactly (case-sensitive) for the input controls:

- weekly, monthly, specials
- fName, lName, email
- comments

Style the form so that:

- the labels have a width of 120px are right aligned to sit before the input fields
- the text fields are sized to be 35 characters
- the comments area has 5 rows and 34 characters per line
- the width of the fieldset is 350px with a grey lined border
- the submit button aligns with the input fields

On a mobile device, adjust the styles so that the labels sit above the input fields and the input fields have a width of 100%.

You may apply other styles as you see fit, so long as the above requirements are met.

### Sample Page
The full sized page should look similar to the following image:
{% include img-medium.html
    url="/morea/forms/images/simple-form-full.png"
    alt="Sample Form"
%}

The mobile sized page should look similar this image:
{% include img-small.html
    url="/morea/forms/images/simple-form-mobile.png"
    alt="Sample Mobile Form"
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
