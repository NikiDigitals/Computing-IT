- Course/Module/Topic: The Git & Github Bootcamp  
  Issuer: Udemy  
  Lesson: full bootcamp  
  Date: 2025-09-05  
  Type: note  
  Tags: #Github #Git #gitBash #gitkraken  
  Related Project(s)  
  Related journals:

---

## Overview

Using Git and GitHub is part of a standard skill set every person working in IT should have.

- Git core (Committing, Branching and Merging, Diffing, Stashing, and undoing changes)
- Github - collab core (Fetching & pulling, Odds & Ends, Collaborative workflows)
- Git extras (Rebashing, Tags, Reflogs, Aliases)
- A <b>repository</b> is a directory with its own history

## keyconcepts GIT

<b>Git</B> is a Version control system (VCS) to:

- Track changes across files
- version control - Compare versions of a project
- Go back to older versions of a project and refer to them if needed.
- Collaborate and share changes with others
- Combine changes.

### Git commit

- With the commands `git add` and `git commit`, you can save changes from different files in specific groups as a reference point.
- Every commit adds a hash code to the reference point as a timestamp to retrieve when necessary. It also adds a parent hash code from a previous commit.

<b>Commit messages</b>

- Try to keep every commit about '1' thing. Remember, it needs to be clear to anyone what was changed!!!!
- Use the present tense imperative style or whatever is normal in your organisation.
- Sometimes the message needs to be longer than just a single line. Use the editor to do this. Make sure the first line is a summary.
- When you forgot a file or need to fix the last commit message, you can amend Commits with `--amend`

### Git Branching

Branches create multiple paths in the same project.  
It allows us to work on different aspects of the same project without interfering with each other's work.  
In the list with all branches, the active one has a \*

<b>Master</b>
This is the branch created by Git when you first initialise a Git repository.
Many people view this branch as the "official branch" for their codebase.

### Git merge

Branches are used to develop new features, among other purposes. When it's finished, it needs to be merged back into the master/main.
When merging branches, the changes are 'merged' into your current location.
For example, when you are on the master branch, the branch you merge will be copied/merged to the master by adding all the commits from the branch.
It doesn't delete or change the branch.

- <b>fast forward merge</b> When master has no new commits, and the branch does. When merging the branch back into the master, it can jump directly to the last commit of the branch as the new reference point for the master.
- <b>>merge commit</b> when new commits have been made on both branches that are not in conflict with each other, Git will merge automatically. It just prompts for the commit message.

<b>Merge conflicts</b>  
When git doesn't know what to do, it will show the problem with markers.

```
<<<< HEAD
Content of the branch file: current location
====
Content of the file you want to merge with
>>> Branch name
```

1. Open up the files with merge conflicts
2. Edit the files to remove the conflict. Decide which keeps the content from both.
3. Remove the conflict markers in the document
4. Add your changes and then make the commit

- It is possible to use VSCode to resolve conflicts:  
  VSCode has an automatic function built in, giving you the following options:
  - Accept Current Changes
  - Accept incoming changes
  - Accept Both changes
  - Compare Changes

### git diff

This comment is all about comparing and looking at changes between commits, branches, files, our working directory and so on.  
Alongside `git status` and `git log`, it provides a clearer view of the repository's changes over time.
Diff shows only a few lines before and after the changes. it starts with header @@

<b><understanding diff output</b>

```
diff --git a/rainbow.txt b/rainbow.txt    # this line gives the files that are compared. a/old version and b/newversion
index  72d1d5a..f3c8118 100642            # metadata <hash file-A...<hash file-b>  < mode-identifier>
--- a/rainbow.txt                         # indicator saying changes in file-a will be shown with a - sign
+++ b/rainbow.txt                         # indicator saying changes in file-b will be shown with a + sign
@@ -3.4 + 3.5 @@ orange                   # header block with changes. First numbers from file-a (-), second set from file-b(+)
yellow                                    -3.4 means: from file-a '4' lines are extracted, starting on line '3' of the file.
green                                     #
blue                                      #
- purple                                  # change that comes from file-a indicated with a -
+ indigo                                  # change that comes from file-b indicated with a +
+ violet                                  # change that comes from filr b indicated with a +
```

When diff creates a header saying --- /dev/null, it indicates that there was no 'file-a' to compare with.
In GitKraken, you can see the differences by just clicking on the files from the unstaged/staged boxes.
You can also see the differences between commits. Select commit 1, hold shift, and select the second one.

## git stashing

Stashing allows you to switch between branches without committing the changes made.  
You can 'save' the changes made to a file to return to them later on.  
Those changes can be reapplied to the working copy on any branch. It isn't necessary to reapply them on the branch you made them on.  
It is possible to use Multiple stashes. They are kept in the order they are stashed, which means the newest stash will get index {0}

<b>The stash list:</b>

```
stash@{index}: WIP on <branchname: hash <last commit message>
stash@{0}: WIP on master: 56B6A73 merged bugfix
```

### Undoing changes & time traveling

The `git checkout` command is one with many functions. It can create branches, switch to new branches, restore files, and undo history.
When going back in time, looking at a specific commit with `git checkout <commit hash>`, the HEAD becomes detached from a particular branch; instead, it references a commit.
To attach the HEAD back to a branch, use the `switch <branch-name>` command.

<b>Travel to an old commit</b>  
It is possible to leave the branch and go back to an old commit with `git checkout`.
When doing so, Git tells you you have a detached Head. This means that the Head is no longer pointing to a branch but to a specific commit.

The 'detached HEAD' options:

1. Stay in detached HEAD to examine the contents of the old commit
2. Leave and go back to the last location > reattach HEAD to a branch.
3. Create and save a new branch and switch to it. > Head is now attached to the new branch. (makes a branch at the level of that old commit)

<b> Referencing a commit relative to another particular commit</b>  
Referencing relative to another commit is done with the command `git checkout HEAD~1`
The number shows the number of steps taken back:  
`HEAD~1` refers to the commit before HEAD (parent)
`HEAD~2` refers to 2 commits before the HEAD (grandparent)

<b>Discarding changes in a file and the use of git restore</b>  
It is possible to delete all changes made in a file before committing to it with the command `git checkout HEAD <filename>`  
This is also possible with the new command `git restore`. Restore can be used to restore the current working file and revert to the status of a former commit.
`Git restore` also has the option to unstage a staged file when needed.

### Git Reset

When you commit on the master branch, but meant to do so on another branch, it is possible to undo those commits wit `git reset.`

### Git Revert

Revers to an old commit undoing changes by creating a new commit from this action.

### .Gitignore

When working on a project, you may want to ignore specific files in Git.
Examples of files you never want to commit include:

- Secrets, API keys, credentials, etc
- operating files
- Log files
- Dependencies & packaging

### HEAD

Head is a pointer that shows your location in your repository.  
It points to the specific branch.
online platform for sharing work done on Git.

## Commands/Syntax

`q` to leave the log. List of branches, and diff.

`git status` gives you feedback on the status of the repository.  
`git init <Name of repository>` Create a new repository in your current directory.

`git add <file names>` to state the files ready to commit and save them in the repository.  
`git add .` to commit all files at the same time.

`git commit -m "commit message"`  
`git commit` to commit and open an editor to record the message.  
`git commit --amend` redo the last commit to fix an error in the message or add forgotten files.  
`git commit -a -m "message"` stages and commits all files in one step.

`git log` gives the log of all the commits in the repo.  
`git log --oneline` makes the logs easier to look at with 1 log per line.

`git branch` gives a list of the current branches in a repository.  
`git branch <branch-name>` Create a new branch based on the current HEAD.  
`git branch -d <branch-name>` deleted the branch when it's fully merged.  
`git branch -D <branch-name>` deletes the branch, no matter its merging status  
`git branch -m <new_name>` changes the name of the branch you are currently on.

`git switch <branch-name>` Switch onto another branch in the repo.  
`git switch -c <branch-name>` creates a new branch and switches to it directly in one step.  
`git checkout <branch-name>` is the older command to switch between branches. (has many options and can do a lot more)  
`git checkout -b <name-Branch>` creates a new branch and switches to it directly in one step.

`git switch -` back to the last branch HEAD was located.  
`git checkout <commit hash>` detaches the HEAD from the branch to look at a specific commit in the past. (To move back, switch to a branch.)
`git checkout HEAD~1` references a commit relative to another particular commit.  
 `git checkout HEAD <file>` discards any changes in that file.  
`git checkout HEAD <filename>` or `git checkout -- <filename>` discards any changes made so far in that file.

`git merge <branch-name>` merges the branch into the current location branch. (make sure you switched to the correct branch!)

`git diff` lists all changes in the working directory that are not staged yet.  
`git diff HEAD` lists all changes in the working directory(tree) since the last commit.  
`git diff --staged` lists the changes between the staging area and the last commit  
`git diff --cached` does the same as --staged (shows what will be included when I run the command git commit now)  
`git diff HEAD <path/filename>` Show only the differences in a specific file  
`git diff --staged <path/filename>` Show only the differences in a specific file or files.  
`git diff branch1..branch2` compares all files in the branches. (you can add a filename here as well)  
`git diff commit1..commit2` Compare the differences between 2 commits (use the hashes) (you can add a filename here as well)

`git stash` or `git stash save` all uncommitted changes (staged and unstaged) will be stashed, reverting the changes in a working copy.  
`git stash pop` removes the most recently stashed changes and re-applies them to the working copy.  
`git stash apply` keeps the changes in the stash and reapplies them to the current working copy.  
`git stash list` gives a list of all the stashed items.  
`git stash apply stash@{index}` if you want to apply a specific stash.  
`git stash drop stash@{index}` removes a specific stash from the 'saved' list.  
`git stash clear` removes all stashed items.

`git restore <filename>` restores the file to the content of the last commit in HEAD. (same as git checkout HEAD <filename>`)
`git restore --source HEAD~1 <filename>`Restores the content to the state of the parent commit. (1 step before HEAD) `git restore --source <hash commit) <filename>`Restores the content to the commit that has been specified.  `git restore --staged <file>` unstages a file when you don't want to commit it.

`git reset <commit-hash>` Resets the repo back to the a specific commit, deleting the once did after that point in time. The changes in files are not deleted.  
 `git reset --hard <hash commit>` Resets the repo upto the specific commit and deleted all changes made in the working files.  
 `git reset --hard HEAD~1` to reset and go back to a specific commit relative to the position of HEAD

`git revert <hash-commit>` reverses to the specifi commit by creating a new commit.

## github

<b>Github</b> is a service that hosts Git repositories in the cloud, making it easier to collaborate with other people.

- The online platform for sharing work done on Git.

## keyconcepts Github

- <b>Github</b> is a service that hosts Git repositories in the cloud, making it easier to collaborate with other people.
- Github the THE home of open source projects.
- Your github profile showcases your oen projects and contributions to other projectss. It can ac as an resume that many rmployers will consult in the hiring process. by being active involved , you also stay up to date!
- it is allowed to clone any public repo, pushing changes is a different story.

### configuring SSH keys

- An SSH key makes it possible to connect to Github from the terminal without having to log in every single time.
- These steps are different for all OS systems. See resources.

### Github push

- When you created a repo on your local system first:

* create an empty repo on github
* connect your local reppo (add a remote)
* Push everything to Github
* **origin** is the conventional name for a remote
*

- When you start a new project

* make a new repo on github
* clone it to your local machine
* when you make changes push it to github

## Commands/Syntax

`git clone <url>` make a clone from your repo on github to your local machine.
`git remote -v` to view any existing remotes for yout repository

`git remote add <name> <url>` Adding a new remote to the local git repository
`git remote rename <old> <new>` for renaming the remote
`git remote remove <name>` Delete a remote
`git push <remote name> <branch>` push your local repo to github

## external resources

[Git documentation](https://git-scm.com/doc) The official git documentation and book for references.  
[.gitignore file](toptal.com/developers/gitignore) A generator to create a start gitignore fi;e for specific projects
[generate a ssh-key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
