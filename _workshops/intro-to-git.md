---
layout: workshop
module: Intro to Git
track: misc
---

#**Intro to Git**#
This is a tutorial designed for beginners with the goal of teaching them how to use the command line to start contributing to Github repos.
________________________

###Initialization###

First lets start off by making an account at

https://github.com/

After creating a Github account we would want to initialize everything on our local machines in order to use git.

Open up the command line and enter

>git config --global user.name "Whatever you used as your username"  
>git config --global user.email "Whatever you used as the email"

###Starting to Upload Files###
______________________________

Now that we have initialized everything lets try uploading something onto Github by creating our own repository through

https://github.com/new

Here you would specify some of the details of what your repository will contain. The repository name would be the title of whatever you're uploading and the description helps explain what your repository does.

After specifying the details of your soon to be live repository you will then

>cd "(directory of the folder in which the files you want uploaded to be)"
>git init

note: cd stands for change directory and is used to navigate around your machine.

Now to start actually adding files that you want to upload you would use these commands:

>git add "name of file you want to upload"

git add will let you choose which files you want to add to the repository. If you wish to add all files in a certain directory then you could choose to use "git add ." instead of typing the file name of everything you're uploading.

note: git add does not actually upload any files. You use git add to choose which files you're going to upload.

>git commit -m "comment that follows the upload"

git commit will "confirms" what you're about to upload and "locks it in" so that it'll be ready for you to upload.

>git remote add origin "url of the github repository you created"
>git push -u origin master

After this step you should see that the files have been uploaded. git push is the step which actually uploads everything that you've committed.



###Downloading from a public repo###
______________________________

If we want to download another person's repository then we would find the URL of their repo and enter

>git clone "url"

If you've already downloaded a repository then you could cd (change directory) to the folder where the downloaded repo is and use

>git pull

to update your version of the repo to the most up-to-date version.

But what if we don't know if our branch is up-to-date or not? We can check if it is by using

>git status

note: It is also a good habit to check if your repo is up-to-date before working or uploading any changes.

