---
title: Set up Git repository locally
description: This article provides guidance to create your local Git repository and contribute to documentation, including the forking and cloning process.
---
# Set up Git repository locally for documentation

This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Adobe documentation. Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.

You run these one-time setup activities to get started contributing:
<<<<<<< HEAD
> [!div class="checklist"]
> * Determine the appropriate repository
> * Fork the repository to your GitHub account
> * Choose a local folder for the cloned files
> * Clone the repository to your local machine
> * Configure the upstream remote value

> [!IMPORTANT]
> If you're making only minor changes to an article, you *do not* need to complete the steps in this article. You can simply click the Edit icon and make text edits in your browser.
=======

* Determine the appropriate repository
* Fork the repository to your GitHub account
* Choose a local folder for the cloned files
* Clone the repository to your local machine
* Configure the upstream remote value

> [!NOTE]
> Follow these steps only to make major changes to existing article or create new articles. If you're making only minor changes to an article, you *do not* need to complete the steps in this article. Just click the Edit option to edit the article directory in your browser.
>>>>>>> cf485c226705d478fc1697eb394f341411d2749b
>

## Overview

<<<<<<< HEAD
To contribute to Adobe documentation, you first need to fork the appropriate repository into your own GitHub account so that you have read/write permissions. Then, you can can make and edit Markdown files locally by cloning the corresponding documentation repository. Then you use pull requests to merge (submit) changes into the read-only central shared repository.

## Determine the repository

Adobe Experience Cloud documentation resides in several different repositories at [github.com](https://www.github.com).

1. If you are unsure of which repository to use, then visit the article using your web browser. Select the **Edit** link (pencil icon) on the upper right of the article. (If you don't see an Edit link, that content is not yet available in GitHub.)
=======
To contribute to Adobe documentation, you can make and edit Markdown files locally by cloning the corresponding documentation repository. You fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes. Then you use pull requests to merge changes into the read-only central shared repository.

![GitHub Triangle](/assets/git-and-github-initial-setup.png)

If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## Determine the repository

Documentation hosted at [docs.adobe.com](https://docs.adobe.com) resides in several different repositories at [github.com](https://www.github.com).
>>>>>>> cf485c226705d478fc1697eb394f341411d2749b

1. If you are unsure of which repository to use, then visit the article on docs.adobe.com using your web browser. Select the **Edit** link (pencil icon) on the upper right of the article.

   ![Click Edit to determine the repo and file location.](assets/edit-article.png)

<<<<<<< HEAD
=======
1. That link takes you to github.com location for the corresponding Markdown file in the appropriate repository. Note the URL to view the repository name.

   ![Notice the URL to determine the repository location.](media/public-repo.png)<br>

>>>>>>> cf485c226705d478fc1697eb394f341411d2749b
## Fork the repository

Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.

<<<<<<< HEAD
A personal fork is required since all main documentation repositories provide read-only access, which means you cannot make changes directly on content in the repositories. To make changes, you must submit a pull request (PR) from your fork into the main repository. To facilitate this process, you first need your own copy of the repository, in which you have write access. A GitHub *fork* serves that purpose.

1. Go to the main repository's GitHub page and click the **Fork** button on the upper right.

2. If you are prompted, select your GitHub account tile as the destination where the fork should be created. This prompt creates a copy of the repository within your GitHub account, known as a fork.
=======
A personal fork is required since all main documentation repositories provide read-only access, which means you cannot make changes directly on content in the repositories. To make changes, you must submit a pull request from your fork into the main repository. To facilitate this process, you first need your own copy of the repository, in which you have write access. A GitHub *fork* serves that purpose.

1. Go to the main repository's GitHub page and click the **Fork** button on the upper right.

   ![GitHub profile example](./media/contribute-get-started-setup-local/fork.png)
   
1. If you are prompted, select your GitHub account tile as the destination where the fork should be created. This prompt creates a copy of the repository within your GitHub account, known as a fork.
>>>>>>> cf485c226705d478fc1697eb394f341411d2749b

## Choose a local folder

Make a local folder to hold a copy of the repository locally. Some of the repositories can be large. Choose a location with available disk space.

1. Choose a folder name should be easy for you to remember and type. For example, consider making a folder in your user profile directory `~/Documents/docs/`

   > [!NOTE]
   > Avoid choosing a local folder path that is nested inside of another git repository folder location. While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.
   
1. Run the **clone** command to pull a copy of the repository (your fork) down to your computer on the current directory.

### Authenticate by using Git Credential Manager

1. Run the **clone** command, by providing the repository name. Cloning downloads (clone) the forked repository on your local computer. 

    > [!NOTE]
    > You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:
    >
    > ![Clone or download](./media/contribute-get-started-setup-local/clone-or-download.png)

    Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork. Otherwise, you cannot contribute changes. Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.

The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk. A new folder is made within the current folder. It may take a few minutes, depending on the repository size. You can explore the folder to see the structure once it is finished.

## Configure remote upstream

After cloning the repository, set up a read-only remote connection to the main repository named **upstream**. You use the upstream URL to keep your local repository in sync with the latest changes made by others. The **git remote** command is used to set the configuration value. You use the **fetch** command to refresh the branch info from the upstream repository.
