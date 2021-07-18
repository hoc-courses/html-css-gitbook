---
description: Using GitHub Classroom to manage assignments
---

# Assignments Intro

We are going to be using **GitHub Classroom** to manage homework assignments. This will give you lots of experience using **git** and **GitHub**, which is a very useful skill, both for personal use, and one that employers require of new hires.

## Summary

GitHub Classroom allows instructors to create a set of repositories that are templates for assignments that they can then assign to students.

For each assignment, GitHub Classroom will make a special URL link. When you go to that link in a browser, GitHub will create a private repository for you, with a name that includes both the assignment name and your GitHub username.  This repository is a clone of the starter repository. The repository is a private repository owned by the course staff \(so we can view it\) that the student will have write access to.

The student uses this created repository to create their assignment. This will involve cloning the repository to your local computer, editing the files and adding new ones, committing the changes \(to your local repository\), and pushing these changes back to the GitHub repository \(so the instructor can view it\).

The basic workflow is:

* The instructor provides you with a repository on GitHub with the start of a project.
* You **clone** this repo to your laptop
* You do some work
* You **commit** the changes you made to the project
* You do some more work
* You **commit** the changes you made to the project
* You **add** files if you created new ones in the project
* You **push** the changes back to your remote repo on GitHub
* You do some more work
* You **commit** your work
* You **push** your changes to the GitHub Repo
* repeat until done
* The instructor clones your repo from GitHub so they have a copy to look at.

## Starting an assignment

You will receive a link \(URL\) to the assignment on the Homework page. Paste the link into a browser. You will be presented with a page like the following. 

Click the **Accept this assignment** button.

![](../.gitbook/assets/image%20%28192%29.png)

You will be directed to the following screen, asking you to wait for the assignment repository to be configured..

![](../.gitbook/assets/image%20%28200%29.png)

After a minute or so, refresh the page and then click on the link to the assignment.

![](../.gitbook/assets/image%20%28207%29.png)

Clicking on the assignment link will redirect you to the GitHub website where a repository has been created for you. The repository is not within your own GitHub account. It is part of the classroom account for the course.

![](../.gitbook/assets/image%20%28209%29.png)

### Assignment Contents

The assignment repository contains all of the files you need to complete the assignment. 

#### README.md - Assignment Directions

The assignment will always contain at a minimum, a README.md file, which is what a repo displays as the default file for the repo. It is written in a special language \(markdown\) which allows the author to add special tags which will format the content to display nicely.

#### Starter Files

Depending on the nature of the assignment, there may be starter files included in the assignment repo that you will use to start your assignment. The README.md file would explain what is included and how to setup the assignment with any starter files.

### Cloning the Repository to your Local Computer

Cloning is what you do when you want to **create a local copy of a GitHub repository and maintain a connection to the GitHub repository from your local computer**. This allows you to work on the assignment on your local computer and push your changes back to the GitHub repository when the assignment is complete \(or at any time along the way to save intermediate snapshots\).

To clone a GitHub repository, you click on the green Code button, and then click on the clipboard icon to copy the URL for this repository.

![](../.gitbook/assets/image%20%28198%29.png)

The next step is to use the repository URL in the **git clone** command to clone the repository. 

There are two options for how to clone your assignment repository.

#### From the Command Line

Before issuing the git clone command, make sure your current directory is where you want the repository folder to be created. In this case, you should create it in your **web-dev-fall-2021** course folder.

One disadvantage of doing this from the command line, is that the Bash Shell doesn't paste without using the right mouse button to bring up the context menu and then selecting the Paste option from that menu.

So, first you would type git clone on the command line, then use the context menu to paste in the GitHub repository URL as the second argument and then enter.

![](../.gitbook/assets/image%20%28203%29.png)

Once the command has completed, you can issue the **ls** command to see that a new directory, named bash-shell-\[your-githubusername\], has been created. Use the **cd** command to change directories into the newly created directory, followed by the **ls** command, to see the files that are included in this assignment.

#### From Visual Studio Code

When VS Code first starts up, you are presented with a welcome screen that gives you the option of cloning a repository.

![](../.gitbook/assets/image%20%28204%29.png)

After you click on either of the links shown above, you will be presented with a box to paste in the assignment URL.

![](../.gitbook/assets/image%20%28194%29.png)

This will then automatically clone the GitHub repository and load the project.

## Turning in Your Assignment.

The following depicts the process that occurs on your local computer and the commands involved with working with your local repository, and the push command that pushes the changes from your local repository to your corresponding GitHub repository.

![](../.gitbook/assets/image%20%28202%29.png)

**git init** - this step occurred automatically when the GitHub repository was cloned to your local computer. You only need to do this step when you create a local repository first.

**git add** - adds any changed files to the staging area to be committed to your local repository.

**git commit -m "some message"** - commits the changed files in your staging area to a new snapshot, which is permanently available in the history of tracked changes for your repo. This git commit command takes **an additional flag, -m**, **followed by a message in quotes**, to provide a message to describe the changes associated with this commit.

**git push** - pushes any changes you have made since the last commit to the GitHub repository, thereby syncs up the GitHub repo with your local repo.

These three steps, **a**dd, **c**ommit, **p**ush, are commonly referred to as the **ACP cycle**, and can be repeated as many times as desired as you work on your project. Is is a good practice to push to GitHub whenever you are at a stable point after making some changes. This ensures that you can always return to that point if the need arises.

Once these operators are complete, your assignment has been turned in and your instructor can view your assignment and provide feedback if necessary.

At any time, you can return to the GitHub page for the assignment repo, and refresh the page to see any changes you have pushed.

**Note:** if you have forgotten the URL for the GitHub assignment repo, you can just paste in the assignment URL again and it will take you to the GitHub assignment repo page.

