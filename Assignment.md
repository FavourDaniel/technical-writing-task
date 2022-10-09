## Table of contents
1. Introduction
2. What is GitHub?
3. Why GitHub?
4. Git vs GitHub
5. How to clone
6. How to make a pull request
7. How to do a commit
8. Github desktop vs Github CLI
9. Conclusion
    

## Introduction 

As teams work remote;y, it is important that 

It lets you track and manage changes made to files and folders

## What is Github?


## Why GitHub?


## Git vs GitHub


## How to clone
In order to make changes to codes, folders or file, you need to have a copy of the repository where all the files are stored in on your local computer. Assuming you just started working as a developer in a new company, you obviously do not have the files required for your work. All of these files would be stored in a repository which allows you to have access to it from anywhere. With GitHub you can easily clone the repository needed for your work to your local computer, make changes to the project, make a pull request for teammates to see and approve your work and then it gets merged. We would be focusing on cloning a repository for now.

Let's take a look at simple steps to clone a repository

### Sign into your GitHub account. 
Navigate to your browser and log into your GitHub account. If you do not have an account, create one [here](https://github.com/).

### Find the repository to clone
To search for a repo, you can use the `search or jump to...` tab. 

![search](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f4qcn1cnywm7mczl05y0.png)
Search for the repository of your choice and select it to show its details. [Here](https://github.com/wise4rmgod/TechnicalWriterResources) is a sample repository you can use to practice.

After selecting the repo, you should see a screen like the one below

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/dvrq9msndt5m3ptz9avf.png)
Now, click on the code tab in green color and you should see cloning options. 


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ue5pjtki97lj32rlhaxz.png)

HTTPS, SSH and GitHub CLI are 3 different ways you can clone a repository to local computer. You can choose `HTTPS` for this case and copy the link by hitting the copy icon.

The copied link is what would be used to clone the repo.

### Cloning the repository
To clone the repository you would need a terminal, open up Git Bash terminal. If you do not have Git installed on your system, install it [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

Navigate to the directory you want the repository to be cloned to. In my case, it would be cloned to my desktop.
Use the command below to clone

```
git clone <repo link>
```

![git clone](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/u21fefjl55o628kvq0w2.png)
and that's it. You have successfully cloned the repo to your local computer. Check the directory where it was cloned to, and you should see the folder there.

## How to make a pull request
A pull request is a Git action where a contributor requests that the maintainer of a Git repository evaluate code that they intend to merge into a project.

When you have cloned the repo to your desktop and worked or improved the project, you would want to let your team know that.  Repositories usually have maintainers, and these maintainers are the people who have been assigned the position of reviewing work of team members or collaborators. The work you have done needs to be checked testes and checked first to ensure there are no errors, that way ......

Let's create a pull request

### Forking the repo
The repository you want to make a pull request or contribute to needs to be forked. Forking a repository allows you to make changes to that repo without making those changes directly to the original repository.

To fork a repository, hit the `fork` icon on that repository's page

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y61bvi3tc3g2t3s53idd.png)

Choosing to fork a repository makes a copy for you on your own repositories page.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ejulklckfppy0tj3i91c.png)

After forking, clone the repository with the same steps as discussed previously.
 

### Create a new branch
Once the repository has been successfully cloned, you need to create a new branch. The new branch is where your changes would be made. It's recommended that you preserve your main (or master) branch as a "clean" version of the repository from which you forked it so that you can always build it and observe how the "original" repository would function in the absence of your changes. It also ensures that you can always quickly rebase the main/master branch from the upstream without worrying about conflicts.


In git bash, cd into the cloned repo and run the below command to create a new branch

```
git checkout -b <branch-name>
```


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/a9ktn4b7y76rwdljvn94.png)

Any change you want to make should be done in this branch. You can review the changes by running the `git status` command.

### Push branch and changes to GitHub
In the terminal, run the below command

```
git add .
```
This command basically marks or takes note of the files to be version controlled. In this case `git add .` tells git to version control the current directory (.). You can also specify files to be version controlled by using `git add <filename.extension>`.

Commit the changes or marked files and use a descriptive commit message to state what change(s) has been implemented.

```
git commit -m "<commit message>"
```

After committing, run the below command to push the changes to GitHub while maintaining the same branch you made the changes on.

```
git push origin <branch-name>
```
After completing this step, return to GitHub. You should have two branches now on that repository.

11. If you have done the previous steps successfully, you should get a message stating you have made a successful push. Go back to GitHub to see your pushed branch.
12. On GitHub, on the right-hand side of the new branch, you will see a green button tagged 'compare and pull request', click it to proceed.
13. By clicking on 'compare and pull request' you have initiated a pull request, on this page you will see two bars showing your new branch with changes on the right and the Master branch published by the repository owner on the left. Below these bars is a text box, where you can add a message stating why you want to make a pull request to the owner and possibly the changes you made. Then, click 'create pull request'.
14. You have successfully created a pull request after completing step 13, all that's left is to wait for the repository author to accept your request and publish the change you made.

## How to do a commit
[Commit](https://github.com/git-guides/git-commit) is a git command used to save changes made to a local repository before the repository is pushed to the GitHub platform. You have to be specific with the changes you want to commit and also add a message of what the change is about when you implement the commit command line.

The commit syntax is:- git commit -m "a message explaining what the commit is about"

## GitHub desktop vs GitHub CLI
[GitHub Desktop](https://docs.github.com/en/desktop) is a software programme version of GitHub that can be installed on your device. You can implement most Git commands from GitHub desktop with visual confirmation of all the changes you make.
[Github CLI](https://docs.github.com/en/get-started/using-github/github-cli) is an open-source tool that allows developers to access GitHub using your computer's command line interface. You do not need to install GitHub or any software to use GitHub CLI. All you need is already on your computer.

## Conclusion
As a newbie in program development learning how to use GitHub is an essential part of your career in program development. GitHub is basic knowledge and it is necessary to help you connect with other developers, learn from other developers, and possibly get a job opportunity.

I hope this guide was helpful to get you started on what GitHub is and how it works.