# Intro-Course-Github-Practice-Fall-2025
Welcome to the NURobotics Intro to Robotics Course's practice repository. We'll be using this repo as practice to get familiar with git and GitHub. The following is a step-by-step instructional guide for making your first commit and push!

# Purpose of a README file
## AKA what even is this file you're reading right now?
It introduces and explains a project. Typically it's the first file you create in a project.

Today's instructions will be in this(README) file.

For more info: https://www.makeareadme.com/

# Tutorial
## Overview
We've provided a txt file with a template of some info for you to fill out. In this tutorial, we'll be duplicating the template, renaming the file, filling it out, and eventually merging it with the main branch.

## Git and GitHub
What's the difference between these things? What even is "git"?

Well, let's start with git. Git is a version control system (VCS). It's a way to track changes in code and is a key asset when working on a codebase with several developers. Think of it like the version history feature in Google Docs. You can see what the file looked like at different timestamps, see who made what changes, and even revert to old versions and restore changes.

GitHub, on the other hand, is a service that hosts git repositories. There are other repository-hosting services like GitLab and Bitbucket, but GitHub is the most popular and is what we'll use.

Check out this post to learn more about the differences: https://blog.hubspot.com/website/git-vs-github.

TDLR - Git is the software that actually tracks code changes within a repository, and GitHub hosts these repositories via a web interface.

## Accessing the repository
What is a repository? GitHub docs define it as:
> A repository contains all of your project's files and each file's revision history. You can discuss and manage your project's work within the repository.

Well, the first step in this tutorial was to access the repository on GitHub. If you're reading this now, chances are you're here! If not, go to https://github.com/NEURoboticsClub/Intro-Course-Github-Practice-Fall-2025.

## Opening the Command Line
### On a Windows
>Click: the Start button or press the Windows key on your keyboard.

>Type: cmd or Command Prompt into the search bar.

>Select: "Command Prompt" from the search results to open it.

### On a Mac
>Open Spotlight: Press the Command (⌘) key + Spacebar. 

>Type "Terminal": In the search bar that appears, type Terminal. 

>Launch Terminal: Press Enter or double-click on the Terminal application from the search results.

## Cloning a Remote Repository
### What is a remote repository?
A remote URL is Git's fancy way of saying "the place where your code is stored." That URL could be your repository on GitHub, or another user's fork, or even on a completely different server.

You can only push to two types of URL addresses:

For an HTTPS URL:
`https://github.com/user/repo.git`

For an SSH URL:
`git@github.com:user/repo.git`

Git associates a remote URL with a name, and your default remote is usually called `origin`.


### Cloning *this* repo
In your command line type `git clone https://github.com/NEURoboticsClub/Intro-Course-Github-Practice-Fall-2025.git`

You can find the link by clicking the green `code` button and then copying the HTTPS URL.
![Cloning a repo from GitHub](img/git_clone_url.png)

Cool! Now we have a local version of the repository that we can make changes to. It should look like this now.
![Cloning a repo in terminal](img/git_clone.png)

## Creating a new branch
Before we actually start making changes, we're going to create a new branch. Branches allow us developers to work in a contained area and not affect the main branch directly. 

Why is this important? Well, say you're responsible for developing an algorithm for using the ultrasonic/servo sensors on the elegoo kit and your team is using GitHub to host the code. The main branch is where all the action happens and should be code that is tested and validated to work. As you're working on your algorithm, you might introduce bugs or break existing code. By working on a separate branch, you can safely develop your feature and then merge that branch back into main when complete.

Creating a new branch isn't 1000% necessary - it depends on how your team uses GitHub. The nice thing about working with a VCS like git is that it's easy to revert changes should something go wrong. Regardless, we're going to be creating a branch to do our work.

In your command line type `git branch your-name`.

Then to switch to the branch you just created, type `git checkout your-name`.

It should look like this:
![Switching branch](img/branch-checkout.png)

Then to `push` the branch to the remote repo, type `git push -u origin your-branch-name`


## Making local changes
Okay recap - we've cloned the repository from GitHub, created a branch for us to do some development in, published the branch to GitHub so it knows it exists, and now we're ready to make our changes.

For this activity, we'll be duplicating the template file, renaming it, and populating it with information.

To do this type `cp template.txt your-name.txt`

![Duplicating a file](img/duplicate_file.png)

To fill out the .txt file you can open it in a text editor or you can edit it directly through the command line.

Type `nano your-name.txt`.

Then directly edit the file. To exit, follow the instructions on the bottom of the terminal.

![Editing a file](img/edit-template.png)

## Staging and committing
Nice! We've made some changes in the repo and now we should add and commit these changes. Whenever we make a commit, we are taking a snapshot of what the repository looks like at this point in time. This way, we can revert to old commits if necessary or even just view what changes happened when.

But first we need to add the changed files.
To do this type `git add .`

Then type `git commit -m "a description of what you are changing to the repo"`

For this activity, your message can be "edited your-name.txt"

![Adding and commiting a file](img/git_add_commit.png)

## Pushing changes
Now that we've created a commit with the desired changes, we can push to origin. Why do we need to do this? Well, we've already told GitHub that we created a branch but it doesn't do any automatic checking if the branch had changed on our local machine - that's why we need to push the changes. 

Type `git push`

Hmmm did this do anything? Let's see! Go back to the repo in GitHub and refresh your page. Hmmm main looks unchanged... but wait! That's expected! We've made changes on our own branch. Hit the dropdown where it says "main" and find your branch.

![View branch on GitHub](img/view-branch.png)

Aha! Our changes are here. 

## Opening a pull request
Now that we have our updated branch in the GitHub repo, let's create a PR so we can see the changes in main! Hit the "Compare & Pull Request" button to get it started.

![Preview PR](img/push-changes.png)

It should open up a page that looks something like this. It'll show what's been changed on our branch between when we created the branch and now.

If all looks good, hit "Create Pull Request".

![Create PR in GitHub Desktop](img/pull-request.png)

We're almost there now! We now have a pull request that will preview the changes before we actually merge it into the main branch. 

Click the `merge request` button

## Aftermath
The moment of truth. Is our code finally on the main branch? Switch from the "Pull requests" tab to the "Code" tab. Awesome! You'll see that the PR was merged and that the newly created file is now on the main branch. Nice work!

![Update main](img/updated_main.png) 
