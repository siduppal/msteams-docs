---
title: Tools for writing for Teams developers
description: What tools to use when writing for teams developers. 
keywords: Teams writers developers tools platform dev docs
ms.date: 01/09/2019
---
# Setting up your tools

These are the tools I use. YMMV.

## Markdown

All of our source documents are written in MarkDown, a simple text format that has the extension md.  Specifically we use the GitHub flavor of MD, as I recall.  You can find the answer to any question you might have on how to use MD with a simple web search. Try to keep things as simple as possible - no tables within tables, no nested lists, that sort of thing. It makes your writing much easier to read, and limits build issues.

## GitHub

First of all, you need to get a source repository set up on your local machine so you can have access to those markdown files.  We use GitHub to manage all source documents, which in turn uses git.
When I started I spent a couple of hours discussing git with someone who knew it really well, and that conversation paid off. I did not find it obvious or intuitive at first because it used odd terms and did not work like other tools I had experience with. Now that I understand it I'd be reluctant to use anything else.

## GitHub Desktop

I really like the GitHub Desktop tool as a way to clone, branch, and update source documents. It is less error prone than the git command line, and is much more self documenting.
Install it from: https://desktop.github.com/

If you have access to GitHub on the web and can access [MicrosoftDocs/msteams-docs](https://github.com/MicrosoftDocs/msteams-docs) you should be able to log into the client and get access to the same repos with the same log in credentials.

Your first step is to clone the MicrosoftDocs/msteams-docs repo to your local machine. Since I'm already signed in and have a local repo, I can't walk through the steps without messing up this writing session. As I recall, it was pretty obvious. You want to File>Clone Repository, and in the filter box in the Clone a repository dialog, enter `msteams-docs'. Take a moment to set up your local path - this is where all your local copies of all files will be stored.

The files stored on your local machine are now a copy of everything that is in the master branch of msteams-docs at this particular moment in time.  If you edit one of these files and check it in locally, and then 