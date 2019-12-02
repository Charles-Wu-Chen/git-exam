# git-exam
This repo is used for git exam

basic usage:
https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow


A normal simple steps using git flow workflow

git checkout master
git checkout -b development
git checkout -b feature_branch

--making change in feature branch
git add .
git commit -m "message"
git push --set-upstream origin feature/branch1

--the below steps will be replaced pull request and merge, 
git checkout development
git merge feature/branch1
git push --set-upstream origin development

if the pull request has conflict, 


<<<<<<< HEAD
Step 1: Checkout the source branch (feature branch) and merge in the changes from the target branch (from dev changes). Resolve conflicts.
=======
Step 1: Checkout the source branch (feature branch) and merge in the changes from the target branch (from dev changes). Resolve conflicts (this can be done easier from IDE IMO).
>>>>>>> add readme
git checkout feature/stateless-component
git pull origin development

	git pull is the same as git fetch + git merge
	'
	git pull origin master
	===
	git fetch origin
	git merge origin/master
	'
	
Step 2: After the merge conflicts are resolved, stage the changes accordingly, commit the changes and push.
git commit
git push origin HEAD



--the below steps will be replaced pull request and merge, 
git checkout master
git merge develop
git branch -d feature_branch



reset



diff


