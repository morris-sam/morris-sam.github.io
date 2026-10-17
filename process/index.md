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

## Step 1: Create a GitHub Account

To do this, visit the [GitHub sign up page](https://github.com/signup).

This is a standard sign up page, requiring an email and password, but also a username.

Your username will be public, so ideally choose something that is relevant to you, as this will be part of your website.

Once you have an account, GitHub will open your main profile page, which can be accessed by visiting `https://github.com/{your username}`.

<font size="1">[Back to Table of Contents](#table-of-contents)</font>

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

In the bottom left, next to your profile picture (by default this is a white background with a random pattern), enter a brief description of the changes you made (not in the description box, right above it).

In the bottom left corner, click the button labeled "Commit {number} files to **main**". On the top right, there will now be a button to `Push to Origin`, which will update your main GitHub repository with the files you added locally.

Back on `https://github.com/{your username}/{your username}.github.io`, you'll now see all the files you downloaded from the Minimal page.

In the `Actions` tab of your repository, there will be a workflow called "pages build and deployment".

The chart below describes the meaning of the symbols to the left of these words.

| Color & Symbol | Meaning                                                          |
|:---------------|:-----------------------------------------------------------------|
| Red X          | Something went wrong, likely a file not being imported correctly |
| Yellow Loading | The website is still being loaded, nothing's wrong               |
| Green Check    | Your website is up, nothing's wrong                              |

Once the icon is a green check, your website should be up and running! Visit `{your username}.github.io` to test it.