Git Commands
============
A list of my commonly used Git commands

## Install Git
### install Git on Mac OSX
There are several ways to install Git on a Mac. In fact, if you've installed XCode (or it's Command Line Tools), Git may already be installed. To find out, open a terminal and enter git --version.

```
$ git --version
git version 2.7.0 (Apple Git-66)

```
### Git for Mac Installer
The easiest way to install Git on a Mac is via the stand-alone installer:

1. Download the latest [Git for Mac installer](https://sourceforge.net/projects/git-osx-installer/files/).

2. Follow the prompts to install Git.

3. Open a terminal and verify the installation was successful by typing git --version:

```
$ git --version
git version 2.9.2git 
```

### Install Git on Windows
#### Git for Windows stand-alone installer
1. Download the latest [Git for Windows installer](https://git-for-windows.github.io/).

2. sWhen you've successfully started the installer, you should see the Git Setup wizard screen. Follow the Next and Finish prompts to complete the installation. The default options are pretty sensible for most users.

3. Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).

4. Run the following commands to configure your Git username and email using the following commands, replacing Emma's name with your own. These details will be associated with any commits that you create:

```s
$ git config --global user.name "Emma Paris"
$ git config --global user.email "eparis@atlassian.com"
```

### Tell Git Who You Are

| Command | Description |
| ------- | ----------- |
| `git config --global user.name "Sam Smith"` <br> `git config --global "user.email sam@example.com"` | Configure the author name <br>and email address to be used <br>with your commits. |
| `git remote -v` | List all currently configured<br> remote repositories |

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` <br> `git clone username@host:ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Commit any files you've added <br> with git add, and also commit any <br>files you've changed since then |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branchName]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | CommitId is the leading characters<br> of the changeset ID, up to 10, but<br> must be unique. Get the ID using |
| `git log --summary` | View changes (detailed) |
| `git diff` <br> `git diff --base <filename>` <br> `git diff [source branch] [target branch]` | Preview changes before merging |

### Undo Local Changes

| Command | Description |
| ------- | ----------- |
| `git checkout -- <filename>` | If you mess up, you can replace the changes<br> in your working tree with the last content<br> in head. Changes already added to the <br>index, as well as new files, will be kept.|
| `git fetch origin` <br> `git reset --hard origin/master` | Instead, to drop all your local changes <br>and commits, fetch the latest history from <br>the server and point your local master<br> branch at it, do this. |

### Tag

| Command | Description |
| ------- | ----------- |
| `git tag 1.0.0 <commitID>` | You can use tagging to mark a significant<br> changeset, such as a release |
| `git push --tags origin` | Push all tags to remote repository |

### Search

| Command | Description |
| ------- | ----------- |
| `git grep "foo()"` | Search the working directory for foo():|
