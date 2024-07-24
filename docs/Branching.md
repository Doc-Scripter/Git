# Branching
## Create and Switch to New Branch:
### Create a local branch named greet and switch to it.
````bash
git checkout -b greet 
````
### In the lib directory, create a new file named greeter.sh and add the provided code to it. Commit these changes.
````bash
cd lib/
nano greeter.sh
git add greeter.sh 
git commit -m "file org:created greeter.sh file"
````

## Update the lib/hello.sh file by adding the content below, stage and commit the changes.
````bash
nano hello.sh 
git add hello.sh 
git commit -m "update:changed content in hello.sh"
````

##  Update the Makefile with the following comment and commit the changes.

````bash
nano Makefile 
git add Makefile 
git commit -m "update:changed content in Makefile"
````

## Switch back to the main branch, compare and show the differences between the main and greet branches for Makefile, hello.sh, and greeter.sh files.
````bash
git checkout main 
git diff main greet -- Makefile lib/hello.sh lib/greeter.sh
````
## Generate a README.md file for the project with the provided content. Commit this file.
````bash
echo "This is the Hello World example from the git project.">README.md
git add README.md 
git commit -m "file org:created README.me"
````

## Draw a commit tree diagram illustrating the diverging changes between all branches to demonstrate the branch history.
````bash
git log --graph  --all
````



