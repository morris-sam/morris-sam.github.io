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
4. [Installing VSCode](#step-4-installing-vscode)
5. [Download, Install, and Test the Minimal Theme](#step-5-download-install-and-test-the-minimal-theme)
6. [Basic Customization](#step-6-basic-customization)
7. [My Personal Changes](#step-7-my-personal-changes)

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

## Step 4: Installing VSCode

Your computer's default file editing software may be great, but if it's not, one is going to be needed.

VSCode is a free software that allows for file editing, among other features. 

It can be downloaded from [the VSCode website](https://code.visualstudio.com), and used in the following steps.

## Step 5: Download, Install, and Test the Minimal Theme

This website was not created on its own completely from scratch. It was created using a theme called "Minimal", which can be found [on the Minimal GitHub page](https://github.com/pages-themes/minimal).

To use the "Minimal" theme, open their repository and look for a green button labeled `<> Code`.

After opening this, click the button labeled `Download ZIP`. This will download a folder to your computer, containing everything you need for your website.

Open up the cloned repository folder you made in the last step, and move the contents of the downloaded folder (not the entire folder itself) into that folder.

Once this is done, go back to GitHub Desktop, and you'll now see that there are changed files. Make sure all the boxes in the list are checked.

In the bottom left, in the section labeled `Summary`, enter a brief description of the changes you made (not in the big `Description` box, the smaller one right above it).

In the bottom left corner, click the button labeled `Commit {number} files to main`. This will execute a "commit", or change, to your repository.

On the top right, the button that was labeled `Fetch origin` will now be labeled `Push origin`, which will update your main GitHub repository with the files from your commit.

Back on `https://github.com/{your username}/{your username}.github.io`, you'll now see all the files you downloaded from the Minimal page.

In the `Actions` tab of your repository, there will be a workflow called `pages build and deployment`.

The chart below describes the meaning of the symbols to the left of these words.

| Color & Symbol | Meaning                                                          |
|:---------------|:-----------------------------------------------------------------|
| Red X          | Something went wrong, likely a file not being imported correctly |
| Yellow Loading | The website is still being loaded, nothing's wrong               |
| Green Check    | Your website is up, nothing's wrong                              |

Once the icon is a green check, your website should be up and running! Visit `{your username}.github.io` to test it.

## Step 6: Basic Customization

On GitHub Desktop, in `Settings > Integrations`, change the setting for `External Editor` to whatever you're using as your text editor.

Navigate to `Repository > Open in {integration}`, and your website files will be opened in your selected editor.

### Name, Title, and Image

In the file labeled `_config.yml`, there are settings you can change that will alter the look of your website.

**Name -** The setting labeled `title` is where you can input your name, or whatever you want to have at the top of the page.

**Title -** The setting labeled `description` is where you can input a description of yourself, usually a title or brief description.

**Image -** The setting labeled `logo` is a path to where a profile picture of you is stored. By default, this is `/assets/img/logo.png`, but it can be changed based on your preferences.

In your files, there will be a folder called `assets`, and a folder within that called `img`. If you choose to replace the image that is in this file, make sure to keep the name consistent between your config setting and the image (`logo.png` and `logo.png` by default).

**Bonus -** The setting labeled `show_downloads` can be set to `false`, as you usually won't have something for people viewing your site to immediately download.

### Contents on the right

The basis of this section is stored in a file called `index.md`. This file uses the `.md` extension, which means the file is read in Markdown format.

A list of Markdown formatting symbols and best practices can be found at [https://www.markdownguide.org/basic-syntax/](https://www.markdownguide.org/basic-syntax/).

After making changes to this file and saving it to your computer, you'll see these changes on GitHub Desktop.

From here, you can push it nto GitHub, which pushes it live to your site after a couple of minutes.

## Step 7: My Personal Changes

Due to personal preference, I changed a few of the settings and made some changes to the underlying functionality of this repository. Feel free to do them also.

### File Editing Software

Instead of VSCode, I used [IntelliJ IDEA](https://www.jetbrains.com/idea/), which is a paid software used in software development.

No steps are different between setting up VSCode or IntelliJ.

### Profile Settings

#### Email Settings

One of the things GitHub does by default is it will attach your username and email address to any commits you make. As a personal issue, I don't want to have my email address available to anyone that looks at my commits.

In your profile settings, go to `Access > Emails`, and enable `Keep my email addresses private` and `Block command line pushes that expose my email`. These won't affect previous commits, only future ones.

#### Authentication Settings

Since your GitHub account is the configuration method for your website, keeping it secure is a **must**.

In your profile settings, go to `Access > Password and authentication`, and under `Two-factor authentication`, you can have four different methods of authentication in case someone gets your password.

### Repository

#### Settings

In your repository, there are some buttons at the top that can access different features (such as "Issues" and "Pull requests"). A lot of these cause clutter in your repository, and can be removed.

In the tab labeled `Settings`, navigate to the `General` category, and scroll down to `Features`. These can all be unchecked, and GitHub will remove these tabs.

Back on the main repository page, there is an `About` section on the right. At the top right of this section is a gear icon that can change these settings.

This allows you to change the description, add a website, and add tags to this section. Since this is the repository of a website, the box under `Website` labeled "Use your GitHub Pages website" can be checked, and will link your website here.

While in this section, the options for what to include in the home page (releases, deployments, and packages) can be disabled, as these also aren't used.

Finish by clicking the green `Save changes` button in the bottom right corner.

#### Contents

Some of what we imported from Minimal isn't necessary, and can be deleted in the repository.

1. The `docs` folder. The files within it are primarily used on the Minimal GitHub page, and aren't needed for our purposes.
2. The `README` file. Below your repository files, this is the text box that describes what the repository is. This is the default from Minimal, and isn't ideal if someone visits your repository.
   The `README.md` file contains the contents of this area, and can be altered just like the `index.md` file.

#### Formatting & QOL Changes

To adjust the default layout and theme of the website to create something more customized, I adjusted two different files.
- The `default.html` file, accessed through the `_layouts` folder. This contains instructions for the generic layout of the site, and I made three small changes.
   1. *Removed unnecessary code.* Minimal can change what's listed on the page depending on whether the account is a user or organization, but since this is always a user account, the "organization" options aren't needed. 
   Sections that contain `if site.github.is_project_page` and end with `endif` can be removed, as they're not relevant for us. 
   Lines that contain `if site.github.is_user_page` can also be removed, _as long as_ the corresponding `endif` is removed, and the lines in between are unchanged.
   This should be lines 25-30, 32, and 48-50. 
  2. *Added a link to this subpage.* Links can be nested in text, so I added a line that, when clicked, opens this subpage on the process.
  3. *Added a "last updated" indicator.* GitHub Pages has some variables built into it, such as the `site.github.is_project_page` used above. Three of them are used to make this line work, all obtained from the [Jekyll GitHub page](https://github.com/jekyll/github-metadata/blob/main/docs/site.github.md).
  - `site.time` This gets the current time (at least when the current version of the site was published), and formats it in [Strftime](https://strftime.net). In my `_config.yml` file, I added a variable for my `timezone` as `America/Los Angeles`, as it would default to GMT.
  - `site.github.repository_url` This gets the link to the repository the site is hosted from, involving no change in moving it from one account to another. This was also used for linking this subpage.
  - `site.github.build_revision` This returns a hash that corresponds to the current version of the repository. Using this will link to the changes made in the last commit.
- The `jekyll-theme-minimal.scss` file, accessed through the `_sass` folder. This defines the general theme of the site, including measurements for how wide certain sections are. In this, I adjusted four measurements:
  1. On line 76, I adjusted the `pre > padding` measurement from `8px 15px` to `8px 10px`.
  2. On line 122, I adjusted the `header > width` measurement from `270px` to `310px`.
  3. On line 206, I adjusted the `footer > width` measurement from `270px` to `310px`.
  4. On line 268, I adjusted the `body > padding` measurement from `15px` to `10px`.
