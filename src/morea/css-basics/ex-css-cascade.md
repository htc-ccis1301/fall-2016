---
title: "CSS Cascade"
published: true
morea_id: ex-css-cascade
morea_type: experience
morea_summary: "Practice applying CSS to a web page while exploring the CSS Cascade."
morea_sort_order: 2
---

# {{ page.title }}
In this exercise we will explore the way CSS is applied and how the *cascade* works in more detail.  This exercise is similar to the one in Hands-On-Practice 4.7 in your textbook, so you can refer back to it, but remember that the actual exercise is different.

## Prerequisites
The following topics were covered earlier:

- [Basic CSS]( {{ site.baseurl }}/morea/css-basics/read-css-basics.html ): To complete this assignment you should be familiar with how CSS works and how to use it to alter the background and font colors on a web page.  You should also understand how to validate the CSS on web page.
- [Browser Developer Tools]( {{ site.baseurl }}/morea/css-basics/read-dev-tools.html ): To complete this assignment you should also be familiar with how to use the browser developer tools in Chrome.

## GitHub
The GitHub repository for this assignment is [css-cascade](https://github.com/htc-ccis1301/css-cascade).

## Instructions
Open the project folder in [Brackets]().  Notice that you have an HTML file and a CSS file provided for you.  If you view the web page, you'll see that it should look like this.

<img class="img-responsive" src="{{ "/morea/css-basics/img/initial-page.png" | prepend:site.baseurl }}" alt="Screenshot of initial web page." />

### Inherited CSS
Notice that there is a CSS rule to set the background color of the `body` element to be light purple (#E6E6FA), and the foreground or text color to be dark purple (#191970).

This style is inherited by every element inside of the body making the entire background light purple and all of the text dark purple.  

If a child element has a CSS rule applied to it directly, that is applied to the element instead of  the inherited style.  

1. Add a new style rule to the external CSS file to give paragraph elements a medium purple background color (#AEAED4).

2. Look at one of the paragraph elements using the developer tools.  Notice that the inherited style for the background color from the body is crossed out.
<img class="img-responsive" src="{{ "/morea/css-basics/img/inherited-applied-p-style.png" | prepend:site.baseurl }}" alt="Screenshot of CSS applied to p tags to change background-color." />

3. Notice that while this changed the background-color, it did not affect the text color.  While the paragraphs no longer use the inherited background-color, they still inherit the color property that controls the text color.

### Specificity
What happens if two rules would affect the same element?  How does the browser know which rule to apply?

1.  Add an id element to one of the paragraphs in the main content.  You can name the id whatever you would like and apply it to any one of the paragraphs in the main element.  

2.  Add a CSS rule to the external CSS file to change the background-color of that ID to be white.

3.  We now have two rules that apply to that paragraph.  Use the developer tools to see the CSS applied to that paragraph.  
<img class="img-responsive" src="{{ "/morea/css-basics/img/id-override-p-style.png" | prepend:site.baseurl }}" alt="Screenshot of CSS applied to p tag by id." />

4.  Notice that the browser did apply the `p` element rule, but then for the paragraph with this id, the rule is crossed out.  This means that the rule is overridden by another rule that applies to the same element.  

Because the style rule for ID is more specific than the style rule for all HTML p elements, the browser uses the ID rule.  

Rules that are more specific win.

We do not need to use id's to be more specific.  We can also use style classes or descendant selectors. A style class is more specific than an HTML tag name, an ID is more specific than a style class.  

Using HTML tags in a descendant selector is also more specific than using a single HTML tag, but when style classes or id's start to be involved, things can become more complex.  We'll leave it at this for now, but if you want to know more, checkout the [official rules](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity).

### Last one in wins
If there are two rules that are equally specific, the last one in wins.  

1.  Add a second CSS rule to your external style sheet that will change the background-color of the  paragraphs to be red.  

2.  Again look at the applied CSS using the developer tools.
<img class="img-responsive" src="{{ "/morea/css-basics/img/id-override-p-style.png" | prepend:site.baseurl }}" alt="Screenshot of two CSS rules applied to p tag." />

3.  Notice the line numbers.  The color will be set by the rule that is the last in the file to set the background-color.  

4.  Take out this red paragraph rule.  It's not so pretty with my purples!

This is an important thing to remember, as a common cause of issues in this course is having multiple rules for the same selector in the CSS file.  This is not incorrect, but if you have a long CSS file and do not see the other rule, this can be confusing.  Because of this, I strongly encourage you to look through your CSS before adding a new rule for a new selector.  Make sure there isn't already one there that you can add a new property into instead of adding a new rule.

### Cascade - External, Embedded, & Inline CSS
For this course, I'm going to expect that you understand how external, embedded, and inline CSS work together.  This can be a topic for quizzes and exams.  However for all your assignments, except for this one, you should use only external CSS.  

1.  Add an embedded style to the index.html file to change the color of the paragraphs to be blue (#A6C6DF).

2.  When you view your page, you should see that your paragraphs are now blue.
<img class="img-responsive" src="{{ "/morea/css-basics/img/embedded-override-external.png" | prepend:site.baseurl }}" alt="Screenshot of embedded style overriding external." />

3.  Next add an inline style to one of the paragraphs that does not have the ID applied to it.

4.  Notice that one paragraph you applied the inline CSS to is now a lighter blue.
<img class="img-responsive" src="{{ "/morea/css-basics/img/inline-override-both.png" | prepend:site.baseurl }}" alt="Screenshot of inline style overriding both embedded and external." />


### Descendant Selectors
Descendant selectors in CSS are very important.  They get used __a lot__ because they help you to be more specific without the need for adding extra stuff into your HTML.  Let's say that we want to have all of the paragraphs in the main content get their background-color from their parent element.  

Let's add this new rule to our external stylesheet. First we need to know how to write the selector to get only paragraphs that are inside the main element.  

{% highlight bash %}
main p {

}
{% endhighlight %}

Next question is how do we know what the background-color of their parent element is? It could be different for each paragraph, right?  They may not all be direct children of the `main` element.  (Notice the one that is a child of a `div` which is then a child of `main`.)  To have an element use the value of its parent, we can use the word `inherit` as the value of the property.

{% highlight bash %}
main p {
  background-color: inherit;
}
{% endhighlight %}

Now what color do you expect the background-color for paragraphs to be?  Will they all have the same background-color, or do you think some will still be different?  Think about this before you try it out.  If things are different than what you expected, see if you can figure out why.  Use the developer tools to help you.

<div class="alert alert-info">
:dizzy: Note that you don't need to use `inherit` very often because it is the default behavior.  You would only need to use it to *undo* other applied CSS, much like we are doing here.
</div>

## Submit
Create a pull-request and submit the screenshot of it in the Assignment box on D2L.

You must also submit screenshots that show you have validated both the CSS & HTML file for this assignment.  Please ensure that you capture the validator URL and the validator output in each screenshot.
