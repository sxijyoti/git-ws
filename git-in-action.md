---
title: 'Git in Action!'
description: 'Basics of Git and Github'
authors: Saijyoti Panda, Pranav V Bhat
tags: ['git', github, 'open-source']
date: '2025-10-17'
---

Have you ever worked on a project and broken something but couldn't go back? Or wanted to share your code with the world but weren't able to?

That’s where Git and Github comes in, they make saving changes, sharing and collaborating easy.

## Why Git? And What Is It Anyway?

If you ever made a project, you would be familiar with something like this:

![Multiple project folders showing version chaos](https://i.ibb.co/BV5Dm37y/multiple-folders.png)

Git lets you unify all this into a **SINGLE** folder!

Now, what is Git exactly?

Git is a version control tool that keeps track of all the changes you make in your project. It lets you experiment with new features safely and collaborate with others without breaking anything. 

Think of it as a time machine for your code where you can go back, explore past versions and undo mistakes. _Maybe even look at Linus Toravlds past commits for Linux and fix some bugs!_

Cool, right? Having the power to jump back to any version of your project whenever you want.

And when you power Git with Github, it opens the door to a world of endless possibilities. I mean:
- You can share your projects online so anyone can see or use them.
- You can collaborate globally on projects with friends or contributors.
- You can contribute to open-source projects and learn from code written by others.

You are no longer restricted to your friends or your city. The world is your playground! Its like unlocking a whole new superpower ;)

## Installing Git & Setting up SSH

If you haven't installed Git yet. Don't worry, we have some scripts for you that you could run to download Git and also set an SSH key for the same!

NOTE: Use the username and email you use for Github or it would lead to errors!

### For Linux/MacOS

Run the below command:
```
curl -sS https://gist.githubusercontent.com/Prana-vvb/5f48ae8e1173f7b1db105d80c70c2542/raw/10241f14b24427834cebd24128a4fa801fdac148/setup_unix.sh | bash
```

### For Windows

Make sure [Git](https://git-scm.com/) is installed before that!

Then,
- Open Powershell as admin
- Make sure to run `Set-ExecutionPolicy Unrestricted` first
- Run the below command

```
curl -sS https://gist.githubusercontent.com/Prana-vvb/b2602c1aafb692691a88d167a1d9f645/raw/dfaa4f7899b5531d6f9b9993267dc25f841ee4ce/setup_windows.ps1 | powershell -
```

**NOTE: If all these methods fail, do look at something called GITHUB DESKTOP. It's just a Google Search away** ^^

## Creating a Repository

Creating a repo in Github is easy.

Go to your Profile! And click on the `NEW` button

![Image of new button](https://i.ibb.co/rGVSGtX6/new-button.png)

then type in the Name of the Repository and click on `Create Repository`

![Create Repository](https://i.ibb.co/b5V5cXpR/create-repo.png)

**TADA! Now you have your very own repo!**

Btw, you can change the visibility later on too. Just go to Settings.

## Forking and Cloning Repositories

Let's say you want to contribute to someone's repository or maybe an open source project! But what's the best way to do that?

Well that’s where **Forking** comes in. This means creating your own copy of the repository so you can experiment and make changes safely without affecting the original project.

And how is that done?

### How to fork a repository

Click on `Fork`

![Image of fork option](https://i.ibb.co/d4gc2C16/fork-button.png)

Then click on `Create Fork`

Now that you have your own copy of the repository. How will you work from your local system??

### Cloning the Repository

This is where **Cloning** comes in. This lets you copy the repository to your local system so you can work on it locally.

```
git clone <insert-the-repo-link>
```

and where do you find this URL?

![Image of Clone links](https://i.ibb.co/VcYhZQNK/clone-layout.png)

NOTE: Click on SSH and copy link if you have the SSH Setup!

## Working with Branches

Hmm.... what if I want to experiment with a feature? Is there any way to do that **without having to create multiple folders**?

YES! **Branches** let you create multiple parallel versions that you can safely work. Once you are satisfied, you can **merge** them to the `main` branch.

Interesting isn't it? But how do you make a new branch? Run the following commands in your terminal:

```
# Check which branch you are on
git branch

# Create a new branch and switch to it
git checkout -b your-new-branch-name

# Switch to an existing branch
git checkout name-of-the-branch
```

## Git Commits

Remember we talked about exploring past versions? But how are these versions made?

**Commits** lets you do all these cool stuff. They let you take a snapshot of your project at a point in time.

Before committing, make sure you’ve added all the files you want to track:
```
# Add specific files
git add file1 file2

# Or add all changes
git add .
```

Then, commit your changes with a message:
```
git commit -m "Describe your changes"
```
We recommend using [Commit Conventions](https://www.conventionalcommits.org/) to keep your messages clear.

Tip: Pull latest changes before you start work and before you push, to avoid conflicts and keep your branch up to date.

```
# If you're working directly on main
git pull origin main

# If you're on a feature branch
git pull origin your-branch-name
```

But wait, these commits stay on your local system until you  **Push** them:
```
# Push changes to the main branch
git push origin main

# Push changes to a different branch
git push origin your-branch-name
```
An example for this,

<img src="https://i.ibb.co/vCqzQshh/commit-example.jpg" alt="Commit" width="350" />

## Push Requests

Once you’ve made changes on your branch and committed them, it’s time to **share your work** with the original project. That’s what a Pull Request (PR) does.

A PR is basically saying:

> “Hey, I made some changes! Can you review them and merge them into the main project?”

### How to create a PR

Click on Compare and Pull

![Compare and PR](https://i.ibb.co/rGD3zP3V/compare.png)

Then, write a description of the changes you made, double-check the branches at the top, and click `Create Pull Request`.

![Image of Pull Request](https://i.ibb.co/SwWy1FKD/PR-img.png)


That brings us to the end of the blog.

We’ve covered most of the basics of Git and GitHub here. There’s still a lot more to explore, for example, things like merge conflicts, rebasing and deeper Git workflows.

Maybe we’ll dive into those in our next Git blog! ^^