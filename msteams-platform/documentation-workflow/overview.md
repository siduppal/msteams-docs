---
title: How to write for teams developers
description: What processes to use when writing for teams developers. 
keywords: Teams writers developers platform dev docs
ms.date: 01/09/2019
---
# Writing for developers who use the Teams platform

Developing for Teams is all about writing *Teams apps*. If you need to discuss other topics, such as using the product, or selling the product, there are better places for you to put your content, where it will be seen by the right people.
This content is for developers, people who have been tasked with extending the Teams platform, either as third party developers or as internal line of business developers.

This audience needs:

- Short, succinct topics that explain what teams apps are, and how to use them to do specific tasks.
- Comprehensive documentation that covers every feature of the platform. This is the first place they will look.
- Simple and direct writing. Don't assume that your reader is as skilled in the English language as you are.
- Documents that share a common style. To achieve this across all Microsoft properties follow the Microsoft and Office Style guides.

## Microsoft and Office provide writing style guides

- [Microsoft Writing Style Guide](https://worldready.cloudapp.net/Styleguide/Read?id=2700&topicid=29021)
- [Office Style Guide](https://aka.ms/officestyleguide)

## The Teams Platform Documentation set

All of the Teams Platform documentation (our developer docs for writing teams apps) is maintained in a single GitHub repository:

[MicrosoftDocs/msteams-docs](https://github.com/MicrosoftDocs/msteams-docs)

Anyone can clone the documentation set and work on revisions for later integration back into the master branch, however if you want to work more closely with the doc set and use the preview functionality that our build system provides you will need to have an internal Microsoft Account, and be added as a contributor to the repo. At the moment Bill Bliss is the administrator for this.

Typically we use personal GitHub credentials when working with the repository, so you will need to have your own GitHub credentials before requesting access from Bill.

This GitHub page is the place where we manage issues and pull requests, but it is rarely used to create branches and manage files while writing. There are other tools that work better for those tasks.

## Other Teams-related documentation sets

The Teams developer documentation is just part of the Teams documentation ecosystem. There are also documentation sets for every-day users of the product, as well as for IT professionals who need to set up and maintain the product in an enterprise environment. These doc sets are maintained by other groups, but you may need to work with them to communicate clearly.

Teams apps also depend on technologies that are not directly developed by the Teams group. These technologies include:

- **Bot Framework**, which is now owned by the Azure team. Teams uses the Bot Framework, and our docs need to be kept in sync with theirs.
- **Microsoft Graph**, which is an external documentation set that Bill Bliss has been maintaining.

## Get started writing:

- Set up your writing environment [Tools for writing](`/documentation-workflow/tools-for-writing)

 - The day to day process of writing a topic [Writing workflow](`/documentation-workflow/writing-workflow)