# Netherhall Archers

This repository contains the source code for the Netherhall Archers club website. The site uses the [Jekyll](https://jekyllrb.com/) tool to build the website from these source files. Indeed, this repo is set up so that any push to the master branch will automatically be built and deployed to the live website. You should therefore be careful when you make changes!

## How can I make changes to the website?

### Ask the website maintainer

Adam Pettigrew is currently the person mainly responsible for maintaining the website. If you have changes that need making and you don't want to do it yourself, send him an email asking for the changes you want. Please be clear and include all details that will be needed!

### Do it yourself

There are three ways to make changes.

#### 1) Become a maintainer

Ask Adam Pettigrew or another maintainer for access to the repository. Only Committee members will be given write access to this repository - if you're not on the committee, follow option 2.

**If you're comfortable with git and the command line:** 
First, [install Jekyll](https://jekyllrb.com/docs/) on your own computer. Make your changes on your own computer, and please ensure that you build and check the website there before you commit to GitHub. Please name all your commits clearly to indicate the changes that you've made.

NB **Do not** make changes to the main trunk. Instead, create your own working branch (named e.g. "john-working") and make all your changes in that branch. Once you've made your changes, create a pull request against the master branch (again, please **do not** simply merge into master). Adam or another admin will review and accept your changes.

**If you want to use the web interface:**
If you only need to make simple changes to the content of pages (rather than to the overall design or structure), you can edit pages directly in the GitHub web interface.

First, you will need to have created a GitHub account (otherwise, you can't be given write access to the repo in the first place). Whenever you're logged in and view a file within the repo, you will be able to edit the text using the edit button (like a pencil) on the webpage.

When you've made your changes, you *must* describe them in the "Commit changes" dialog at the foot of the page, so that other people know what you've done.

You *must* also make sure that you select the "Create a new branch for this commit and start a pull request" option. This allows the admins to review your changes before they are pushed to the live website.

#### 2) Fork the repo

If you're not a Committee member, you can fork the repo to your own account on GitHub. Once you've done that, you can follow the same instructions as above: work locally or via the web interface to make changes to your own version, and submit a pull request once you're finished. Please name all your commits clearly to indicate the changes that you've made.

## How is the site structured?

The repository structure can look intimidating but, in general, you should only need to worry about a few files.

The code for the three main pages is in four files in the main directory: `index.html` (the main home page); `whats-going-on.html` (the "What's going on" page); `getting-started.html` (the "Getting started" page); and `about-us.html` (the "About us" page).

The Jekyll site contains lots of information about how pages work but there are a few key things to understand.

- Each file starts with some metadata, separated from the rest of the page by a line of hyphens. **Do not** touch this area unless you know what you're doing, or you will break things!
- Below that this is the actual content. In most cases, you will see the content that will be shown on the page. You will see HTML code in these files! If you're just changing words on the page, make sure not to change any HTML tags (the text in `<...>`) and you'll be fine.
- Some pages (like the `index.html` page) seem to have no content, and all pages will contain code like `{% include placeholder.html %}`. This is because some content (mostly stuff that's reused on several pages) is in separate files called 'includes', and these can be placed on any page.
- To edit the content of the `index.html` page, you need to open the `_layouts` directory and then the `front.html` file. 
- To edit the content of any 'include', you need to open the `_includes` directory and then the relevant file. (Check carefully if you change any includes - by their nature, they may be reused on several pages, so be sure you've not changed pages other than the one you wanted to.)
