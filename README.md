# Initializing a Repository and Making Commits

First off, when you are trying to make use of git, there are some general setup that needs to be cleared off before we start using git on our working environment.

But before then, we should have git installed on our PCs

After installation of git, then we can use this setting to setup our git configuration

First thing, we initialize git on our working directory

```
git init
```

#### Code Output

<img width="851" alt="image1" src="https://github.com/tundek/DevOps/assets/15998669/6c5887c9-8e23-46a3-b1af-b490b7971056">


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

<img width="660" alt="image2" src="https://github.com/tundek/DevOps/assets/15998669/191a6e74-c50a-4f1f-8c1b-6fcd8fe24fcc">


From the above image, i used the `git status` to check the current status of my files on GIT and it indicates that none of the files are being tracked since i initialized git on the working folder.

This id also indicated with the red color of al files that are yet to be tracked.

I ran another command `git add .` command to start tracking all the files in the directory.

<img width="460" alt="image3" src="https://github.com/tundek/DevOps/assets/15998669/22366269-bb23-4248-aa83-270218576c84">


After running the `git add` command followed by the git status, the above is the result, showing a green color of all the working files indicating the files are now being tracked and once work is done, can be commited.

Let's commit the changes into the history books using the command 
```
git commit -m "first commit"
```

#### Code Output

<img width="567" alt="image4" src="https://github.com/tundek/DevOps/assets/15998669/231b190a-4c6d-424e-8df8-dd1e4e141e77">



# Working with Branches

It's good that we now able to make commits and save into the history book which doesn't really go away unless maybe you or someone else tear (delete) the history book, but not sure anyone will do that nowadays.

Anyway, let's say we have a project already in production and our customers are enjoying, but we need to add a new feature or work on an existing feature. How do we go about this without running into issues with our customers complaining they are unabel to use our softwares.

A concept of branches came onboard, where by we create an exact copy of our project and we can make edits as required. It might be working on a new or existing feature. After working, testing and making sure all is fine with our new version, then we merge to the main branch. Enough talking, let's get working

#### Creating a new branch

With what i have seen (abi), there seems to be a number of ways to creating a new branch. Let's explore some of them.

```
git branch my_new_branch
```

The above creates a new branch but doesn't login to it

To create and switch into a new branch, use 
```
git switch -c another_branch
```

#### Code output

<img width="498" alt="image5" src="https://github.com/tundek/DevOps/assets/15998669/04266c4d-d334-4fbc-8ac7-243dcf7381c1">

<img width="547" alt="image6" src="https://github.com/tundek/DevOps/assets/15998669/c0b996d7-3126-4abc-bac1-4cff5ffae8a4">


###### Another method of creating branch, using the checkout command and listing the branch

Use can also the use the command 
```
git checkout -b newest_branch
```

and use 
```
git branch
````
to check the list of all available branches

#### Code output

<img width="562" alt="image7" src="https://github.com/tundek/DevOps/assets/15998669/5ff4e6ba-eb08-4c12-a8f2-455450f3fb2f">


### Change into an Old branch

To change your current branch into an old one, use the command

`git checkout <branch-name>` OR `git swith <branch-name>`

Example:

#### Code output

Switch => 

<img width="505" alt="image8" src="https://github.com/tundek/DevOps/assets/15998669/1c6ec98f-d43e-43ec-ba90-d8f6f9b273a1">

Checkout =>

<img width="528" alt="image9" src="https://github.com/tundek/DevOps/assets/15998669/e240c843-5a62-4c8c-ac01-950afb45ddb0">


### Mergin a Branch into another Branch

Let's switch into a new branch and make some changes on the new branch we switch to. Then exit into the main branch and see if the changes effect on the main branch

```
git switch new-branch
```

Make some edits on the new branch, commit the changes and switch back into the main branch then run the following commands

```
git merge -m "Merging sample file, into the main branch" new-branch
```

#### Code output

<img width="923" alt="image10" src="https://github.com/tundek/DevOps/assets/15998669/bed6412d-af7b-408d-9e77-30127de999cf">



# Collaboration and Remote Repositories

We have been working on our local computer or local server all these while, when we want to collaborate with other developers or team mates, they might not have access to our local computer, which is why it is important to work remotely and collaborate from their. 

For Creating Remote repositories, we will be using GitHub as a Social Coding platform where repositories can be created, worked on.


The account creation for github should be fairly simple to do, visit the [GitHub Website](https://github.com)
After that, create a repository where all your files will be hosted and let's connect to the repo and upload all the work we have done so that we can collaborate with our workmates.

<img width="1231" alt="image11" src="https://github.com/tundek/DevOps/assets/15998669/8620d03e-824c-4d80-a77a-005efc68398e">



First off, we need to add a remote reporsitory to the local repo we have been working on, use the command

```
git remote add origin https://github.com/tundek/DevOps.git
```

Afterwards, it is time to push all your files to the remote repository using the command

`git push origin <branch-name>` => `git push origin main`

<img width="572" alt="Screenshot 2023-09-16 at 18 17 59" src="https://github.com/tundek/DevOps/assets/15998669/f7364c92-38ce-4a8c-9c89-637435e35a84">

# Branch Management and Tagging

## Introduction to Markdown Syntax

## 1. Heading

Just like having Headings h1 .... h6 in html, it is a little bit similar where a single # represents the highest heading and the more the number of # the smaller the heading becomes

Example:

# Heading 1
## Heading 2
### Heading 3

## 2. Emphasis

Making your text have the required text editing set, like Bold or italics,
Example

*italic* or _italic_
**bold** or __bold__

## 3. List
Listing items on your documentation 


- Item 1
- Item 2
- Item 3

1. First item
2. Second item
3. Third item

## 4. Links
Creating links can also be done with the markdown where text in the [] will be displayed and the link will be in the ()

[Click here for more info] (https://ecom2win.com)


## 5. Images
We can use image(s) in our markdown as well. 

![Alt Text](https://example.com/image.jpg)


## 6 Snippet
To display code snipet in our markdown, we use the `` sign wh

`git checkout new-branch`














