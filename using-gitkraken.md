## Working on the website using Gitkraken

Although there's a lot of words on this page, this is to make sure everyone understands and can contribute to the website, rather than because it's particularly hard! Once you're set up (which will explain most of the jargon in this list!), the process of making a change is:

- pull any changes from GitHub since you last worked on the website;
- make your changes using Notepad (or your preferred text editor - **NOT** Microsoft Word!);
- commit your changes;
- push your changes to GitHub;
- create a pull request to get your changes approved.


## Getting started with Gitkraken

[Gitkraken](https://www.gitkraken.com/) is available for Windows, macOS and Linux. It's free to use for public repositories like this, and gives you a nice user interface that helps to connect your computer to GitHub, and to keep your files in sync with everyone else's. They have [lots of nice tutorials](https://www.gitkraken.com/learn/git/tutorials), including videos, to help understand some of the concepts. (You don't have the understand the concepts to edit the website, though! Just follow the instructions and all should be well.)

I recommend downloading [this Gitkraken cheat sheet](https://www.gitkraken.com/downloads/gitkraken-for-github-cheat-sheet-v3.pdf) (PDF), which gives you instructions for several of the steps below.

### Connect to GitHub

First, you need to connect Gitkraken to your GitHub account so that it can copy this repository to your local computer. Follow the instructions in the cheat sheet above to do this.

### Clone the repository

Second, you need to copy the repository. This is called 'cloning' the 'repo'. Again, follow the instructions in the cheat sheet. You will need to pick a suitable folder on your computer to store the repo - pick something you'll be able to find easily!

### Work in your own branch

Git lets everyone have their separate 'branch' to work in, which keeps everyone's edits separate while letting them be merged together when needed to update the live website. You only need to create a branch once. To do this, click the 'Branch' button in the Gitkraken toolbar at the top of the window. Name your branch something like 'john-pettigrew-working' and save. If you have this branch selected when you work, Gitkraken will track all your edits there.

## Important Gitkraken features you'll need

Gitkraken can do a lot, probably much more than you'll need. However, there are only a few things you really need to know.

The left-hand side has a bar with information about the branches and tags in the repository. You can mostly ignore this.

The right-hand side bar will show you the files that were changed in any commit (when you select one in the main part of the window). If you select a file from this list, Gitkraken will show the contents of the file in the main part of the window, highlighting anything that was added or deleted as part of this specific commit. This is also the area you'll use when making your own commits (see below).

The middle of the window shows the history of the project, with all the different branches and the commits within each of them. If you double-click on a branch or a specific commit, Gitkraken will change the files on your computer so that they match that branch and commit. This can be very useful, but also dangerous if you work in the wrong branch or (worse) on an old commit! When you start work, make sure you have your own branch selected.

The toolbar at the top of the window has two key buttons:

- *Pull*: clicking this will 'pull' any changes from GitHub that have been made since you last synchronised. Obviously, it's good to work on the latest version of the site!
- *Push*: clicking this will 'push' any changes you have made on your computer up to GitHub so that other people can see them.

### Creating a commit

When you make changes to files on your computer, Gitkraken will keep an eye on exactly what changes you make. Once you're happy that you have a good version, you should 'commit' these changes. When you commit, you're saving a record of the changes to git locally, which you can later push to the GitHub website and share with other people.

Once you've made some changes, you'll see at the top of the right-hand side the note '2 changes in your working directory' (or however many files you've changed). Click 'View changes' or use the shortcut Ctrl-Shift-S. You are now ready to create your commit.

- Click the green 'Stage all changes' button, which moves your changes from the top box to the middle one. (You can choose to commit only some changes if you want.)
- Type a message into the 'Commit message' box at the bottom that explains what you've done in these changes.
- Click the green 'Commit changes to x files' button at the bottom.

### Pushing your changes to GitHub

To synchronise your changes with GitHub, click the 'Push' button in the toolbar. You may be asked to pull upstream changes before you can push your own. If someone else has edited a file while you've been working, you may get a message about clashing edits (e.g. if you've both changed the same word, git can't know whose version to use). If you have any problems resolving clashes, you can ask Adam or John. However, this will probably be very rare!

### Creating a pull request

When you've made some changes you're happy with, you'll want those changes applied to the live site. For safety, you should always ask someone else to check your work before it goes live. This is what a 'pull request' does - ask ('request') someone to 'pull' your changes into the main branch of the project.

To create a pull request, right-click on your branch in Gitkraken (either in the left-hand bar or on the) and choose the menu entry that starts 'Start a pull request...', which is about half-way down.

The dialog that opens is a bit scary, but you can ignore most of it. You'll see GitHub selected at the top, with 'From' and 'To' boxes underneath. These will be pre-completed with the right values, so don't change them. You do, however, need to give your pull request a title and a description. These needn't be long - just enough to let people know what you're asking to be done.

You *must* add a reviewer for your pull request. This is the person who'll be asked initially to accept the request. Pick Adam, who is known as 'blurryhumanface' on GitHub. You can ignore the rest of the boxes.

Then, click the green button labelled 'Create Pull Request'.
