# How to use git
This file contains only a small subset of the available commands for git. For a more detailed example, check out [Atlassian's documentation on git](https://www.atlassian.com/git/tutorials/what-is-version-control).

## Copy a repository from the internet to your computer

`git clone <url> <optionalFolderName>`

To clone this repo into a folder called devAcademy, you would use the following command: `git clone https://github.com/kaizen-soze/class-resources.git` devAcademy

Without the folder name, git will attempt to create a folder with the same name as the repo.

## View all changed files in your repository

`git status`

## Add a file to a new commit

A commit will only contain the changes that you tell git that you want it to have. Files must be added manually before you can commit.

### Adding one file at a time
`git add` is only for adding newly-created files to a repository. Modified files are included with the `-m` flag of `git commit`.

So, if you add a brand new file called `contactPage.html`, git will not add it unless you invoke `git add`

`git add <newFile>`
`git add contactPage.html`

To view all newly-added files, run `git status`. You can copy/paste the filenames from there.

### Adding all newly-created files
`git add .`

## Add a new commit

When you make changes to a piece of software, it's usually because you're fixing a bug or implementing a feature. These changes can be in one file or multiple files, but that changed code can be added to the repository and grouped together. This grouping is called a commit.

Commits are added to the commit log, and the message for each commit (should) help you to understand what changes have been made.

When your changes are finished and you've added all relevant changes, you want to add the commit to your repository.

### Syntax
`git commit -<flags> <commit message>`

### Common flags
The `a` flag tells git that the commit should include any files you've added with the `git add` command.

The `m` flag tells git that the commit should include all modified files. Git automatically tracks which files have been modified.

### Usage
`git commit -am "My commit message"`

## Move code from your computer to the remote repository

`git push`

Typically `git push` doesn't require any arguments, but there are exceptions.

If you push code from a new branch that doesn't exist remotely, git will tell you.

```
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin your-branch-name
```

When you see this message, simply copy/paste the command that git tells you to run. The new branch will then be added to the remote repository

## View all available branches in the repository

`git branch`

## Undo all changes to a single file

Sometimes you have made so many mistakes that you just need to start over from scratch. To undo all changes to a single file, run `git checkout`

### Syntax
`git checkout <filename>`

You must use the exact path for the file in order for the command to be a success. Run `git status` to see all changed files and then copy/paste the name of the file you want to undo changes to.

## Create a new branch

`git checkout -b <branchName>`

## View all repository URLs

It's possible for the same repository to have multiple endpoints. We'll cover the why and how at a later date. For now, just run:

`git remote -v`

To see all remote URLs for your repository