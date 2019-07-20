#Read this documentation to understand about this repository.

************************************************************************************************

#Example: Start a new repository and publish it to GitHub

First, you will need to create a new repository on GitHub. You can learn how to create a new repository in our Hello World guide. Do not initialize the repository with a README, .gitignore or License. This empty repository will await your code.
************************************************************************************************
#create a new directory, and initialize it with git-specific functions

>"git init my-repo"
to simply initialize the git inside the project folder use: "git init"

 change into the `my-repo` directory
>cd my-repo

 create the first file in the project
>touch README.md

 git isn't aware of the file, stage it
>git add README.md

 take a snapshot of the staging area
>git commit -m "add README to initial commit"

 provide the path for the repository you created on github
>git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

 push changes to github
>git push --set-upstream origin master

************************************************************************************************
#Example: contribute to an existing branch on GitHub

 assumption: a project called `repo` already exists on the machine, and a new branch has been pushed to GitHub.com since the last time changes were made locally

 change into the `repo` directory
>cd repo

 update all remote tracking branches, and the currently checked out branch
>git pull

 change into the existing branch called `feature-a`
>git checkout feature-a

 make changes, for example, edit `file1.md` using the text editor

 stage the changed file
>git add file1.md

 take a snapshot of the staging area
>git commit -m "edit file1"

 push changes to github
>git push

************************************************************************************************
#if origin already exists in the repository

git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
It means pretty much what it says, the remote origin already exists, ie. you've already set it up before. You can type `git remote -v` to see what/where remotes are set. If you made a mistake before you can type `git remote rm origin` to clear it out and try again.\n

************************************************************************************************
#Connect your local project folder to your empty folder/repository on Github.

The screen you should be seeing now on Github is titled 'Quick setup — if you’ve done this kind of thing before'.

Copy the link in the input right beneath the title, it should look something like this: https://github.com/mindplace/test-repo.git This is the web address that your local folder will use to push its contents to the remote folder on Github.

1.Go back to your project in the terminal/command line.

2.In your terminal/command line, type git remote add origin [copied web address]

Example: git remote add origin https://github.com/mindplace/test-repo.git

3.Push your branch to Github: git push origin master

4.Go back to the folder/repository screen on Github that you just left, and refresh it. The title 'Quick setup — if you’ve done this kind of thing before' should disappear, and you should see your files there

************************************************************************************************

Let’s say you have already added/committed some files to your git repository and you then add them to your .gitignore; these files will still be present in your repository index. This article we will see how to get rid of them.

Step 1: Commit all your changes
Before proceeding, make sure all your changes are committed, including your .gitignore file.

Step 2: Remove everything from the repository
To clear your repo, use:

>git rm -r --cached .

rm is the remove command
-r will allow recursive removal
–cached will only remove files from the index. Your files will still be there.
The . indicates that all files will be untracked. You can untrack a specific file with git rm --cached foo.txt (thanks @amadeann).
The rm command can be unforgiving. If you wish to try what it does beforehand, add the -n or --dry-run flag to test things out.

Step 3: Re add everything
>git add .

Step 4: Commit
>git commit -m ".gitignore fix"

Your repository is clean :)

Push the changes to your remote to see the changes effective there as well.

#To remove the .git from the project folder
> rm -rf .git

Execute this command inside the folder where you want  to remove the git.

************************************************
Create a new branch:
>git checkout -b feature_branch_name

Edit, add and commit your files.

Delete a Local GIT branch
To delete the local GIT branch we can try one of the following commands:
>git branch -d branch_name

>git branch -D branch_name
************************************************
To change the active branch:
>git checkout branch_name

To merge the branch to the master branch,you need to switch to master branch using `git checkout master`, then run:
>git merge new_branch

To see the current active branch:
>git branch

the active branch shown with astrick sign as `*master/any_branch`.


