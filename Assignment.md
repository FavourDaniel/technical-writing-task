

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
Every basic fundamental skill a developer should have is the knowledge of Git and GitHub. The two tools provide a lot of benefits for organizations and individuals in the sense that everyone can contribute to a project from anyhwere. In this article, we would see how this two tools have made developers life simple and easy.

## What is Github?
GitHub is an open source cloud-based Git repository hosting service.
GitHub makes it possible for developers anyhwere in the world to make contributions to a project, and has been a major factor for remote work as well. It helps in sustaining consistency and visibility.

## Why GitHub?
GiHub has many advantages hence why it has been widely adopted.
- Collaboration: It helps to create seamless collaboration across teams in managing and tracking changes to a project, that way every memeber of the teams is up to date with the latest changes
- Backup of files: GitHub helps to prevent situations when your local computer has been tampered with and you accidentally lose all your files. Hosting projects in an online repository helps for easy retrieval at any time.


## Git vs GitHub
Git is a version control system which is employed to record changes made to files by keeping a track of modifications done to the code. It helps to ensure all team members are working on the latest version of the file. It allows different people to work together on a project from their local machine.

GitHub on the other hand is a Git repository hosting service. It hosts projects which have been worked on already from your local machine. This allows collaborators to see the latest version of that projects and clone a copy of it to their local machine at any point in time.

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

On that repository you should see a `compare and pull request` button, select it. This allows you to initiate a pull request showcasing the change you made and how it differs from the content of the original repository. In the dialogue box below, add a message stating the changes you made and your intent for the pull request, the select `create pull request`.

After initiating a pull request, the maintainer of that repository has to review the changes made and decide whether or not to merge your changes into the original repository.

## How to do a commit
A commit message lets you describe the change or improvement made to a file. It should be descriptive and intentional that way other collaborators know the exact change that has been made.
To make a commit, use the below command

```
git commit -m "<commit message>"
```

## GitHub desktop vs GitHub CLI
Referring to the documentation, [GitHub Desktop](https://www.bing.com/search?q=what+is+github+desktop&cvid=240c58ee909b4a81ab123642ceca7810&aqs=edge.0.69i59j0l8.11779j0j1&pglt=299&FORM=ANNTA1&PC=U531) is an application that enables you to interact with GitHub using a GUI instead of the command line or a web browser, while [GitHub CLI](https://docs.github.com/en/github-cli) is an open source tool for using GitHub from your computer's command line.


## Conclusion
Git and GitHub are two fundamental tools for every developer as they help to maintain project files and keep everyone on the team up to date. Maintaining the synergy in every organization is important, hence why you should start using these two tools.
