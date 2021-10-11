# Week 3: Tuesday 10/1

### GitHub Collaborative Development

#### Collaborators

A GitHub repository has at a minimum a single owner who created the repository within their account. That owner can add collaborators (other GitHub users) that are given access to the repository. A collaborator is allowed to clone and push changes to the repository. This is the typical set up for a software development group within a company that is working on a project. 

#### Open-source Community

Some repositories want to allow contributions from the development community outside of the collaborators. Git has a featured called forking, which is used for this purpose. 

When you fork a repo, you first go to the repo you wish to fork, click the fork button, and this creates a copy of the repo within your own account. The copy has a link back to the original repo, which enables two important features:

1. You can pull an update from the original to your copy when desired.
2. You can create and test a proposed change locally and then create a pull request to the original repository, asking to merge your changes into their repo.

Let's look at an example of an open-source project: Visual Studio Code. Take a look at the following files: README, Issues, Pull Requests, Insights, Contributors

* README
* Issues
* Pull Requests
* Insights
* Contributors

{% embed url="https://github.com/microsoft/vscode" %}

In this exercise, we're going to focus on the first scenario, where we are limiting the repository to our restricted set of collaborators.



### Software Development Workflow

All git repositories start out with a main branch. This is supposed to be "production ready", meaning that it can be deployed to the production site at any time.

How do you control the process of developers working on features and adding their changes to the production code and minimizing the introduction of bugs into production? There is not a single agreed upon solution. Over the years the solutions have evolved.

Early on, when desktop applications predominated, there was the need (which still exists) to support multiple versions of the software simultaneously. For example, multiple versions of the Chrome browser are out in the field at the same time. If there is a bug discovered in an earlier version, Google has to fix that bug in all of the versions that are currently supported in the field. They cannot say that the customer has to upgrade to the latest version to get the fix. This made  the number of long-lived branches that needed to be maintained more complex and slows down the whole development process.

Web applications are different. There is only a single version at a time. This reduces the complexity, but it is still a difficult problem with a lot of different solutions.

There are two main contributors to minimizing the change of buggy code going into production.

1. **Branching**: working in an isolated environment until your code is ready to be incorporated into the main branch.
2. **Testing**: building and running tests continuously on your local changes, and the merge in changes to find bugs as quickly as possible. Tests are then run on the main branch to ensure that the entire code base works with all recent changes incorporated.

If you have extremely good testing practices, which is somewhat rare, then you can possibly eliminate the need for branching altogether and just work in your local copy of the main branch, run the tests on your local copy, and then push your changes into the main branch on GitHub.  

There is a current movement to support this model, as it reduces the complexity greatly, and thereby increases productivity. But it requires a lot of tooling in place to automate the running of tests and it also requires that the developers are experienced and understand the processes and know how to write good tests and high quality code. 

When there are more junior developers on the team, then short-lived feature branches, and paired-programming are recommended techniques.

In most cases, the trend is toward trunk-based-development, meaning that you want to minimize the amount of time developers are working away from the trunk (main) branch. If a branch is necessary it should be short-lived.

An additional technique to support short-lived branches, is to use feature tags to be able to toggle on/off a feature in the production code. The feature can be incrementally incorporated into the production code, but it would be turned off until it is complete.  

### Working within a Branch

Git can be tricky to get beyond the basics of working in your own repo in the main branch. When working within a branch, you just need to use the few commands:

* **git add** . (add any changes to staging area for next commit) 
* **git commit** -m”comment” (take a snapshot of staging area) 
* **git push** (push changes to GitHub) 
* **git status** (check for current status) 
* **git log --oneline** (show history of changes with one line summary)





### Branching









****



Create a site called

### Git/GitHub

* [Intro](https://www.youtube.com/watch?v=BCQHnlnPusY\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=1)
* [Branching](https://www.youtube.com/watch?v=oPpnCh7InLY\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=2)
* [Issues](https://www.youtube.com/watch?v=WMykv2ZMyEQ\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=4)
* [Merge Conflicts](https://www.youtube.com/watch?v=JtIX3HJKwfo\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=9)
* Template Repo
* npm/package.json/node_modules
  * markdownlint-cli
  * prettier
  * cspell
* [Undoing commit to wrong branch](https://www.clearvision-cm.com/blog/what-to-do-when-you-commit-to-the-wrong-git-branch/)
* review git commands
  * git status
  * git add
  * git commit
  * git push
* new git commands
  * git branch
  * git checkout -b \[branch]
    * pulls uncommitted files to new branch [https://www.atlassian.com/git/tutorials/using-branches/git-checkout](https://www.atlassian.com/git/tutorials/using-branches/git-checkout)

### Creating a Repo for Collaboration

We're going to create a practice repository where we can learn

* how to create and setup repo for collaboration
* how to create markdown files
* how to work in branches
* how to use pull requests
* how to resolve merge conflicts

