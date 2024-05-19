## Git Hidden Folder

There is a hidden folder `.git` which tells you that our project is a Git Repo.

If we want to creat a Git Repo in a new project. We've created a folder where we gonna initialize it, using `git init`
```sh
mkdir workspaces/tmp/new-project/
cd workspaces/tmp/new-project/    
git init
touch Readme.md 
code Readme.md
# make some changes to readme.md
git status
git add .
git commit -a -m "add readme file"
```

## Cloning

We can clone three ways: HTTPS, SSH, GitHub CLI

Since we're using GitHub Codespaces, we'll create a temporary directory in our workspace

```sh
mkdir workspaces/tmp/
cd workspaces/tmp/
```

### HTTPS

```sh
git clone https://github.com/mrv-testin/GitHub-Foundations-Example_01.git
cd GitHub-Foundations-Example_01/
```

## SSH
```sh
git clone git@github.com:mrv-testin/GitHub-Foundations-Example_01.git
```

We will need to create our own SSH rsa Key pair
```sh
sshe-keygen -t rsa
```
We can test our connection here:
```
ssh -T git@github.com
```

## Commits
When we want to commit code we can write git commit which will open up the commit edit message in the editor of choice. 
```sh
git commit
```
But first we need to set the global editor
```sh
git config --global core.editor emacs
```
Make a commit and commit message withou opening an editor 
```sh
git commit -m "add another exclamation mark"
```

## Branches

## Remotes

## Stashing

```
git stash list
git stash
git stash save myName
git stash apply 
git stash pop
```

## Merging

## Add

When we want to stage changes that will be included in the commit. We can use the . to add all possible files.
```sh
git add Readme.md
git add .
```

## Reset
Reset allows you to move staged changes (where they are available to be committed) to be unstaged   

This is useful when you want to revert all file not to be committed
```sh
git add . 
git reset
```
> git reset will revert git add . 

## Status

Git status shows you what files will o not be committed
```sh
git status
```

## Gitconfig file
The _gitconfig_ file is what stores your global configurations for git such as email, name, editor and more. 

Showing the content of the gitconfig file
```sh
git config --list
```
When you first install Git on a machine you are supposed to set your name and email 
```
git config --global user.name "mrv-testin"
git config --global user.email millonesmam@gmail.com
```

## Log
git log will show recent git commits to the git tree (history of changes)

## Push
When we want to push a repo to our remote origin    
```
git push
```
To push, first we need to commit before