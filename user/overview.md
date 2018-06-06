---
title: Adobe Docs contributor guide overview
description: The guide describes how you can contribute to the Adobe documentation site.
---

# Adobe Docs contributor guide overview

IMPORTANT: COPIED FROM MICROSOFT - REPLACE CONTENTS WITH OUR OWN

<https://docs.microsoft.com/en-us/contribute/>

Welcome to the Adobe Docs Contributor Guide!

Some of our Adobe documentation is open source, hosted on GitHub. You can contribute to this documentation in a number of ways, from making quick edits to existing documents to submitting entire articles, complete with assets. This open source model streamlines and improves communication between the product engineers, the content teams, and our customers. 

> [!IMPORTANT]
> All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](link) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Code of Conduct FAQ](link).<br>
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.adobe.com Terms of Use](link). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.

## Quick edits to existing documents

Quick edits streamline the process to report and fix small errors and omissions in documents. While you can create issues to report mistakes, it's faster and easier to create a pull request (PR) to fix the issue. If an article displays an edit button as shown in the following figure, you can make a quick fix yourself. 

1. Click the **Edit** button to go to the source file on GitHub.<br>
![Location of the Edit link](assets/edit-article.png)<br>
1. Click the pencil icon, shown in the following figure to edit the article.<br>
> [!NOTE]
> If the pencil icon is grayed out, you need to login to your GitHub account, or create a new account. Make your changes in the web editor. You can click the **Preview changes** tab to check formatting of your change.<br>
![Location of the pencil icon](assets/edit-icon.png)<br>
1. Once you have made your changes, scroll to the bottom of the page. Enter a title and description for your PR and click **Propose file change** as shown in the following figure:<br>
![proposing your change](assets/submit-pull-request.png)<br>

That's it! Content team members will review and merge your PR. You may get some feedback requesting changes if you made larger changes.

The GitHub editing UI responds to your permissions on the repository. The preceding images are accurate for contributors that do not have write permissions to the target repository. GitHub automatically creates a fork of the target repository in your account. If you have write access to the target repository, GitHub creates a new branch in the target repo. The branch name has the form **\<GitHubId\>-patch-n** using your GitHub ID, and a numeric identifier for the patch branch.

We use PRs for all changes, even for contributors that have write access. Most repositories have the `master` branch protected so that updates must be submitted as PRs.

The in-browser editing experience is best for minor or infrequent changes. If you make large contributions, or use advanced Git features (such as branch management or advanced merge conflict resolution), we recommend that you [fork the repo and work locally](how-to-write-workflows-major.md).

## Review open PRs

You can read new topics before they are published by checking the currently open PRs. Reviews follow the [GitHub flow](https://guides.github.com/introduction/flow/) process. You can see proposed updates or new articles in public repositories. Review them and add your comments. Look at any of our docs repositories, and check the open pull requests (PRs) for areas that interest you. Community feedback on proposed updates helps the entire community.

## Create quality issues

Our docs are a continuous work in progress. Good issues help us focus our efforts on the highest priorities for the community. The more detail you can provide, the more helpful the issue. Tell us what information you sought. Tell us the search terms you used. If you can't get started, tell us how you want to start exploring unfamiliar technology.

Issues start the conversation about what's needed. The content team will respond to these issues with ideas for what we can add, and ask for your opinions. When we create a draft, we'll ask you to [review the PR](#review-open-prs).

## Get more involved

Other topics help you get started productively contributing to Microsoft Docs. They explain working with GitHub repositories, Markdown tools, and extensions used in the Adobe Docs platform.
