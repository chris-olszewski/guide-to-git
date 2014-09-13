title: Git-ing To Know The Basics
author:
  name: Chris Olszewski
outputs: slides.html
controls: true
theme: jdan/cleaver-retro

--

# Git-ing To Know The Basics
## A simple guide to git and GitHub

--

### What's git?

-**Git:** a version control system for source code specifically created for collaborative coding. It keeps track of the additions and deletions of each line of code in every file checked in the repository.
-**GitHub:** a website which hosts the git repository and provides project management tools as well.

--

### Git Specific Vocabulary

**Repository:** Project that git keeps track of. Completely contained in a single folder.
**Branch:** An alternative version of the repository. Usually used for adding features.
**Commit:** A single update to a branch of a repository.

--

### Git-ing Started

- `mkdir repo`
- `cd repo`
- `git init`

These three commands simply make a folder, move into the folder and create a git repository in the folder. Simple as that.

--

### Argh, Look at all these file I have! Things are git-ing out of hand

Okay, we have these files now. We should start keeping track of them, but how do we know what git is keeping track of?
`git status` comes to the rescue! This command reveals all files that have been changed since the last commit.
By default all changed files are untracked or will not be part of the next commit. Adding these files to the next commit is as easy as `git add path/to/file`

--

### Commits continued

The files we just added are now ready to be bundled up into a commit! `git commit -m "My first commit"`
This saves the changes to the git repository. Each commit is a separate version of the repo.

--

### Chris got bored, these are all the commands you'll need to git started

- `mkdir repo`
- `cd repo`
- `git init`
- `git add path/to/file`
- `git commit -m "Initial commit"`
- `git push origin master`

--

### Wait that's some bad git-iquette! You shouldn't be pushing to master!

- Before you start changing files `git branch new-branch`
- Change files
- `git add .` (This is shorthand for adding all changed files to the commit)
- `git commit -m "Commit for this branch"
- `git push origin new-branch`

--

### Now let's turn to GitHub

- Go to the repo homepage and click on the branches tab
- Find your branch and create click compare & create pull request
- Usually a small description of which feature you are adding is nice
- (Optional) Wait until somebody else reviews the changed code before you merge the pull request

--

### Crap, we're git-ing errors

It's okay though, we can easily work through this.
- Go back to your nice pretty command line interface with git
- Switch to the branch you're trying to merge `git checkout problem-branch`
- Pull the master branch from the origin repo `git pull origin master`
- You should see something along the lines of "Warning, conflict with auto-merging"
- Check what's up by running `git status` this should list any problem files

--

### Errors (cont)

- Check out these listed files in your text editor
- There should be a line similar to ">>>>>>>>>"
- Delete this line and all lines around this that look problematic. You should know what you were trying to change, keep your changes in and make sure this new file works fine.

--

### Questions?

Please feel free to ask me any questions. Git is an insanely powerful tool that will let you contribute to both private and open source projects easily.
