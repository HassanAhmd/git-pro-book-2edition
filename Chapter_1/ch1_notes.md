# The Three States where files in git reside in.
1. **Modified**:
    Modified means that you have changed the file but have not committed to your local database yet.

2. **Staged**:
    Staged means that you have marked a modified file in its current version to go into your next commit snapshot.

3. **committed**
    Committed means that the data is safely stored in your local database.

And this the components or the three main sections of a Git project:
* *Working Directory* 
    - Is a single checkout of one version of the project.
* *Staging Area*
    - Is a file, generally contained in your Git directory, that stores information about what will go into your next commit.
* *.git directory*
    - Is where Git stores the metadata and object database for your project. This is the most important part of Git, and it is what is copied when you clone a respository from another computer.
    
The Workflow is this: 
1. You modify files in your working tree.

2. You selectively stage just those changes you want to be part of your next commit, which adds *only* those changes to the staging area.

3. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory. 


# Customize Git enviroment
You will do these configurations only once on any given computer; they will stick around between upgrades.
You can also change them at any given time by running the commands again.

* Git has tool called `git config` that lets you get and set configuration variables that control all aspects of how Git looks and operates.

This are **local client settings for the Git software** on your computer.
These variables can be stored in three different places:


1. **System** `[path]/etc/gitconfig`(Linux/macOS) file: Applies to every user on the computer and all their repositories. 
If you pass the option `--system` to `git config`, it read and writes from this file specifically.
Because this is a system configuration file, you will need administrative priviledges to make change to it. 

2. **Global** Applies to the current user(account) across all their repositories. They define personal preferences (like your name, email, etc) that should persist regardless of which project you are working on.
And stored in `~/.gitconfig` or `~/.config/git/config`(Linux/macOS) and `%USERPROFILE%\.gitconfig`(Windows).

3. **Local** This are repository-specific settings that apply *only to the current project* (the `.git` directory you are currently working in). Stored in the `config` file located inside the hidden `.git` directory of the repository. `<repository_root>/.git/config`
This file is automatically created when you run `git init` or `git clone`.


