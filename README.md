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
