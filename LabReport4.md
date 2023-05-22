# Lab Report 4

This Lab Report consists of 6 steps that is Step 4 to Step 9.

## Step 4 - Log into ieng6

<img src="step4.png" width="70%" hieght="70%">

Keys pressed: `ssh cs15lsp23eh@ieng6.ucsd.edu <enter>, Password: <enter>` By this I successfully logged into my ieng6 account. These commands are accessing my CSE 15L course specific account and then asking me for my password to help me log into my account.

## Step 5 - Clone your fork of the repository from your Github account

<img src="step5.png" width="70%" hieght="70%">

Keys pressed: `git clone https://github.com/ucsd-cse15l-s23/lab7 <enter>` By putting in the `git clone` command I am able to clone any repository I have forked. Therefore, after putting in the `git clone` command I put in the url of the repository I want to clone, and it gets cloned onto my device. I can then press `cd lab7` to change the current directory to `lab7` so that I can access all the files inside that directory.

## Step 6 - Run the tests, demonstrating that they fail

<img src="step6.png" width="70%" hieght="70%">

Keys pressed: `javac ListExamples.java ListExamplesTests.java <enter>` Here by pressing `javac` I can run the files to make sure they do not have any errors. However, in the picture above we can see that there are 6 errors in the file and therefore we need to edit the `ListExamples.java` file to correct the errors and make sure the file runs.

## Step 7 - Edit the code file to fix the failing test

<img src="step7.png" width="70%" hieght="70%">

Keys pressed: 
1. `vim ListExamples.java` The command `vim` lets me modify the file `ListExamples.java` and correct the errors. Now, by using `vim` commands I will be correcting line 44 where the error is caused, that is instead of `index1` it should be corrected to `index2`.
2. `:44 <enter>` This `vim` command takes my cursor to line 44 where the error is present.
3. `<l><l><l><l><l>` By pressing `l` 5 times, I am able to move my cursor to the right 5 times so that I am on the `1` in `index1` on line 44.
4. `x` This command will remove `1` from `index1`.
5. `i` This command enters insert mode and will help me insert a character at the place where my cursor is which is after `x` in `index`.
6. `2 <esc>` By this I am inserting `2` after `index` which makes it `index2` and then I am pressing `<esc>` to exit from the insert mode back to normal mode.
7. `:wq` By pressing this last command, I am able to save the changes I made and quit out of `vim` back to my terminal. `w` saves the changes and `q` quits from `vim`.

## Step 8 - Run the tests, demonstrating that they now succeed

<img src="step8.png" width="70%" hieght="70%">

Keys pressed: `<up><up><up><up>`

## Step 9 - Commit and push the resulting change to your Github account 

<img src="step9.png" width="70%" hieght="70%">

Keys pressed:
