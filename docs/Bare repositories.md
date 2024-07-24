 # Bare repositories

## What is a bare repository and why is it needed?

* A bare repository is a Git repository that does not have a working directory. It is typically used as a central repository that collaborators push and pull from.

## Create a bare repository named hello.git from the existing hello repository.
````bash
git clone --bare ../hello hello.git
````
## Add the bare hello.git repository as a remote to the original repository hello.
````bash
git remote add origin hello.git/
````
## Change the README.md file in the original repository with the provided content:
````bash
nano README.md 
````

## Commit the changes and push them to the shared repository.
````bash
git add README.md 
git commit -m "Update:changed content in README.md"
git push origin
git push --set-upstream origin main
````
## Switch to the cloned repository cloned_hello and pull down the changes just pushed to the shared repository.
````bash
cd cloned_hello/
git pull origin main
````
