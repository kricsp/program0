# CS580u Programming and System Tools
## Fall 2018
### PROGRAM 0 README FILE

## KNOWN BUGS AND INCOMPLETE PARTS:
- What parts of the program you were not able to complete

## REFERENCES:
- List any outside resources used

## MISCELLANEOUS COMMENTS:
- Anything you would like the grader to know

# Assignment Description
## Program 0 - Getting Familiar with Your Environment
### Due Date: 5:00 p.m., August 31st, 2018

*All programs will be tested on the machines in the Q22 lab. If your code does not run on the system in this lab, it is considered non-functioning EVEN IF IT RUNS ON YOUR PERSONAL COMPUTER. Always check that your code runs on the lab machines before submitting.*

### Driver Code and Test Files

* program0.c

### Grading Rubric

**_TOTAL: 10 points_**
* **Part B: 8 points**
    * Must have at least 2 commits (3 points)
    * Must have at least 1 issue posted (3 points)
    * Google form submitted (2 pts)
* **Part C: 2 points**
    * Follows requested program structure and submission format

### Guidelines

This is an individual assignment. You must do the vast majority of the work on your own. It is permissible to consult with classmates to ask general questions about the assignment, to help discover and fix specific bugs, and to talk about high level approaches in general terms. It is not permissible to give or receive answers or solution details from fellow students.

You may research online for additional resources; however, you may not use code that was written specifically *to* solve the problem you have been given, and you may not have anyone else help you write the code or solve the problem. You may use code snippets found online, providing that they are appropriately and clearly cited, within your submitted code.

*By submitting this assignment, you agree that you have followed the above guidelines regarding collaboration and research.*

__In this program, you will learn to__:

* Write and execute a simple c program in a command-line environment
* Use `git` to manage your programs and submit your work for grading.

Look for these icons!

| | Meaning |
|:----:|---------|
| :bulb: | Tips and useful information |
| :warning: | Caution! This could cause you problems. |
| :no_entry_sign: | Danger! Don't do this! |

## Part A: Writing the Code
The first thing we are going to do is learn how to work with git and Github.
First, let's set up our git credentials. Enter the following two commands in the terminal:

`git config --global user.name "Firstname Lastname"`

`git config --global user.email "email@binghamton.edu"`

:warning: **Replace `Firstname Lastname` and `email@binghamton.edu` with your information**

In your program directory, you are going to clone this repository to get a copy of the source code onto your account. To do this, you will first need to have signed up for a Github account if you didn't already have one.

### Github
You will need a Github account to submit your programs. You will also use your Github account any time you need help with your code. If you do not already have one, you can go to [Github](https://github.com) and sign up.

Once you have signed up for an account, fill out and submit the following google form:
[https://goo.gl/forms/TeleAPwdN9znIJWH2](https://goo.gl/forms/TeleAPwdN9znIJWH2)

:warning: You must log in with your bmail to use the form.

When you click on the link to fork your own repo of Program 0, Github will set things up for you.

:warning: :warning: :warning: :warning: :warning: :warning:

**It is extremely important that you do not interrupt the setup process. It can sometimes take up to 5 minutes to set everything up depending on Github's current server load. If you interrupt the process, we will have to manually fix it for you.**

:warning: :warning: :warning: :warning: :warning: :warning:

Once the fork has completed setting up, look at the Github landing page for your fork of this program. You should see a green button that says "Clone or download". Press it and you should see a URL like https://github.com/binghamtonuniversity-cs342/program-0-fall18-username.git. Copy that text somewhere you can access it, then go back to the terminal.

Next, be sure you are in your program directory and execute the following command in the terminal:

`git clone URL`

:bulb: *where URL is the copied text ending in ".git".*

We will explore git workflows in-depth later in this lab.

Now that we have our repository set up, we will edit the code. Change your directory to the cloned repository.

You can use any editor you like for editing c programs. Some that I recommend:
* Atom (my personal favorite)
* gedit
* vim

If you cloned the git repository correctly, you should have a `program0.c` file with the following contents:

```c
#include <stdio.h>

int main(){
    printf("Hello World");
}
```

Change the file to print, "Hello world from `your name`".

Save and run the file with gcc using the following commands:
```shell
gcc program0.c
./a.out
```

### Submitting an issue
What if you have a problem with your code? That's what we are here for, and Github makes it easy to get help.
* Navigate back to your repo on Github. One of the tabs is labeled **issues**. Click on this tab.
* You should see a green button labeled **New Issue**. Click on this button to create a new issue.
* Submit your issue by providing the following:
    * Title - should be descriptive of the problem
    * In the body provide
        * Filename
        * Line number(s)
        * Description of the issue
* After you submit your issue, you can click on the ellipses (...) in the top right corner, and select **CopyURL**. You can then post this URL on Piazza (_you don't need to post the issue on Piazza this time_).

:warning: This is always the process for getting help with your code. If you copy and paste code into Piazza or just link to your repo without creating an issue, we will ask you to create an issue first, which will delay how quickly we can help you.

## Part C: Submission
* Required code naming and organization:
    * program0.c

:no_entry: Every program will have a required submission guidelines. Please read submission requirements carefully. Any deviations from specifications on future programs will result in point deductions or incomplete grades.

## README

You should have notice that part of this readme file has three sections titled:
* KNOWN BUGS AND INCOMPLETE PARTS
* REFERENCES
* MISCELLANEOUS COMMENTS

Before your final submission, edit the content for each of these sections in this README for your program. You do not have to use markdown, but you can find out more about markdown [here](https://guides.github.com/features/mastering-markdown/) if you would like to.

### Git

In this and future programs, we will use Github Classroom repositories. You have already [forked](https://help.github.com/articles/fork-a-repo/) this repository when you accepted the emailed link. That makes a copy of the repository, free for you to make changes. Then you cloned your forked repository to get a working copy onto this machine.

Now that we have made local changes to our working copy, let's [commit](https://git-scm.com/docs/git-commit) those changes to the repository:

:warning: *These commands all presume that your current working directory is within the directory tracked by `git`.*

```shell
git commit -a -m "first commit"
```

The `-a` says that git should add all tracked files with changes to your commit, and the `-m` says the next string contains the commit message, which is required by git any time you make a commit.

What about _untracked files_? Run the following commands:

```shell
touch info.txt
git status
```
You'll notice that `git` tells us that `info.txt` is an _untracked file_. That means it's not being tracked by the repository. Let's fix that by [adding](https://git-scm.com/docs/git-add) it.

```shell
git add info.txt
git commit -a -m "Added info.txt file"
```
:warning: *You* __must__ *add any new files you create to the repository with the `git add` command or they will not upload to the repo, and your code will not work.*

Once we've made the commits for a given coding session, we need to add those to the repository by performing a [push](https://git-scm.com/docs/git-push):

```shell
git push
```

Lastly, the next time we begin a coding session, we will need to [pull](https://git-scm.com/docs/git-pull) to ensure we have the most updated working copy.

```shell
git pull
```
:bulb: You should get a message that you are already up to date.

This will allow you to keep your code in the lab and on your own computer synchronized if you want to work outside of lab.

Lastly we are going to make our final commit. You will need to do this when your submission is ready for grading.

```shell
git commit -a -m "final commit message"
git push
```

:bulb: You may get a message that there have not been any changes. That's okay, that just means you have already *commited* all changes.

You can commit as often as you like, and revert your code to any previous commit using the **commit hash**. The commit hash is a long number that identifies a specific version of your code. I recommending making commits often with a comment describing the state of your code. To find your most recent commit hash, use the following command:

```shell
git rev-parse HEAD
```    
You should get a long, strange looking number:
```
35e27598324d8b4d7ddeb4d7aa8abe91c6263705
```

To complete your submission, you must copy and paste this number into mycourses. Go to MyCourses, select cs580u, and **Assignment Hash Submission**. Select Program 0, and where it says text submission, paste your commit hash. The TAs will only grade your submission that corresponds to the hash you submitted. You can update this as often as you like until the deadline.

I strongly recommend making a submission early on, even if your assignment is not 100% working, to avoid late penalties. You can resubmit as many times as you like.

:warning: You __MUST__ submit the commit hash on mycourses before the deadline to be considered on time **even if your program is completely working before the deadline**. :warning:

That's it! We've completed our work for this program. We will use this submission process for all subsequent programs.

:bulb: Useful `git` references:
- https://guides.github.com/introduction/flow/
- https://help.github.com
- https://git-scm.com/doc
