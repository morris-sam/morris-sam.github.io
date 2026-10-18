---
layout: default
---

# Website Process

These steps will describe how this website was created, and explain how you can make a website like this of your own.
I would recommend reading through the entire documentation once before attempting this to help avoid confusion.

## Table of Contents:
1. [Create a GitHub account](#step-1-create-a-github-account)
2. [Create the Website Repository](#step-2-create-a-website-repository)
3. [Install and set up GitHub Desktop](#step-3-install-and-set-up-github-desktop)
4. [Download, Install, and Test the Minimal Theme](#step-4-download-install-and-test-the-minimal-theme)
5. [Basic Customization](#step-5-basic-customization)

## Step 1: Create a GitHub Account

To do this, visit the [GitHub sign up page](https://github.com/signup).

This is a standard sign up page, requiring an email and password, but also a username.

Your username will be public, so ideally choose something that is relevant to you, as this will be part of your website.

Once you have an account, GitHub will open your main profile page, which can be accessed by visiting `https://github.com/{your username}`.

## Step 2: Create a Website Repository

> Definition: "A repository is the most basic element of GitHub. It's a place where you can store your code, your files, and each file's revision history. Repositories can have multiple collaborators and can be either public or private." [Source](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories)

On the top bar of your GitHub page, there will be a tab called `Repositories`. This will list repositories you own or have access to.

Click the button on the top left labeled `New`, and enter your "Repository name" as `{your username}.github.io`, then click `Create repository`.

**The format of the repository name is important, as the website will not work otherwise.**

## Step 3: Install and set up GitHub Desktop

GitHub Desktop is a local version of GitHub for just your computer, downloadable from the [GitHub Desktop website](https://desktop.github.com/download/).

Once you have GitHub Desktop installed, opened, and you're signed in, you'll need to bring in your website repository.

You'll see your website repository on the side of teh GitHub Desktop menu.

Click it, and choose to clone it to your computer, as well as where in your computer to store it.

GitHub Desktop will now show you a list of your changed files on the left, and a message saying `No Local Changes` on the right.

## Step 4: Download, Install, and Test the Minimal Theme

This website was not created on its own completely from scratch. It was created using a theme called "Minimal", which can be found [here](https://github.com/pages-themes/minimal).

To use the "Minimal" theme, open their repository and look for a green button labeled `<> Code`.

After opening this, click the button labeled `Download ZIP`. This will download a folder to your computer, containing everything you need for your website.

Open up the cloned repository folder you made in the last step, and move the contents of the downloaded folder (not the entire folder itself) into that folder.

Once this is done, go back to GitHub Desktop, and you'll now see that there are changed files. Make sure all the boxes in the list are checked.

In the bottom left, in the section labeled "Summary", enter a brief description of the changes you made (not in the "Description" box, right above it).

In the bottom left corner, click the button labeled "Commit {number} files to **main**". On the top right, the button that was labeled `Fetch origin` will now be labeled `Push origin`, which will update your main GitHub repository with the files you added locally.

Back on `https://github.com/{your username}/{your username}.github.io`, you'll now see all the files you downloaded from the Minimal page.

In the `Actions` tab of your repository, there will be a workflow called "pages build and deployment".

The chart below describes the meaning of the symbols to the left of these words.

| Color & Symbol | Meaning                                                          |
|:---------------|:-----------------------------------------------------------------|
| Red X          | Something went wrong, likely a file not being imported correctly |
| Yellow Loading | The website is still being loaded, nothing's wrong               |
| Green Check    | Your website is up, nothing's wrong                              |

Once the icon is a green check, your website should be up and running! Visit `{your username}.github.io` to test it.

## Step 5: Basic Customization

### Name, Title, and Image

In the file labeled `_config.yml`, there are settings you can change that will alter the look of your website.

**Name -** The setting labeled "title:" is where you can input your name, or whatever you want to have at the top of the page.

**Title -** The setting labeled "description:" is where you can input a description of yourself, usually a title or brief description.

**Image -** The setting labeled "logo:" is a path to where a profile picture of you is stored. By default, this is `/assets/img/logo.png`, but it can be changed based on your preferences.

In your files, there will be a folder called "assets", and a folder within that called "img". If you choose to replace the image that is in this file, make sure to keep the name consistent between your config setting and the image (`logo.png` and `logo.png` by default).

**Bonus -** The setting labeled "show_downloads:" can be set to `false`, as you usually won't have something for people viewing your site to immediately download.

### Contents on the right

The basis of this section is stored in a file called `index.md`. This file uses the `.md` extension, which can use Markdown symbols for format editing. 

A list of these can be found at <https://www.markdownguide.org/basic-syntax/>, as well as some best practices when using Markdown.

After making changes to this file, you can push it through GitHub Desktop onto GitHub, which pushes it live to your site after a couple of minutes.

