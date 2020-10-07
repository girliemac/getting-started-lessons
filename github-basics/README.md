# [Lesson Topic]

This lesson covers the basics of GitHub, a platform to host and manage changes to your code.


## [Pre-lecture quiz](.github/pre-lecture-quiz.md)

### Introduction

In this lesson, we'll cover:
- tracking the work you do on your machine
- working on projects with others
- how to contribute to open source software

> Notes

### Prerequisite

Before we can well get started, you'll need to check if Git is installed. In the terminal type: 
`git --version`

If Git is not installed, [download Git](https://git-scm.com/downloads). Then, setup your local Git profile in the terminal:
`git config --global user.name "your-name"`
`git config --global user.email "your-email"`

To check if Git is already configured you can type:
`git config --list`

You'll also need a GitHub account, a code editor (like Visual Studio Code), and you'll need to open your terminal (or: command prompt). 
Navigate to [github.com](https://github.com/) and create an account if you haven't already, or log in, and fill out your profile. 

### Preparation

We'll need both a folder with a (code) project on your local machine (laptop or PC), and a public repository on GitHub, which will serve as an example for how to contribute to the projects of others.  

---

## [Code management]

You have a folder locally with some code project and you want to start tracking your progress using git - the version control system. Some people compare using git to writing a love letter to your future self. Reading your commit messages days or weeks or months later you'll be able to recall why you made a decision, or "rollback" a change - that is, when you write good "commit messages".

### Task:

On GitHub, in the repositories tab, or from the navigation bar top-right, find the “new repo” button. Give your repository (folder) a name, and select “create repository”.

In your terminal, switch to the folder (or: directory) you want to start tracking:
`cd [name of your folder]`

Initialize a git repository in your project:
`git init`

`git status` will list out all the files in your working directory.

Then type `git add .` to add all your files & changes for tracking.

Then type:
`git commit -m "first commit"`

This commits all of your files, adding the message “first commit”. For your next commit messages you will want to be more descriptive in your description. 

Next type:
`git remote add origin https://github.com/username/repository_name.git`

Your GitHub Repository page will list the repository URL, so feel free to copy and paste from there, rather than typing it in manually. This creates a remote, or connection, named “origin” pointing at the GitHub repository you created earlier.

Then type:
`git push -u origin main`

This sends your commits in your “main” branch to GitHub. 

If you want to continue making changes and pushing them to GitHub you’ll just need to use the following three commands:
```
git add .
git commit -m "type your commit message here"
git push 
```

You might also want to adopt a `.gitignore` file to prevent files you don't want to track from showing up on GitHub - like that notes file you store in the same folder but has no place on a public repository. You can find templates for `.gitignore` files at github.com/github/gitignore.

#### Commit messages
A great Git commit subject line completes the following sentence:
If applied, this commit will <your subject line here>

For the subject use the imperative, present tense: "change" not "changed" nor "changes". 
Just as in the subject, in the body (optional) also use the imperative, present tense. The body should include the motivation for the change and contrast this with previous behavior. The why, not the how. 

### Task:

## [Working on projects with others]

In your repository, navigate to Insights > Community to see how your project compares to recommended community standards.

Like, did you add a description for your project? How about a README? GitHub provides guidance for writing a [README](https://docs.github.com/articles/about-readmes/). Does your project have [contributing guidelines](https://docs.github.com/articles/setting-guidelines-for-repository-contributors/), a [Code of Conduct](https://docs.github.com/articles/adding-a-code-of-conduct-to-your-project/), and perhaps most importantly, a [license](https://docs.github.com/articles/adding-a-license-to-a-repository/)? All these resources will benefit onboarding new team members. And those are typically the kind of things new contributors look at before even looking at your code, to find out if your project is the right place for them to be spending their time.

### Task: 

Contributing docs help people contribute to the project. It explains what types of contributions you're looking for and how the process works. You will probably want people to "fork" your project, creating a replica of your repository on their GitHub profile. From there they will clone the project to their local machine. You will want to ask them to create a "branch" for their work. Ask contributors to concentrate their contributions on one thing at a time - that way the chances that you can "merge" in their work is higher. Imagine they write a bug fix, add a new feature, and update several tests - what if you want to, or can only implement 2 out of 3, or 1 out of 3 changes?

Be the change you want to see in the world, and create branches for your own work as well. Any commits you make will be made on the branch you’re currently “checked out” to. Use `git status` to see which branch that is.

Create a new branch:
`git branch [branch-name]`

Switch to the specified branch and update the working directory:
`git checkout [branch-name]`

Combine the specified branch’s history into the current branch: 
$ git merge [branch]

Delete a branch once you're done with it:
$ git branch -d [branch-name]

Once you made your changes, commit and push your code, and create a pull request on GitHub. Pull request is a silly term because really you want to push your changes to the project. But the maintainer (project owner) or core team needs to consider your changes before merging it with the project's "main" branch.  

A pull request is the place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more. A good pull request follows rougly the same rules as a commit message. You can add a reference to an issue in the issue tracker, when your work for instance fixes an issue. This is done using a `#` followed by the number of your issue. For example `#97`.

Fingers crossed that all checks pass and the project owner(s) merge your changes into the project 🤞

Update your current local working branch with all new commits from the corresponding remote branch on GitHub:
`git pull`


## [How to contribute to open source]

First, let's find a repository - or: repo - on GitHub we'll want to copy the contents of to our machine. 

![Get a repo locally](/images/clone_repo.png)

Now, we have several ways of copying code. We could "clone" the contents of the repository, using HTTPS, SSH, or using the GitHub CLI (Command Line Interface). 

Open your terminal to clone the repository like so:
`git clone https://github.com/ProjectURL`

To work on the project, switch to the right folder:
`cd ProjectURL`

We could also open the entire project using [Codespaces](https://github.com/features/codespaces), GitHub's embedded code editor / cloud development environment, or [GitHub Desktop](https://desktop.github.com/).

Lastly, we could download the code in a zipped folder. 

### Task:

You can star, watching, and/or "fork" any public repository on GitHub. You can find your starred repositories in the top-right drop-down menu. It's like bookmarking, but for code. 

Projects have an issue tracker, mostly on GitHub in the "Issues" tab unless indicated otherwise, where people discuss issues related to the project. And the Pull Requests tab is where people discuss and review changes that are in progress.

Projects might also have discussion in forums, mailing lists, or chat channels like Slack, Discord or IRC.

✅ Knowledge Check - use this moment to stretch students' knowledge with open questions

## [Topic 2]

## [Topic 3]

🚀 Challenge: Add a challenge for students to work on collaboratively in class to enhance the project

Optional: add a screenshot of the completed lesson's UI if appropriate

## [Post-lecture quiz](.github/post-lecture-quiz.md)

## Review & Self Study

Read more about [contributing to open source software](https://opensource.guide/how-to-contribute/#how-to-submit-a-contribution). 

[Git cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/).

Practice, practice, practice. GitHub has great learning paths available via [lab.github.com](https://lab.github.com/):
- [First Day on GitHub](https://lab.github.com/githubtraining/first-day-on-github)
- [First Week on GitHub](https://lab.github.com/githubtraining/first-week-on-github)

You'll also find more advanced labs. 

**Assignment Due [MM/YY]**: [Assignment Name](assignment.md)
