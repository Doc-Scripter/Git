# Local and remote repositories

## In the work/ directory, make a clone of the repository hello as cloned_hello. (Do not use copy command)
````bash
git clone hello cloned_hello
````

## Show the logs for the cloned repository.
````bash
git log
````

## Display the name of the remote repository and provide more information about it.
````bash
git remote origin show
````

## List all remote and local branches in the cloned_hello repository.
````bash
cd cloned_hello/
git remote -v
````

## Make changes to the original repository, update the README.md file with the provided content, and commit the changes.
````bash
nano README.md 
git add README.md 
git commit -m "feat:upadte contents in README.md"
````

## Inside the cloned repository (cloned_hello), fetch the changes from the remote repository and display the logs. Ensure that commits from the hello repository are included in the logs.
````bash
cd cloned_hello/
git fetch
git log -all
````
## Merge the changes from the remote main branch into the local main branch.
````bash
git merge origin/main
````
## Add a local branch named greet tracking the remote origin/greet branch.
````bash
git checkout -b greet origin/greet
````
## Add a remote to your Git repository and push the main and greet branches to the remote.
````bash
git  remote add master https://learn.zone01kisumu.ke/git/cliffootieno/git
git push -u master main greet
````
## Be ready for this question in the audit!
### "What is the single git command equivalent to what you did before to bring changes from remote to local main branch?"
````bash
git pull
 ````