# git-exam
This repo is used for git exam

basic usage:
https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow


##A normal simple steps using git flow workflow

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

##if the pull request has conflict, 


Step 1: Checkout the source branch (feature branch) and merge in the changes from the target branch (from dev changes). Resolve conflicts (this can be done easier from IDE IMO).

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


##rebase

git checkout feature/branch1
...making changes
git rebase development
git checkout development
git merge 1adb0e3

##reset



git reset is equivalent to executing git reset --mixed HEAD

If you need to remove from the staging area, use
git reset HEAD <file>
Default is —mixed will reset in staging area from HEAD

Discard the local changes
—hard will reset local directory
using git reset --hard.
git reset --hard origin/<branch_name>


##diff

Summary:
There are 3 places/stages holding code

1 local working directory. (Red color)
2 stage area /cached / green files/ index/ after run "git add ."
3 HEAD/ last commit / after run “git commit -m …"

Git diff —cached  2 vs 3
Git diff 1 vs 2
Git diff HEAD 1 vs 3



//  compare the working directory with local repository.
    git diff HEAD [filename]

    // compare the working directory with index.
    git diff [filename]

    // compare the index with local repository.
    git diff --cached [filename]

Check the difference between Local repo with Remote repo(2 points)
git diff origin/<branch>


