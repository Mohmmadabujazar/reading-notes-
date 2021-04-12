# Git Push

> What Does git push Do?
git push updates the remote branch with local commits. It is one of the four commands in Git that prompts interaction with the remote repository. You can also think of git push as update or publish.

>By default, git push only updates the corresponding branch on the remote. So, if you are checked out to the master branch when you execute git push, then only the master branch will be updated. It's always a good idea to use git status to see what branch you are on before pushing to the remote.

>How to Use git push
After you make and commit changes locally, you can share them with the remote repository using git push. Pushing changes to the remote makes your commits accessible to others who you may be collaborating with. This will also update any open pull requests with the branch that you're working on.

>As best practice, it's important to run the git pull command before you push any new changes to the remote branch. This will update your local branch with any new changes that may have been pushed to the remote from other contributors. Pulling before you push can reduce the amount of merge conflicts you create on GitHub - allowing you to resolve them locally before pushing your changes to the remote branch.

>Common usages and options for git push
git push -f: Force a push that would otherwise be blocked, usually because it will delete or overwrite existing commits (Use with caution!)
git push -u origin [branch]: Useful when pushing a new branch, this creates an upstream tracking branch with a lasting relationship to your local branch
git push --all: Push all branches
git push --tags: Publish tags that aren't yet in the remote repository
You can see all of the options with git push in git-scm's documentation.

>Why can't I push?
If you are trying to git push but are running into problems, there are a few common solutions.

>Check your branch
Check what branch you are currently on with git status. If you are working on a protected branch, like master, you may be unable to push commits directly to the remote. If this happens to you, it's OK! You can fix this a few ways.

>Work was not yet on any branch
Create and checkout to a new branch from your current commit: git checkout -b [branchname]
Then, push the new branch up to the remote: git push -u origin [branchname]
Accidentally committed to the wrong branch
Checkout to the branch that you intended to commit to: git checkout [branchname]
Merge the commits from the branch that you did accidentally commit to: git merge [master]
Push your changes to the remote: git push
Fix the other branch by checking out to that branch, finding what commit it should be pointed to, and using git reset --hard to correct the branch pointer
Related Terms
git commit -m "descriptive message": Records file snapshots permanently in version history.
git clone [url]: Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits.
git status: Always a good idea, this command shows you what branch you're on, what files are in the working or staging directory, and any other important information.
git pull: Updates your current local working branch with all new commits from the corresponding remote branch on GitHub. git pull is a combination of git fetch and git merge.

# Git Add
```
The git add command adds new or changed files in your working directory to the Git staging area.

git add is an important command - without it, no git commit would ever do anything. Sometimes, git add can have a reputation for being an unnecessary step in development. But in reality, git add is an important and powerful tool. git add allows you to shape history without changing how you work.

When do you use git add?
git add README.md
As you're working, you change and save a file, or multiple files. Then, before you commit, you must git add. This step allows you to choose what you are going to commit. Commits should be logical, atomic units of change - but not everyone works that way. Maybe you are making changes to files that aren't logical or atomic units of change. git add allows you to systematically shape your commits and your history anyway.

What Does Git Add Do?
git add [filename] selects that file, and moves it to the staging area, marking it for inclusion in the next commit. You can select all files, a directory, specific files, or even specific parts of a file for staging and commit.

This means if you git add a deleted file the deletion is staged for commit. The language of "add" when you're actually "deleting" can be confusing. If you think or use git stage in place of git add, the reality of what is happening may be more clear.

git add and git commit go together hand in hand. They don't work when they aren't used together. And, they both work best when used thinking of their joint functionality.

How to Use git add
Common usages and options for git add
git add <path>: Stage a specific directory or file
git add .: Stage all files (that are not listed in the .gitignore) in the entire repository
git add -p: Interactively stage hunks of changes
You can see all of the many options with git add in git-scm's documentation.

Examples of git add
git add usually fits into the workflow in the following steps:

Create a branch: git branch update-readme
Checkout to that branch: git checkout update-readme
Change a file or files
Save the file or files
Add the files or segments of code that should be included in the next commit: git add README.md
Commit the changes: git commit -m "update the README to include links to contributing guide"
Push the changes to the remote branch: git push -u origin update-readme
But, git add could also be used like:

Create a branch: git branch update-readme
Checkout to that branch: git checkout update-readme
Change a file or files
Save the file or files
Add only one file, or one part of the changed file: git add README.md
Commit the first set of changes: git commit -m "update the README to include links to contributing guide"
Add another file, or another part of the changed file: git add CONTRIBUTING.md
Commit the second set of changes: git commit -m "create the contributing guide"
(Repeat as necessary)
Push the changes to the remote branch: git push -u origin update-readme
git add All Files
Staging all available files is a popular, though risky, operation. This can save time, but the risks are two-fold:

Poorly thought out history
By staging all available changes, the clarity of your history will likely suffer. Being able to shape your history is one of the greatest advantages of using Git. If your commits are too large, contain unrelated changes, or are unclearly described in the commit message, you will lose the benefits of viewing and changing history.

Accidentally staging and committing files
By using an option to add all files at once, you may accidentally stage and commit a file. Most common flags don't add files tracked in the .gitignore file. But, any file not listed in the .gitignore file will be staged and committed. This applies to large binary files, and files containing sensitive information like passwords or authentication tokens.

Deciding to stage all files
If the time is right to stage all files, there are several commands that you can choose from. As always, it's very important to know what you are staging and committing.

git add -A: stages all files, including new, modified, and deleted files, including files in the current directory and in higher directories that still belong to the same git repository
git add .: adds the entire directory recursively, including files whose names begin with a dot
git add -u: stages new and modified files only, NOT deleted files
New files	Modified files	Deleted files	Files with names beginning with a dot	Current directory	Higher directories
git add -A	Yes	Yes	Yes	Yes	Yes	Yes
git add .	Yes	Yes	Yes	Yes	Yes	No
git add -u	No	Yes	Yes	Yes	Yes	Yes
git add A Folder or Specific File
The safest and clearest way to use git add is by designating the specific file or directory to be staged. The syntax for this could look like:

git add directory/: Stage all changes to all files within a directory titled directory
git add README.md: Stage all changes within the README.md file

Undo Added Files
Before undoing a git add, you should first be sure that you won't lose any work. There's no way to "revert" an add in the same way you can revert a commit, but you can move the files out of the staging area.

For example, if you have a staged file, and then you make more changes to that file in your working directory. Now, the versions in your working directory and your staging area are different. If you take action to remove the changed version of the file from the staging area, the changes that were in your working directory but not staged will be overwritten.

To avoid this, first stage all changes, then unstage them together, or commit the changes and reset back before the commit happened.

Using git reset to undo git add
git reset is a flexible and powerful command. One of its many use cases is to move changes out of the staging area. To do this, use the "mixed" level of reset, which is the default.

To move staged changes from the staging area to the working directory without affecting committed history, first make sure that you don't have any additional changes to the files in question as mentioned above. Then, type git reset HEAD (aka git reset --mixed HEAD).

Related Terms
git status: Always a good idea, this command shows you what branch you're on, what files are in the working or staging directory, and any other important information.
git checkout [branch-name]: Switches to the specified branch and updates the working directory.
git commit -m "descriptive message": Records file snapshots permanently in version history.
git push: Uploads all local branch commits to the remote.
```
# Git Commit
```
git commit creates a commit, which is like a snapshot of your repository. These commits are snapshots of your entire repository at specific times. You should make new commits often, based around logical units of change. Over time, commits should tell a story of the history of your repository and how it came to be the way that it currently is. Commits include lots of metadata in addition to the contents and message, like the author, timestamp, and more.

How Git Commit Works
Commits are the building blocks of "save points" within Git's version control.

git commit -m "update the README.md with link to contributing guide"
Commits shape history
By using commits, you're able to craft history intentionally and safely. You can make commits to different branches, and specify exactly what changes you want to include. Commits are created on the branch that you're currently checked out to (wherever HEAD is pointing) so it's always a good idea to run git status before making a commit, to check that you're checked-out to the branch that you intend to be. Before you commit, you will need to stage any new changes that you'd like to include in the commit using git add [file].

Commits are lightweight SHA hashes, objects within Git. As long as you're working with text files, you won't need to worry about how many files you have, how big they are, or how many commits you make. Git can handle it!

Committing in two phases
Commits have two phases to help you craft commits properly. Commits should be logical, atomic units of change that represent a specific idea. But, not all humans work that way. You may get carried away and end up solving two or three problems before you remember to commit! That's OK - Git can handle that. Once you're ready to craft your commits, you'll use git add <FILENAME> to specify the files that you'd like to "stage" for commit. Without adding any files, the command git commit won't work. Git only looks to the staging area to find out what to commit. Staging, or adding, files, is possible through the command line, and also possible with most Git interfaces like GitHub Desktop by selecting the lines or files that you'd like to stage.

You can also use a handy command, git add -p, to walk through the changes and separate them out, even if they're in the same file.

How to Use Git Commit
Common usages and options for Git Commit
git commit: This starts the commit process, but since it doesn't include a -m flag for the message, your default text editor will be opened for you to create the commit message. If you haven't configured anything, there's a good chance this will be VI or Vim. (To get out, press esc, then :w, and then Enter. :wink:)
git commit -m "descriptive commit message": This starts the commit process, and allows you to include the commit message at the same time.
git commit -am "descriptive commit message": In addition to including the commit message, this option allows you to skip the staging phase. The addition of -a will automatically stage any files that are already being tracked by Git (changes to files that you've committed before).
git commit --amend: Replaces the most recent commit with a new commit. (More on this later!)
To see all of the possible options you have with git commit, check out Git's documentation.

How to Undo Commits in Git
Sometimes, you may need to change history. You may need to undo a commit. If you find yourself in this situation, there are a few very important things to remember:

If you are "undoing" a commit that exists on the remote, you could create big problems for your collaborators
Undoing a commit on work that you only have locally is much safer
What can go wrong while changing history?
Changing history for collaborators can be problematic in a few ways. Imagine - You and another collaborator have the same repository, with the same history. But, they make a change that deletes the most recent commit. They continue new commits from the commit directly before that. Meanwhile, you keep working with the commit that the collaborator tried to delete. When they push, they'll have to 'force push', which should show to them that they're changing history. What do you think will happen when you try to push?

In dramatic cases, Git may decide that the histories are too different and the projects are no longer related. This is uncommon, but a big problem.

The most common result is that your git push would return the "deleted" commit to shared history. (First, you would git pull if you were working on the same branch, and then merge, but the results would be the same.) This means that whatever was so important to delete is now back in the repository. A password, token, or large binary file may return without ever alerting you.

git revert
git revert is the safest way to change history with Git. Instead of deleting existing commits, git revert looks at the changes introduced in a specific commit, then applies the inverse of those changes in a new commit. It functions as an "undo commit" command, without sacrificing the integrity of your repository's history. git revert is always the recommended way to change history when it's possible.

git reset
Sometimes, a commit includes sensitive information and needs to actually be deleted. git reset is a very powerful command that may cause you to lose work. By resetting, you move the HEAD pointer and the branch pointer to another point in time - maybe making it seem like the commits in between never happened! Before using git reset:

Make sure to talk with your team about any shared commits
Research the three types of reset to see which is right for you (--soft, --mixed, --hard)
Commit any work that you don't want to be lost intentionally - work that is committed can be gotten back, but uncommitted work cannot
git reflog
If you're changing history and undoing commits, you should know about git reflog. If you get into trouble, the reflog could get you out of trouble. The reflog is a log of every commit that HEAD has pointed to. So, for example, if you use git reset and unintentionally lose commits, you can find and access them with git reflog.

Updating Commits With Git Commit Amend
While git commit --amend does change history, it only changes the most recent commit on your current branch. This can be an extremely useful command for commits that:

Haven't been pushed to the remote yet
Have a spelling error in the commit message
Don't contain the changes that you'd like to contain
Examples of Git Commit
Once you've staged the files that you want to include in your commit, you're ready. Whether you commit in a tool like GitHub Desktop, or through your command line, the commit message is important. Commit messages should be short and descriptive of your change. If you are looking through your repository's history, you'll be guided by the commit messages, so they should tell a story. Commits in the command line can include the message with the following format:

git commit -m "git commit message example"
Commit messages should be present tense and directive, like the following examples:

git commit -m "create file structure for Git guides"
git commit -m "translate Git cheat sheet into German"
git commit -m "update broken URL to Git resources"
If you'd like to include more context in your commit messages, you can also include an extended commit message.

Related commands
git add [file]: Snapshots the file in preparation for versioning, adding it to the staging area.
git status: Always a good idea, this command shows you what branch you're on, what files are in the working or staging directory, and any other important information.
git push: Uploads all local branch commits to the remote.
git log: Browse and inspect the evolution of project files.
```