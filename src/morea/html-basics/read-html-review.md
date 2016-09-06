---
title: "HTML Review"
published: true
morea_id: read-html-review
morea_summary: "A review of the foundational HTML tags and HTML document structure."
morea_type: reading
morea_sort_order: 1
---

# {{ page.title }}
Before we move on to learning new HTML tags, take a moment to look back at the template HTML at the end of chapter 1.

Remember this Basic HTML5 Template:
{% gist mbMosman/5785c6e9534e956b79d7 basicHTML5.html %}

Recall that the elements that are inside of the `<head>` describe the page, while the elements that are in the `<body>` are the visible content on the page.  While the `<title>` in the head section is used by the browser, it is not considered displayable content.  It is however often used as the browser window or tab title.

### Tags and Elements
You might notice that there are two different words used with HTML, "tag" and "element". While these are often used interchangeably, they technically have different meanings.  A tag is just the thing between the angle braces <>, for example you might talk about the `<title>` tag.  The title element on the other hand is everything from the start tag to the end tag.  It also includes the text (or any child elements) between the start and end tag.  So the title element might be `<title>Ice-cream Rocks!</title>`.  

Attributes are also part of an element, and they are also part of the tag since they are written inside of the angle braces <>.  We looked at a few tags that include an attribute.  One example was the `<meta charset="utf-8">` tag.

Remember that attributes are key value pairs. In that example, the name of the attribute is "charset" while the value is "utf-8".  Attribute values must always be enclosed in quotes.


### HTML Structure
It is also very important to understand the tree structure of HTML. This critical to understanding how CSS is applied to your page. We'll start working with CSS in the next module.  It is also important for later work with JavaScript.  

The `<html>` tag is the root of this structure. It will always have two children - `<head>` and `<body>`.  Remember that *__child__* elements, also called children, are those that are between the opening and closing tag of the *__parent__*. Since the html element is the parent of both these elements, we say that the head and body are *__siblings__*.

Relationships go deeper than just parent and child.  In a family tree you would talk about grand-children and grand-parents.  With HTML, instead of talking about grand-children, we use a more generic term of descendant to refer to deeper nested elements.  So while the parent of the title element is head, title is a *__descendant__* of the html element. The reverse would be that html is an *ancestor* of title, but we rarely talk about the relationships from that direction.

### Review Questions
Look at the template HTML above and answer the following questions:

- What is the relationship between the body element and the p (or paragraph) element?
- What is the relationship between the title element and the meta charset element?
- What is the relationship between the meta charset element and the html element?
- What is the relationship between the html element and lang="en"?  
