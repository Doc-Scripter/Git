
# Changed your mind?

## Reverting Changes:
### Modify the latest version of the file with unwanted comments, then revert it back to its original state before staging using a Git command.
````bash
   nano hello.sh 
   git restore hello.sh
````


## Staging and Cleaning:
### Introduce unwanted changes to the file, stage them, then clean the staging area to discard the changes.
````bash
   nano hello.sh 
   git add hello.sh 
   git status
 git restore --staged hello.sh
````



## Committing and Reverting:
### Add the following unwanted changes again, stage the file, commit the changes, then revert them back to their original state.
````bash
nano hello.sh 
git add hello.sh 
git commit -m "comment:unwanted but committed"
git revert HEAD~1
git add hello.sh 
git commit -m "update:reverted back to original"
````

## Tagging and Removing Commits:
### Tag the latest commit with oops, then remove commits made after the v1 version. Ensure that the HEAD points to v1.
````bash
git tag oops HEAD
git reset --hard v1
````
## Displaying Logs with Deleted Commits:
### Show the logs with the deleted commits displayed, particularly focusing on the commit tagged oops.
````bash
git reflog
````
## Cleaning Unreferenced Commits:
### Ensure that unreferenced commits are deleted from the history, meaning there should be no logs for these deleted commits.
````bash
git reflog expire --expire=now --all
````
## Author Information:
### Add an author comment to the file and commit the changes.

````bash
nano hello.sh 
git add hello.sh 
it commit -m "update:added author"
 ````


### Oops the author email was forgotten, update the file to include the email without making a new commit, but include the change in the last commit.
````bash
nano hello.sh 
git add hello.sh 
git commit --ammend --no-edit
````
