---
title: Workflow for writing for Teams developers
description: What processes to use when writing for teams developers. 
keywords: Teams writers developers platform dev docs
ms.date: 01/09/2019
---
# A day in the life of a writer

This is simply my workflow. Yours might be different, and it will evolve as more people join the team.

## Triage meeting

Once a week, check in with stakeholders and discuss priority for work items in the backlog 
[Dev docs task list](https://domoreexp.visualstudio.com/MSTeams/_backlogs/backlog/Partners%20-%20Dev%20Support/Requirements). Sort items in the backlog by priority, and during discussion identify next steps, particularly Subject matter experts (SMEs). As time allows, start work on the items in the order that they are listed. Set tasks to active if they are going to be worked on in the next period.

## Start a task

1. Take a task off of the backlog, track down and read the development work items if listed, and read up on the relevant sections of the docs as needed to become familiar with the context of the issue.

2. Establish a named conversation in Teams in the [Teams Platform > Documentation](https://teams.microsoft.com/l/channel/19%3a76fedd54f6334ba1b6fb0345b4777ad3%40thread.skype/Documentation?groupId=32e3b156-66b2-4135-9aeb-73295a35a55b&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) Channel, where you will discuss the task with stakeholders and manage the review of the topic.  Title the conversation with the work item number and the title of the task.

3. Describe the task, and ping the SMEs with questions that you need to resolve before you go forward. This step is to make sure that the information that you have in the work item is complete and up to date. It usually is not. The main goal here is to scope the work and identify sources of information. Usually that will be a spec or a scheduled conversation with a SME.

4. If you are interviewing a SME I highly recommend recording the meeting. In this case online meetings in Teams are superior to face to face meetings because you can record audio and screen sharing. If you must meet face to face, use an audio recorder app on your phone to record the conversation, and transcribe the notes as soon as possible after the meeting. The point here is to minimize the time that you take from the SME.

5. Decide where the new information should go in the TOC of the documentation set. This is usually harder than it seems.

## Create a branch to hold your new work

1. Use the Github desktop client to create a new branch off of master in the msteams-platform project.

2. Open Visual Studio Code from the root of your local repo. Click on the files icon in the upper left corner of the ide and confirm that you see the source for the repo displayed in the Explorer window.

3. Use VS.Code to add files, delete files, and edit existing files.

4. Regularly check in your changes by pushing your branch to GitHub. This is done in the desktop GitHub client. Start by committing to your local repo using the button in the lower left corner of the screen. This updates your changes locally on your machine. In the tool bar you should now see an option to "Push Origin". Clicking this will send your changes to the GitHub server that contains all of our branches.

5. Preview your changes on the preview site. It usually takes around 5 min. for the build engine to create a new preview based on your changes. You can view your preview by adding "review" to the beginning of the url for the doc set. When viewing the review version of the doc set there is a drop down at the top of the page that lets you select the branch to preview. You may have to click this several times to get your branch to show up if it is new.

## Merge your changes into the Master

When you are ready to merge your changes back into master it is good practice to have someone else review your changes as a last sanity check. Do this by opening a pull request (PR) in GitHub.  Click on Branch>Create pull request, which will open the browser and send you back to the GitHub website to complete your pull request.

Once your changes have been reviewed and updated as needed, use the GitHub website to manage the merge back into master. Browse to your PR and follow the instructions there.

You should now preview your changes by setting the preview site branch to master. Check for conflicts and issues here before pushing master to live.

>[Note]
>Changes to the doc set will not show up publicly until you push master to live.  Never edit live directly - it should only be updated from master in order to protect from versioning issues.

## Using the publishing platform to push to live

The APEX team provides the excellent tools that we use to publish our documentation sets. They have their own documentation here:
[Docs contributor guide](https://review.docs.microsoft.com/en-us/help/contribute/?branch=master).

The OPS portal allows us to monitor the health of the build system that processes our md files and publishes our finished documentation to the web.
[OPS Portal](https://ops.microsoft.com/#/login). Once you are in the OPS portal, you will want to install a plug-in that allows pushing content from the Master branch to the Live branch. This can be done directly from Github using the command line, but the process is complicated and can result in tangled file histories is care is not taken. The plug-in is less complicated to use and more reliable.

Just in case, the command line replacement for the plug in is:
  git checkout master
  git pull
  git checkout live
  git merge master
  git push