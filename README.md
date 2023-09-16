# Initializing a Repository and Making Commits

First off, when you are trying to make use of git, there are some general setup that needs to be cleared off before we start using git on our working environment.

But before then, we should have git installed on our PCs

After installation of git, then we can use this setting to setup our git configuration

First thing, we initialize git on our working directory

`git init`

#### Code Output

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image1.png">

Then we can go ahead with our setup. You can change the information as required to your details

```
    git config --global user.name "Afeez"
    git config --global user.email "tundek79@gmail.com"
    git config --global init.defaultBranch main
```

The above command will 

1. Create a username
2. Create an email for the account
3. create a default branch called main

### Making commits

First, we need to track our working files by adding the files into the staging area before comming them.

There are 3 different stages where files are in the GIT lifecycle
1. Working files (These are the files that you are currently working on and has not been tracked by GIT)
2. Staging (At this stage, the files are already been tracked by GIT but has not been saved)
3. Commit (At this point the files are now saved into the history books (if you will))

#### Here's the demonstration for the above

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image2.png">

From the above image, i used the `git status` to check the current status of my files on GIT and it indicates that none of the files are being tracked since i initialized git on the working folder.

This id also indicated with the red color of al files that are yet to be tracked.

I ran another command `git add .` command to start tracking all the files in the directory.

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image3.png">

After running the `git add` command followed by the git status, the above is the result, showing a green color of all the working files indicating the files are now being tracked and once work is done, can be commited.

Let's commit the changes into the history books using the command `git commit -m "first commit"`

#### Code Output

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image4.png">


# Working with Branches

It's good that we now able to make commits and save into the history book which doesn't really go away unless maybe you or someone else tear (delete) the history book, but not sure anyone will do that nowadays.

Anyway, let's say we have a project already in production and our customers are enjoying, but we need to add a new feature or work on an existing feature. How do we go about this without running into issues with our customers complaining they are unabel to use our softwares.

A concept of branches came onboard, where by we create an exact copy of our project and we can make edits as required. It might be working on a new or existing feature. After working, testing and making sure all is fine with our new version, then we merge to the main branch. Enough talking, let's get working

#### Creating a new branch

With what i have seen (abi), there seems to be a number of ways to creating a new branch. Let's explore some of them.

`git branch my_new_branch`

The above creates a new branch but doesn't login to it

To create and switch into a new branch, use `git switch -c another_branch`

#### Code output

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image5.png">

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image6.png">


###### Another method of creating branch, using the checkout command and listing the branch

Use can also the use the command `git checkout -b newest_branch` and use `git branch` to check the list of all available branches

#### Code output

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image7.png">


### Change into an Old branch

To change your current branch into an old one, use the command

`git checkout <branch-name>` OR `git swith <branch-name>`

Example:

#### Code output

Switch => 

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image8.png">

Checkout =>

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image9.png">


### Mergin a Branch into another Branch

Let's switch into a new branch and make some changes on the new branch we switch to. Then exit into the main branch and see if the changes effect on the main branch

`git switch new-branch`

Make some edits on the new branch, commit the changes and switch back into the main branch then run the following commands

`git merge -m "Merging sample file, into the main branch" new-branch`

#### Code output

<img width="600" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image10.png">


# Collaboration and Remote Repositories

We have been working on our local computer or local server all these while, when we want to collaborate with other developers or team mates, they might not have access to our local computer, which is why it is important to work remotely and collaborate from their. 

For Creating Remote repositories, we will be using GitHub as a Social Coding platform where repositories can be created, worked on.


The account creation for github should be fairly simple to do, visit the [GitHub Website](https://github.com)
After that, create a repository where all your files will be hosted and let's connect to the repo and upload all the work we have done so that we can collaborate with our workmates.

<img width="700" alt="Git init" src="/Users/appple/Documents/DevOps_Projects/DevOps/Project1/images/image11.png">

First off, we need to add a remote reporsitory to the local repo we have been working on, use the command

`git remote add origin https://github.com/tundek/DevOps.git`

Afterwards, it is time to push all your files to the remote repository using the command

`git push origin <branch-name>` => `git push origin main`