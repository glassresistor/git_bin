Just add this to your Bash rc file

# Installation instructions

```
cd ~
git clone git@github.com:pivotbio/git_bin.git

Add this to your bashrc/profile/zrc files
export PATH=$PATH:~/git_bin
```

# Usage

## Update release and go back to release branch

```
make_fresh
```


## Create new feature branch
This updates from release then creates a new branch using the first arguement for the branch name following feature/

```
new_feature new_feature_name
```

## Create new hotfix branch
This updates from release then creates a new branch using the first arguement for the branch name following hotfix/

```
new_feature new_feature_name
```


## Review and Push recent changes
Adds new files and runs add -p to review changes.  Adds a commit and requests a comment then pushes up branch

```
new_feature new_feature_name
```


## Prep for Review
Most complex command this updates from release then reorders the changes so this branches are the most recent then allow the user the ability to squash and ammend the commit message for all commits on that branch.

This command does not push the branch so you have time to review incase it dropped important changes.

```
prep_for_review
git diff release
git status
git push origin <branch_name>
```

## Prune Local Branches
This command compares your local branches to the ones on Github and provides the ability pick which ones delete useing vi

```
prune_local_branches
```
