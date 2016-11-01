---
title: "Building & Styling Tables"
published: true
morea_id: read-tables
morea_summary: "This module is focused on structuring and styling tables for the web.  Tables are a common feature on web pages, organizing information to make it easier to read and understand."
morea_type: reading
morea_sort_order: 1
---
<style>
table {
  margin: 10px;
  padding: 5px;
}

th,td {
  padding: 5px;
  border: 1px solid #000066;
}
</style>


# {{ page.title }}
Read Chapter 9 of your textbook [Basics of Web Design: HTML5 & CSS3](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/) which covers building and styling tables on the web.  

Remember that you can get the example code from the book electronically from the [textbook website](http://wps.pearsoned.com/ecs_felke_bwdHTML5_CSS3_3/).  It is important to experiment with the material as you read and learn it so that you understand it well.

## Overview
Chapter 9 introduces tables, which are a common feature on web pages.  Tables can organize information, making it easier to read and understand.  With the addition of some JavaScript (not covered in this course), the data can also sorted and filtered.  This can allow data that was once printed and distributed as reports, or emailed out in spreadsheets to be accessible on the web any time and anywhere.  

## Basic Table Structure
<div class="alert alert-warning" role="alert">
:warning: The example tables below are styled with the CSS for this site, so they will look different without CSS applied.
</div>

A basic table `<table>` is just made of rows `<tr>` and cells `<td>` (which make up the columns).

{% gist 5785c6e9534e956b79d7 basicTable.html %}

That produces a table that is structured like this:
<table>
    <tr>
        <td>Row 1, Column 1</td><td>Row 1, Column 2</td><td>Row 1, Column 3</td>
    </tr>
    <tr>
        <td>Row 2, Column 1</td><td>Row 2, Column 2</td><td>Row 2, Column 3</td>
    </tr>
    <tr>
        <td>Row 3, Column 1</td><td>Row 3, Column 2</td><td>Row 3, Column 3</td>
    </tr>
</table>


### Headings and Caption
To make the table a little fancier, you can also add headings and a caption or title.

{% gist 5785c6e9534e956b79d7 basicTable2.html %}

That produces a table that is structured like this:
<table>
    <caption>Basic Table with Headings</caption>
    <tr>
        <th>Heading 1</th><th>Heading 2</th><th>Heading 3</th>
    </tr>
    <tr>
        <td>Row 1, Column 1</td><td>Row 1, Column 2</td><td>Row 1, Column 3</td>
    </tr>
    <tr>
        <td>Row 2, Column 1</td><td>Row 2, Column 2</td><td>Row 2, Column 3</td>
    </tr>
    <tr>
        <td>Row 3, Column 1</td><td>Row 3, Column 2</td><td>Row 3, Column 3</td>
    </tr>
</table>


### Spanning Rows & Columns
It's not uncommon to want a row or column to take up the space of more than one *cell*.  This can improve the table display when there are things like grouped rows or columns. This is not something used for every table, but it is important to know that you *can* do this.


### Accessibility
Make sure to use the `id` and `headers` attributes in your tables to support accessibility. Remember that it is your job to know that you need to include these pieces to make your pages accessible. Don't wait for someone to tell you to do it.


### Styling Tables
Older HTML tables were styled using attributes on the HTML tag.  Now that CSS is widely supported, it is considered a best practice to avoid the use of the HTML attributes for styling and to use CSS instead.  

The tables above are styled using the following CSS:
<pre>
table {
  margin: 10px;
  padding: 5px;
}

th,td {
  padding: 5px;
  border: 1px solid #000066;
}
</pre>

### Table Structure
Tables can get rather complex, especially if they are containing groups of data with summary information.  To assist with the layout of these tables, there are grouping elements to help you structure your tables.  These elements are `thead`, `tbody` and `tfoot`.  While it is not necessary to use all of these in every table, you should use them to separate headers from the table body or contents, and if the table contains summary information, it should be placed in the `tfoot`.


## Review Questions

 - What is the purpose of a table in HTML?  
 - Why should you not use attributes such as `cellpadding`, `cellspacing`, and `summary` on new HTML pages?
 - What is the difference between a `th` and a `td` element?
 - Where is a table caption positioned in the table HTML?  Why it is used?
 - How do you have a table cell span multiple rows?  Multiple columns?
 - How is the `headers` attribute used in an HTML table?  Why is it used?
 - How do you eliminate the space between the table's cell borders using CSS?
 - How do you style table rows so that every other row has a different background color?
 - Tables have 3 structural elements to group rows.  One is `tbody`, what are the other two? Give an example of how they might be used.
