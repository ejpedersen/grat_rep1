# Git Basics

## Software

Atom: atom.io

*Atom allows editing and real-time updating of HTML (and other formatted) previews. It is also integrated with Git and GitHub, so you can easily update the repository as you make changes.*

## Workflow

This link has information on workflow in GitHub, which should apply to Git repositories in general:

https://guides.github.com/introduction/flow/

The site does better than I can at explaining this, but I am paraphrasing it for my own edification. I am also emphasizing the aspects relevant to managing this project. People use Git for managing massive projects with large teams (e.g., developing video games), so several of the features are designed to solve problems we probably won't encounter.

### Repositories

A repository is just a folder structure that contains everything relevant to your project. GitHub is just a hosting site for Git repositories (it's basically a fancy Dropbox). These repositories can be hosted on other sites (e.g., Bitbucket) or on private networks.

When working on a project, you clone the repository on GitHub to your local drive. You make your changes locally and then, when satisfied with your changes, update the remote repository on GitHub (see 'Commits & Pushes' below).

### Branches

For our purposes, we'll be working with one primary branch, which is the 'Master Branch'. The Master Branch will become the stable, functioning version of whatever project we're working on. If we worked out a stable version of this JATOS structure and later decided we wanted a massive overhaul, we could create another branch to work on that overhaul while the Master Branch remained functional. This probably won't happen, so we don't have to worry about branching.

### Commits & Pushes

This is the bread and butter of what we'll need to be comfortable with for this project.

A lot of tutorials separate `add` and `commit`, but several programmers treat them as one in the same. When working on a project in Git, you will have a clone of the repository (i.e., folder structure) on your local drive. You will adjust some of the files in that local copy, then `add` and `commit` the changes. When you `commit` a change, you will be required to write a message describing the change (e.g., "corrected typos", "added chat feature"). *Git will intelligently detect which files changed.* This is part of how version control is handled. With each `commit` to the repository, Git keeps a history of these changes, and we will keep (hopefully) descriptive notes of these changes.

If we are satisfied with a `commit` and want to update the remote repository (which everyone will access, unlike your local copy of the repository), you can then `push` the changes to GitHub (or whatever host you're using, but we're using GitHub for this project). Once a change is pushed, the remote repository will be updated.

### Pull Requests

This might not be as relevant for us but it could be super useful. Essentially, if you get a cool idea that we didn't really discuss, or you think you have a better solution to a problem that you know somebody else is working on, you can make those changes all you want and then open a "Pull Request". This makes people aware of your commits prior to you pushing them to the repository. However, we're on a small team and it will be easy for us to delegate tasks, which would prevent any conflicts without having to get others to review and approve changes.

You can also use Pull Requests to bring a programming issue to a team-member's (or the whole team's) attention.

### Example

To add the JATOS file structure to GitHub, I used command line (haven't figured out how to use Atom's integration just yet).

```{r eval = F}
# change local directory to file structure for git repo

cd /c/Users/forst/Documents/GitHub/esc_grat_rep1

# initialize as git repo

git init

# add all files to the repo

git add .

# commit files, with a descriptive message (-m)

git commit -m "first JATOS commit"

# set the remote repository

git remote add origin https://github.com/ejpedersen/grat_rep1.git

# verify that the remote repository is set

git remote -v

# push the local file structure to the remote repo

git push origin master
```


With each change you make (added/modified file or folder), you will follow these steps. Some steps can be skipped if you already completed them (e.g., `git remote add origin`) or altogether (e.g., `git remote -v`). Let's say you've already set up your local filepath and linked to the appropriate GitHub repo, then your code may simply look like this:

```{r eval = F}
git add .

git commit -m "fixed some nonsense"

git push origin master
```


I will update this markdown with instructions on how Atom's integration works. Hopefully this demonstrates how easy it can be even with command line.
