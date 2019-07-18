# git-cheat-sheet
Cheatsheet for git

## Push an existing Git repository
```
cd existing_repo
git remote rename origin old-origin
git remote add origin https://gitlab.com/some-project.git
git push -u origin --all
```

## Push an existing folder
```
cd existing_folder
git init
git remote add origin https://gitlab.com/some-project.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

## Create a new repository
```
git clone https://gitlab.com/some-project.git
cd some-project
nano README.md
git add README.md
git commit -m "add README"
git push -u origin master
```
## Git global setup

```
git config --global user.name "Some Name"
git config --global user.email "something@somecompany.com"
```
### Git remote - get urls
```
git remote -v
```
### Git remote - set urls
```
git remote add origin https://gitlab.com/some-project.git
```
### Git remote - push
```
git remote push -u orgin master 
```
### Git remote - add shortname url
```
git remote add some-short-name https://gitlab.com/some-other-project.git
```
### Git remote - remove url
```
git remote rm origin
```
### Git remote - Remove commit and reset head
```
git push origin +HEAD^:<remote-branch-name>
```
### Git branch - add new branch, check it out and push new branch to origin
```
git branch blah
git checkout blah
git push -u origin blah
```

### Git commits - reset to previous commit 
```
git reset --hard <commit-number>
```
### Git commits - check commits & their messages
```python
git reflog

#To see complete commits
git log
```
## Git Branching
### Git rename branch 
```
git branch -m new-name
```
### Git rename branch in remote
```
git push origin :old-name new-name
```
### Git delete local branch
```
git branch -d branch-name
```
### Git delete remote branch
```
git push origin --delete branch-name
```

## Git Undoing
### Git add file/ change commit message to previous commit 
```
git add file-name
git commit --amend
```
### Git add file/ change commit message of some other old commit 
```
git add file-name
git commit --squash old-commit-id
git rebase --autosquash -i old-commit-id
```
### Git forget tracking a file
```
#Add file's name to .gitignore
git update-index --assume-unchanged <file_name>
```
### Git re-track file
```
#Remove file from .gitignore
git update-index --no-assume-unchanged <file_name>
git add <file_name>
```
### Git add specific commit from a different branch
```
git cherry-pick <commit-hash>
```
