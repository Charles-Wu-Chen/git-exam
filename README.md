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


git checkout development
git merge feature_branch
git checkout master
git merge develop
git branch -d feature_branch