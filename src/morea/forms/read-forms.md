---
title: "Building & Styling Web Forms"
published: true
morea_id: read-forms
morea_summary: "This modules is focused on building forms for the web.  Forms are commonly used on many types of websites to support the collection of data."
morea_type: reading
morea_sort_order: 1
---
<style>

</style>


# {{ page.title }}
Read Chapter 10 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which introduces web based forms.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## Overview
Chapter 9 introduces tables, which are a common feature on web pages.  Tables can organize information, making it easier to read and understand.  With the addition of some JavaScript (not covered in this course), the data can also sorted and filtered.  This can allow data that was once printed and distributed as reports, or emailed out in spreadsheets to be accessible on the web any time and anywhere.  

## Basic form structure
A web form is created using the `<form>` element and contains labels, inputs and buttons.

The form element must include an `action` which indicates the URL for where the form information should be submitted.  The `method` indicates how the data is sent to the web server - `get` or `post`.  The `get` method is the default and causes the data to be appended to the URL that is sent to the web server.  This makes the data sent rather public as it is visible on the request URL.  The alternate method of `post` is more private as the information is transmitted in the body of the message, not on the URL.  This is method is generally preferred.  The form element also allows for an optional `name` and/or `id` which can help provide access to the form for client-side validation of the information using JavaScript.


### Form Controls
There are a variety of form input controls discussed in the chapter.  You will want to be familiar with all of them.

Basic Controls:

- Text Box
- Submit & Reset Buttons
- Check Box and Radio Button
- Hidden Field and Password Box
- Text Area
- Select List

HTML5 Controls:

- Email & Telephone
- Datalist
- Slider and Spinner
- Calendar
- Color Well

A form fields can be required using the HTML5 `required` attribute, however it is important to remember that it is only checked by browsers that support HTML5.  

It is also good to remember that any type of client-side form validation can be circumvented fairly easily and so as you work with back-end services to handle this data, validation should be repeated on the server.  Client-side validation should be treated as merely a convenience to speed up validation for the user, and not relied upon for clean and valid input data.

## Accessibility
Make sure to use one of the two accepted methods to associate a form control with a label to support accessibility tools.

1. Use the label as a container around both the text description and the form control.
2. Use the label as a container for only the text description and then use the `for` attribute on the label element to associate it with the `id` attribute of the form control.

The second method is generally preferred as it allows more flexibility in the form design.

## Styling Forms
There isn't anything particularly special to note about styling web forms. Just use an appropriate selector for the element and add CSS for margin/padding, text, color, or whatever it is you need or desire to make the form look nice.

## Review Questions

 - What is the purpose of an HTML form?  
 - What attribute(s) are required on the form element?
 - What is the purpose of the `method` attribute?
 - What is the difference between the `get` and `post` method of form submission?
 - Which is considered more private?  
 - How do you indicate a form field is required before the form can be submitted?
 - Does requiring a field provide a 100% guarantee that the data is actually present?
 - What are the two methods used for to associate descriptive text to form controls?
 - Are the HTML5 form controls displayed in a non-HTML5 compliant browser? If so, how?
