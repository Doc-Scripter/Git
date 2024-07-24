# Git commits to commit
## Within the work directory, establish a subdirectory named hello


````bash
cd work
mkdir hello
````
## Inside this directory, generate a file titled hello.sh and input the following content:
````bash
cd hello
>hello.sh;nano hello.sh
````
## Initialize the git repository in the hello directory.
````bash
git init
````
## Check the status and act accordingly with the output of the executed command.
````bash
git status
git branch -m master main
````

## Change the hello.sh content 
````bash
 nano hello.sh
````

## Stage the changed file and commit the changes, the working tree should be clean.
````bash
 git add hello.sh 
 git commit -m "update:first commit"
 cat hello.sh
 ````
 ## Modify the hello.sh file to include comments and stage it. 
 ````bash
 nano hello.sh 
 ````
## Make two separate commits: 
 #### The first commit should be for the comment in line 3.
````bash
 git add -p hello.sh 
 e
 git commit -m "comment:adding comment to hello.sh"
 git status
 ````
 ### The second commit should include changes made to lines 4 and 5.
 ````bash
 git add hello.sh 
 git commit -m "update:including the rest of the logic"
 ````
 