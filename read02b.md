* After staging one or multiple files, you should commit the changes and record what you did within the commit message:

* $ git commit -m “made change x,y,z”
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

* Committing All Changes
$ git commit -a
*This command commits a snapshot of all modifications to tracked files in the working directory.

* Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

Example:

* $ git push origin master
*This command pushes changes from the local “master” branch to the remote repository named “origin”.

* For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local repository. However, these names can be changed by the user.