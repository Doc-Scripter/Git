# TAG me

## Referencing Current Version:
### Tag the current version of the repository as v1.
````bash
git tag v1
````
## Tagging Previous Version:
### Tag the version immediately prior to the current version as v1-beta, without relying on commit hashes to navigate through the history.
````bash
git tag v1-beta HEAD~1
````
### Navigating Tagged Versions:
#### Move back and forth between the two tagged versions, v1 and v1-beta.
````bash
git checkout v1
git checkout v1-beta 
````
### Listing Tags:
#### Display a list of all tags present in the repository to verify successful tagging.
````bash
git tag -l
````
