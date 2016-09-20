---
title: "Fan Page Part 7"
published: true
morea_id: ex-fan-page-p7
morea_type: experience
morea_summary: "Give the fan-page a responsive design & layout."
morea_sort_order: 2
---

# {{ page.title }}

## Prerequisites
To successfully complete this assignment, you should be familiar with the two-column page layout and how to use CSS for positioning elements.  This is reviewed in the reading:  [Page Layout]( {{ site.baseurl }}/morea/page-layout/read-page-layout.html ).

{% include alert.html type="warning" content="As you build this site, be careful in the use of images, text, and other content from other sources. Unless you have created the content yourself, I expect that you to have permission to use anyone else's material. You should note such permissions near the content or place it in the footer. You should also note copyright of others materials - for example, note the footer on this page [Guild Wars 2 Boss Timer](http://guildwarstemple.com/dragontimer/)"
%}

## GitHub
The GitHub repository for this assignment is [fan-page](https://github.com/htc-ccis1301/fan-page).

Remember that once you have forked and cloned this repository, you do not need to do that again.  Just continue creating and editing files through Brackets and use the git add, commit, and push commands to update GitHub.


## Requirements
For this assignment, you will modify your fan site to have in-page links and a responsive layout.  

### Navigation
Configure a nav with a unordered list.  Have the first link go to your home page "index.html".  Use a short title or small image/logo to identify your "home page".  This link can be used to come back to the top of the page or return to the home page if other pages are added later.

Setup CSS to remove the underlines from your navigation links, slightly increase the font size, and specify different font colors (not the defaults) for visited and non-visited links.

You can choose to position the nav horizontally or vertically on your page, but add CSS to style the nav list so that it is not too crowded and is separated and distinct from the other content.

### In Page Links
Add additional structure to your main content area through the use of HTML5 article, section or aside elements.  Separate each of your four sub-headings into its own section (or article) element.  Give each section an id attribute and use that to add in-page links to your nav for each of the sections or sub-headings.

### Responsive Layout
Use CSS Media queries to adjust your desktop layout for better usability on a mobile device.  You should aim to

## Note on Grading
This week's requirements are a lot more open than in previous weeks and the grading will be a bit more subjective.  I will look specifically for the color palette, but the remaining points will be based on how well you have designed your site to look professional and illustrate principles from the text as well as the 60-30-10 rule.

## Testing
Once you are happy with your work, push it up to GitHub.  Make sure to check the display of your page live on GitHub Pages and re-validate your page by URL.

## Submit
Create a pull-request add a pull-request comment to include your thoughts on why it would make maintenance of a web site easier to keep all styles in an external CSS file and out of the HTML files.

Submit the following screenshots to the Assignment box on D2L:

- Open-pull request
- Actual web page as published on GitHub (URL in Settings)
- Validation of HTML file
- Validation of CSS file

You __must__ capture both the validator URL and the validator output in the validation screenshots.
