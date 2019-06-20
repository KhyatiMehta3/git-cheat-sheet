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
