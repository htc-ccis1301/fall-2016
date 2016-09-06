---
title: "More Git & GitHub"
published: true
morea_id: read-more-git
morea_summary: "Learn to create a new GitHub repository and populate it with files from your computer."
morea_type: reading
morea_sort_order: 1
morea_labels:
 - GitHub
---

# {{ page.title }}

Throughout this course, we will be using [GitHub](http://github.com/) to manage our projects.  [GitHub](http://github.com/) allows us to have a centralized location to store and manage the projects that we will create in this class. Understanding how to work with Git (the underlying version control system behind [GitHub](http://github.com/)) and [GitHub](http://github.com/) are very important topics in this course.


## Creating a new repository
Most assignments for this class will begin with a starter repository that you will *fork* from our course GitHub page.  This gives you a general layout for the project and any starter code that you should have to begin.  You'll then *clone* the repository to your computer.   

But what do you do if you don't have a repository to fork and clone?  You can create a new repository on the GitHub website and either add starter files to it on the web so that you can clone it to your computer OR you can start with code in a directory on your computer and turn that directory into a git repository that you link to GitHub.  This is the process that I usually follow, as I typically start the project before I think about making a spot for it on GitHub.

The process for creating a new GitHub repository is the same.  On the GitHub website, you go to your profile, then your list of repositories, then click the green "New" button.

{% include img-small.html url="/morea/more-css/images/github-new-repo.png" alt="Screen capture showing new button." %}

On the next page, you need to name the repository, decide if it will be public or private, and whether or not you will initialize it on GitHub then clone or do that on your computer. If you already have files on your computer, it is easiest to leave the "initialize" box unchecked, and generally I just always take this approach anyway.

{% include img-small.html url="/morea/more-css/images/github-new-repo-init.png" alt="Screen capture showing create repository page." %}

__Do not check the box to initialize on GitHub.__  We will start with files on our computer.  The next screen gives you the commands to do this.  

Click the green "Create Repository" button.

{% include img-small.html url="/morea/more-css/images/github-new-repo-cmds.png" alt="Screen capture showing commands to initialize locally." %}

Go to the GitShell (or terminal) and go into the directory that contains your files.  

1. Enter the echo command to create a simple README.md file.  
2. Enter the `git init` command. This is used to initialize a new git repository.  
3. Add and commit the README.md file.
4. Enter the `git remote add origin` command by copying it from GitHub.  This includes the URL to your personal repository and connects your local repository to the remote repository on GitHub.  

Do not push any changes yet.  

## Add an ingore file
The .gitignore file that you see in our class projects is used to keep certain types of files out of your project repository.  Generally these are temporary files or helper files added by your operating system.  Copy one of the .gitignore files from one of your other assignment repositories and add it to each new project.


## Working with Branches
When you create a new repository and make your first commit, that commit is made to the `master` branch.  For work that is not published on the web using GitHub pages, that is fine.  However for this course we want our work to be published, so we need to move it to the gh-pages branch.

{% include alert.html type="tip" content="If you add projects for other courses that are not websites, it will make sense to leave that work on the master branch. Only use the gh-pages branch for websites you want published on GitHub." %}

### What is a branch?
A branch is a separate line of version history for your project.  It is a space where changes can be worked on and versioned in isolation, without affecting other branches of work in the same repository.  Generally work that is on the `master` branch is always complete, tested, and ready for real world use.  To aid in development, we will often create separate branches where we can work on and test separate ideas and features without affecting the "live" version of the project.  More info on [Branching and the GitHub Flow](https://guides.github.com/introduction/flow/).

### The gh-pages branch
The gh-pages branch on GitHub is special.  Using this branch tells GitHub that you want those files to be published to the web.  Remember that you can see the URL for where this is published to in the Settings for your GitHub repository.

If you look back at your previous assignments, you'll notice that all of that work was setup to be on the gh-pages branch for you.  When you forked the code, the default branch had already been switched to be gh-pages.  When you create a new web project repository, you'll need to make this change yourself.

{% highlight bash %}
$ git branch -m master gh-pages
{% endhighlight %}  

{% include alert.html type="warning" content="You will not be able to do this until you have committed a file. If you get an error with this command, make sure you have a file that you have added and committed to your repository." %}

Once you have switched the branch, you can push your changes to GitHub.  However, you will need to specify that you are pushing the changes from the gh-pages branch.

{% highlight bash %}
$ git push -u origin gh-pages
{% endhighlight %}  
