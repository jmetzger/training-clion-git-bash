# Handle conflict in pull/merge request 

## Prerequisites 

  * You have a create a branch 
  * you have pushed that branch to github e.g. git pull origin feature/xyz 
  * you cannot merge with github/bitbucket, because you see a conflict 
  
## Conflict why ?

  * You have the conflict because the branch you want to  merge into has changes you do not have in branch
  
## How to solve ? 

  * Integrate changes from master into your branch 
  * Push again.
  * Merge, Yeah, Done ! 
  
## Walkthrough (Version 1) - most simplistic version

```
# You have conflict in pull request within github
# on your local system with branch
# feature/4711 is active 
git branch 
* feature/4711
master

# you fetch the changes online from the branch master 
# and integrate them into.your branch -> feature/4711 
git pull origin master 

# Eventually solve the conflicts now
# the push again 
git push origin feature/4711 

# Now merge the branch within the pull-request menu
```

## Walkthrough (Version 2) - If you want to do pull --rebase on feature-branch 


```
# Delete unneeded feature branch - online 

# Cleanup locally 
git checkout master 
# -D is need because did not integrate branch locally 
git fetch --prune 
git branch -D feature/4711
git pull --rebase origin master 


```
