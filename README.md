# Netherhall Archers

This repository contains the source code for the Netherhall Archers club website. The site uses the [Jekyll](https://jekyllrb.com/) tool to build the website from these source files. Indeed, this repo is set up so that any push to the master branch will automatically be built and deployed to the live website. You should therefore be careful when you make changes!

## How can I make changes to the website?

### Ask the website maintainer

It's always possible to ask one of the people we're responsible for the site to make changes for you. Adam Pettigrew is currently the main person responsible for maintaining the website. If you have changes that need making and you don't want to do it yourself, send him an email asking for the changes you want (use the committee email address if you don't have his personal email). Please be clear and include all details that will be needed!

### Do it yourself

You're very welcome to have access to make changes yourself - although for obvious reasons, only club members (and probably only committee members) will actually be given write acecss. There are three steps you need to do to make changes.

#### 1) Become a maintainer

Like most websites, you need to create an account to use GitHub. Once you have an account, ask Adam Pettigrew or another maintainer for access to this repository.

#### 2) Make your changes to the site

**If you prefer editing files on your computer:**
This is probably the best option for most people. You will need to copy the files from the GitHub repository (where the source code is kept safe), edit the files using a text editor (e.g. Notepad) and then copy your files back to GitHub. Fortunately, there's some neat software to make this easier. I recommend downloading and using [Gitkraken](https://www.gitkraken.com/). Once you've installed Gitkraken, follow [these steps](using-gitkraken.md) to use it.

**If you prefer using web interface:**
If you only need to make simple changes to the content of pages that already exist (rather than adding pages or changing the overall design or structure of the site), you can edit pages directly in the GitHub web interface. When you've made your changes, *please* describe them in the "Commit changes" dialog at the foot of the page, so that other people know what you've done. *Please* also make sure that you select the "Create a new branch for this commit and start a pull request" option. This allows the admins to review your changes before they are pushed to the live website.

**If prefer using the command line:**
First, install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Jekyll](https://jekyllrb.com/docs/) on your own computer. If you clone the repo to your computer using git, you can edit the site locally using your preferred text editor. Running `bundle exec jekyll serve` will allow you to view the edited version in your browser and make sure you're happy with it before pushing your changes back up to GitHub.

#### 3) Get your changes approved

Whichever option you follow, you should follow these principles.

**Work in your own branch:**
The main value of git is storing a detailed history of a project, so that it's always possible to see which changes have been made - and so fix any mistakes! To help keep things organised, this history can be organised into a number of different 'branches'. This lets each person work on their own branch, without affecting anyone else's code, and then to merge this back into the main trunk (from where the live website is built).

**Name your commits sensibly:**
Git can store changes to several files into a single 'commit', which is when you save your changes back to GitHub. It really helps people know what you've been doing if you put useful information into the name of your commit. For example, if you've added a new post, you might name the commit 'Added a new post'!

**Ask to get your changes applied to the live site:**
The main site is built from the main branch of the repository. However, as noted above, you should work in your own branch (for safety). To get your changes applied to the main branch, you need to ask another admin to do this, via a so-called [pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request). Different software provides different ways to do this, but whichever you choose, you can think of it as 'asking for my changes to be be applied to the live site'. As with a commit, please name your pull requests in an informative way.

## How is the site structured?

The repository structure can look intimidating but, in general, you should only need to worry about a few files.

The code for the three main pages is in four files in the main directory: `index.html` (the main home page); `whats-going-on.html` (the "What's going on" page); `getting-started.html` (the "Getting started" page); and `about-us.html` (the "About us" page).

The Jekyll site contains lots of information about how pages work but there are a few key things to understand.

- Each file starts with some metadata, separated from the rest of the page by a line of hyphens. **Do not** touch this area unless you know what you're doing, or you will break things!
- Below that this is the actual content. In most cases, you will see the content that will be shown on the page. You will see HTML code in these files! If you're just changing words on the page, make sure not to change any HTML tags (the text in `<...>`) and you'll be fine.
- Some pages (like the `index.html` page) seem to have no content, and all pages will contain code like `{% include placeholder.html %}`. This is because some content (mostly stuff that's reused on several pages) is in separate files called 'includes', and these can be placed on any page.
- To edit the content of the `index.html` page, you need to open the `_layouts` directory and then the `front.html` file.
- To edit the content of any 'include', you need to open the `_includes` directory and then the relevant file. (Check carefully if you change any includes - by their nature, they may be reused on several pages, so be sure you've not changed pages other than the one you wanted to.)
