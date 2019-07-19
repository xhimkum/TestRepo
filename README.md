#Read this documentation to understand about this repository.
############################################################
#Example: Start a new repository and publish it to GitHub
First, you will need to create a new repository on GitHub. You can learn how to create a new repository in our Hello World guide. Do not initialize the repository with a README, .gitignore or License. This empty repository will await your code.

# create a new directory, and initialize it with git-specific functions
>"git init my-repo"
to simply initialize the git inside the project folder use: "git init"

# change into the `my-repo` directory
>cd my-repo

# create the first file in the project
>touch README.md

# git isn't aware of the file, stage it
>git add README.md

# take a snapshot of the staging area
>git commit -m "add README to initial commit"

# provide the path for the repository you created on github
>git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

# push changes to github
>git push --set-upstream origin master

#####################################################
#Example: contribute to an existing branch on GitHub
# assumption: a project called `repo` already exists on the machine, and a new branch has been pushed to GitHub.com since the last time changes were made locally

# change into the `repo` directory
>cd repo

# update all remote tracking branches, and the currently checked out branch
>git pull

# change into the existing branch called `feature-a`
>git checkout feature-a

# make changes, for example, edit `file1.md` using the text editor

# stage the changed file
>git add file1.md

# take a snapshot of the staging area
>git commit -m "edit file1"

# push changes to github
>git push


###############
#if origin already exists in the repository
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
It means pretty much what it says, the remote origin already exists, ie. you've already set it up before. You can type git remote -v to see what/where remotes are set. If you made a mistake before you can type "git remote rm origin" to clear it out and try again.
###################################################
#Connect your local project folder to your empty folder/repository on Github.
The screen you should be seeing now on Github is titled 'Quick setup — if you’ve done this kind of thing before'.

Copy the link in the input right beneath the title, it should look something like this: https://github.com/mindplace/test-repo.git This is the web address that your local folder will use to push its contents to the remote folder on Github.

1.Go back to your project in the terminal/command line.

2.In your terminal/command line, type git remote add origin [copied web address]

Example: git remote add origin https://github.com/mindplace/test-repo.git

3.Push your branch to Github: git push origin master

4.Go back to the folder/repository screen on Github that you just left, and refresh it. The title 'Quick setup — if you’ve done this kind of thing before' should disappear, and you should see your files there.


