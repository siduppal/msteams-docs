---
title: Tools for writing for Teams developers
description: What tools to use when writing for teams developers. 
keywords: Teams writers developers tools platform dev docs
ms.date: 01/09/2019
---
# Setting up your tools

These are the tools I use. YMMV. Other topics here will assume that these tools are installed.

## Markdown

All of our source documents are written in MarkDown, a simple text format that has the extension md.  Specifically we use the GitHub flavor of MD.  You can find the answer to any question you might have on how to use MD with a simple web search.
Try to keep things as simple as possible - no tables within tables, no nested lists, that sort of thing. It makes your writing much easier to read, and limits build and rendering issues.

## GitHub

First of all, you need to get a source repository set up on your local machine so you can have access to those markdown files.  We use GitHub to manage all source documents, which in turn uses git.
When I started I spent a couple of hours discussing git with someone who knew it really well, and that conversation paid off. I did not find it obvious or intuitive at first because it used odd terms and did not work like other tools I had experience with. Now that I understand it I'd be reluctant to use anything else.

## GitHub Desktop

I really like the GitHub Desktop tool as a way to clone, branch, and update source documents. It is less error prone than the git command line, and is much more self documenting.
Install it from: https://desktop.github.com/

If you have access to GitHub on the web and can access [MicrosoftDocs/msteams-docs](https://github.com/MicrosoftDocs/msteams-docs) you should be able to log into the client and get access to the same repos with the same log in credentials.

## Clone the msteam-docs repo using GitHub desktop

Your first step is to clone the MicrosoftDocs/msteams-docs repo to your local machine. Since I'm already signed in and have a local repo, I can't walk through the steps without messing up this writing session. As I recall, it was pretty obvious. You want to File>Clone Repository, and in the filter box in the Clone a repository dialog, enter `msteams-docs'. Take a moment to set up your local path - this is where all your local copies of all files will be stored.

>[NOTE]
Don't edit files directly in the master branch until you understand what you are doing.

The files stored on your local machine are now a copy of everything that is in the master branch of msteams-docs at this particular moment in time. You don't want to edit any of these files directly - this is after all the master. What you need to do is create a "branch" off of master to hold your changes until you are ready to have them reviewed and merged into master.

## Create a branch off of master using GitHub desktop

In the GitHub desktop toolbar there is an indicator that says what your current branch name is. Click on the drop-down arrow next to this and click on the "branches" tab.
Below that you will see a box marked "filter" and a button marked "New Branch".  This is where you will create new working branches off of master to keep your work in. It's common to have several branches going at one time to hold work for different work items. Sometimes work items can get delayed and you don't want to hold up other work waiting for them to be resolved.
We have a simple naming convention for branches. It is not enforced in any way, but it helps track who is responsible for what changes.

'Yourname-description-with-hyphens'.  For 'Yourname' first or last works fine - whatever you are comfortable with.

If you now edit a file in your branch, and commit it in locally, nothing will show up on the server until you click "Push origin" in the toolbar of the GitHub desktop. This will push your branch back to the server, and include your changes.

When you are ready to merge your changes back into master it is good practice to have someone else review your changes as a last sanity check. Do this by opening a pull request (PR) in GitHub.  Click on Branch>Create pull request, which will open the browser and send you back to the GitHub website to complete your pull request.

## Editing md files using Visual Studio Code

MD files are simply text files, and so any text editor will work, even notepad - however the best (free) tool that I've found is [Visual Studio Code](https://code.visualstudio.com/). It has extensions for markdown including syntax checking, and provides good integration with GitHub when you need to resolve merge conflicts.

It's best feature is that it builds a project tree in the left hand window based on the directory structure of your files in the repo, which makes finding and managing source files easy.

## Spellchecking and formatting plugins for Code

You will want to add extensions to catch syntax errors in markdown (Markdownlint), and simple spelling errors (Spell Right). There are many options in each category, and some may be better than the ones I use.  New stuff appears all the time.

## Building and deploying sample code using Code

For JavaScript/TypeScript projects Code is an excellent tool. It works with all samples I've tried, and it has decent support for Azure app hosting through the Azure App Service plugin.

## Building and deploying C# code using Visual Studio

C# requires the professional version of Visual Studio, not the Code app. There are decent Azure plugins here as well.  When writing about using samples, it is best of course to use the tools that you are discussing.

## Editing screenshots using Microsoft Paint

Paint is still a go-to tool for creating screenshots. Other tools work just as well, and perhaps better.  Photoshop is an obvious choice if licensing allows it. Paint.net is also free, and more powerful than paint.