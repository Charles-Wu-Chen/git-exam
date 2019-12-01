# git-exam
This repo is used for git exam

basic usage:
https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow


A normal simple steps using git flow workflow

git checkout master
git checkout -b develop
git checkout -b feature_branch

--making change in feature branch
git add .
git commit -m "message"
git push 

git checkout develop
git merge feature_branch
git checkout master
git merge develop
git branch -d feature_branch