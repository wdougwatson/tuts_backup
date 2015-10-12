from [http://www-cs-students.stanford.edu/~blynn/gitmagic/ch02.html#_saving_state](http://www-cs-students.stanford.edu/~blynn/gitmagic/ch02.html#_saving_state "http://www-cs-students.stanford.edu/~blynn/gitmagic/ch02.html#_saving_state")
# Chapter 2. Basic Tricks
Rather than diving into a sea of Git commands, use these elementary examples to get your feet wet. Despite their simplicity, each of them are useful. Indeed, in my first months with Git I never ventured beyond the material in this chapter.

# Saving State
About to attempt something drastic? Before you do, take a snapshot of all files in the current directory with:

    $ git init
    $ git add .
    $ git commit -m "My first backup"
Now if your new edits go awry, restore the pristine version:

    $ git reset --hard
To save the state again:

    $ git commit -a -m "Another backup"
Add, Delete, Rename
The above only keeps track of the files that were present when you first ran git add. If you add new files or subdirectories, you’ll have to tell Git:

    $ git add readme.txt Documentation
Similarly, if you want Git to forget about certain files:

    $ git rm kludge.h obsolete.c
    $ git rm -r incriminating/evidence/
Git deletes these files for you if you haven’t already.

Renaming a file is the same as removing the old name and adding the new name. There’s also the shortcut git mv which has the same syntax as the mv command. For example:

    $ git mv bug.c feature.c


from [https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/ "https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/")


## Create New Repository drop-downCreate a new repository on GitHub.
To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub.
Open Terminal (for Mac and Linux users) or the command prompt (for Windows users).

Change the current working directory to your local project.

Initialize the local directory as a Git repository.

    git init
    # Add the files in your new local repository. This stages them for the first commit.

    git add .
    # Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'.
## Commit the files that you've staged in your local repository.
    git commit -m "First commit"
    # Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.
## Copy remote repository URL
At the top of your GitHub repository's Quick Setup page, click the copy to clipboard icon to copy the remote repository URL.
In the Command prompt, add the URL for the remote repository where your local repository will be pushed.

    git remote add origin remote repository URL
    # Sets the new remote
    git remote -v
    # Verifies the new remote URL
## Push the changes in your local repository to GitHub.

    git push origin master
    # Pushes the changes in your local repository up to the remote repository you specified as the origin

from: who knows?

## git: sync a local repo with a remote repo

    git push origin master
    # Username for http://github.com
    # Password for user@github.com
Thats all for now.
