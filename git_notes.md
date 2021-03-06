# Git notes
Notes form the lessons on git and github.


## Content
- [Commands](#Commands)
  - list of commands introduced in the lectires with a small description as a reminder.
- [Terminology](#Terminology)
  - explanation for some of the terms used in the lessons
- [References](#References)
  - links and references to further learning



---

## Commands
|                        Command        | Description |
| ------------------------------------- | ---|
|`git init`| initialize the git in the folder |
|`git status`| return the current state of the files modified, added or commited |
|`git clone`| copy/clone a (local or remote) reporsitory and initialize git |
|`git log` | log command for returning a detailed list of commits and relevant metadata |
|`git log --oneline` | flag for the log command to reduce shown output more concisely  |
|`git log --stats` | flag for the log command to show file change statistics |
|`git log --decorate` | flag for the log command to show branches and current position |
|`git log -p` | flag for the log command  |
|`git add` | add filed to the the stage |
|`git commit` | submit the file changes to the git |
|`git diff`|  The command can be used to see changes that have been made but haven't been committed, yet. |
|`git tag -a v1.0 <SHA>`| use of tag comand for marking versions and special positions in the code change history |
|`git tag -d v1.0`| remove tag |
|`git branch`| lists out all branches available  |
|`git branch sidebar`| create branch with the name 'sidebar'|
|`git checkout master/sidebar`| swithc to specified branch |
|`git log --oneline --decorate --graph --all` | usefull log command to show git tree |
| `git merge` | (fast forward merge) (merge conflicts) |
| `git commit --amend` | revert the last commit  |
| `git revert <SHA-of-commit-to-revert>` | The git revert command is a forward-moving undo operation that offers a safe method of undoing changes. Instead of deleting or orphaning commits in the commit history, a revert will create a new commit that inverses the changes specified. Git revert is a safer alternative to git reset in regards to losing work. Reverting creates a new commit that reverts or undos a previous commit. Resetting, on the other hand, erases commits! |
| `git reset` | It can be used to move the HEAD and current branch pointer to the referenced commit, erase commits, move committed changes to the staging index, or unstage committed changes
|




TIP-s

TIP: Did you also notice the helpful text that's located just beneath "Changes to be committed"? It says (use "git rm --cached <file>..." to unstage) This is a hint of what you should do if you accidentally ran git add and gave it the wrong file.

TIP: Globbing lets you use special characters to match patterns/characters. In the .gitignore file, you can use the following:
- blank lines can be used for spacing
- `#` - marks line as a comment
- `*` - matches 0 or more characters
- `?`` - matches 1 character
[abc] - matches a, b, _or_ c
** - matches nested directories - a/**/z matches a/z, a/b/z, a/b/c/z

TIP:

It's very important to know which branch you're on when you're about to merge branches together. Remember that making a merge makes a commit.

As of right now, we do not know how to undo changes. We'll go over it in the next lesson, but if you make a merge on the wrong branch, use this command to undo the merge:

`git reset --hard HEAD^`

(Make sure to include the ^ character! It's a known as a "Relative Commit Reference" and indicates "the parent commit". We'll look at Relative Commit References in the next lesson.)


## Terminology

Terminology

Version Control System / Source Code Manager

A version control system (abbreviated as VCS) is a tool that manages different versions of source code. A source code manager (abbreviated as SCM) is another name for a version control system.

Git is an SCM (and therefore a VCS!). The URL for the Git website is https://git-scm.com/ (see how it has "SCM" directly in its domain!).
Commit

Git thinks of its data like a set of snapshots of a mini filesystem. Every time you commit (save the state of your project in Git), it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. You can think of it as a save point in a game - it saves your project's files and any information about them.

Everything you do in Git is to help you make commits, so a commit is the fundamental unit in Git.
Repository / repo

A repository is a directory which contains your project work, as well as a few files (hidden by default on Mac OS X) which are used to communicate with Git. Repositories can exist either locally on your computer or as a remote copy on another computer. A repository is made up of commits.
Working Directory

The Working Directory is the files that you see in your computer's file system. When you open your project files up on a code editor, you're working with files in the Working Directory.

This is in contrast to the files that have been saved (in commits!) in the repository.

When working with Git, the Working Directory is also different from the command line's concept of the current working directory which is the directory that your shell is "looking at" right now.
Checkout

A checkout is when content in the repository has been copied to the Working Directory.
Staging Area / Staging Index / Index

A file in the Git directory that stores information about what will go into your next commit. You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.

A SHA is basically an ID number for each commit. Here's what a commit's SHA might look like: e2adf8ae3e2e4ed40add75cc44cf9d0a869afeb6.

It is a 40-character string composed of characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. "SHA" is shorthand for "Secure Hash Algorithm". If you're interested in learning about hashes, check out our Intro to Computer Science course.
Branch

A branch is when a new line of development is created that diverges from the main line of development. This alternative line of development can continue without altering the main line.

Going back to the example of save point in a game, you can think of a branch as where you make a save point in your game and then decide to try out a risky move in the game. If the risky move doesn't pan out, then you can just go back to the save point. The key thing that makes branches incredibly powerful is that you can make save points on one branch, and then switch to a different branch and make save points there, too.

With this terminology in mind, let's take a high-level look at how we'll be using Git by looking at the typical workflow when working with version control.

## References

[git merge from Atlassian blog](https://www.atlassian.com/git/tutorials/git-merge)
