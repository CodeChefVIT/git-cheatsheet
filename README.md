# :star: git-cheatsheet  :star:

This Repository is a guide to all the git commands you need to use in case any of these situations arise

## Basic Commands :v:

- Clone a Repository
```sh
git init

 Turn an existing directory into a git repository

git clone https://github.com/CodeChefVIT/git-cheatsheet.git

 Replace  url with your required repository url  
```
- Set username and emailId
```sh
   git config --global user.name "FIRST_NAME LAST_NAME"
   
   git config --global user.email "MY_NAME@example.com"
```
- Pushing to a Repository
```sh
  git status
    show modified files in working directory, staged for your next commit
  
  git add .
  git commit -m <commit message>
  git push origin master
   
   To add just one file or a set of files replace the . with your filename in first command
  
  git diff
    diff of what is changed but not staged
  git diff --staged
    diff of what is staged but not yet commited
  git commit -m “[descriptive message]”
    commit your staged content as a new commit snapshot
  
```

- Check where is your Repository remote 
```sh
  git remote -v

  Output should have the repository url similar to this 

  origin	https://github.com/CodeChefVIT/git-cheatsheet.git (fetch)
  origin	https://github.com/CodeChefVIT/git-cheatsheet.git (push)

```

- Change Remote 
```sh
git remote set-url origin <new git url>

```

- Check logs
```sh 
    git log 
   
   Output should be something similar 

    commit 82e2a7c46a96b3b4aaf5acbc0cbc218d118aa922
    Author: <User> <45638240+<User>@users.noreply.github.com>
    Date:   Fri May 15 14:52:32 2020 +0530

    <Commit Message>
```

- Tracking changes 

```sh
  git diff
    To track the changes that are yet to staged.

    git diff --staged
      To track the changes that are staged but not committed.
    
    git diff HEAD
      To track the changes after committing a file.
        
    git status
      To know the state of the files in local directory.
    
    git show
     To show all the changes made in the file for each commit
     
```

 - Ignoring files

```sh 

    Git can ignore specified files from adding into the remote repository using     gitignore. 
    
    Create .gitignore in the project
    
     vim .gitignore 

```
Add the filename/directory you want to ignore by the git in the gitignore file
    
    node_modules  

now, when you add the files it ignores node_modules directory in your project.




## Branches :deciduous_tree:	

- Create new branch
```sh
   git checkout -b newbranch

   Replace newbranch with your branch name
```

- Check current branch
```sh
   git branch

   This should list all your branches and highlight the current branch in green
```

- Switch to new branch
```sh
   git checkout newbranch

```

- Push in new branch
```sh
    git add .
    git commit -m <commit message>
    git push origin <branch name>

```

## Update forked Repository with original Repository  :hourglass:	

  These steps are to be followed when your forked repository is few commits behind original repository

```sh

  - Add original repository url here 

    git remote add upstream https://github.com/whoever/whatever.git

  - Fetch all branches of the repository

    git fetch upstream

  - Make sure you are on master branch

    git checkout master

  -  Rewrite your master branch so that any commits of yours that aren not already in upstream/master are replayed on top of that other branch

    git rebase upstream/master

    This should update your forked repository with original repository

    However if you do not want to rewrite history of master branch then replace last command with this

    git merge upstream/master
    
 

```

## Your dev branch is X commits behind and Y commits ahead of master fix 

```sh
  git checkout master

  git fetch origin master
 
  git checkout dev

  git rebase origin/master

  git checkout master

  git merge --no-ff dev
  
  If you get this message  'Automatic merge failed; fix conflicts and then commit the result'
  
  Check for merge conflicts in code and fix them (master branch should have required files now)
  
  For any such message deleted in  'dev and modified in HEAD. Version HEAD of requirements.txt left in tree' 
  
  File can either be deleted or modified or kept same
  
  git pull origin master (if warning comes)
  
  add , commit , push 


```
## Short hands 

```sh
    git commit -am <message> 
      adds and commits the changes in a single command

```

```sh
    git push -u origin <branch name>
      use -u (upstream) for pushing your first commit changes into the remote repository
      and later on you avoid origin <branch name>

   git push 
      works fine till the last commit    

```

```sh
    git diff > difference.txt
      If you are feeling hard to track all the changes on console 
      above helps to writes/pipes the differences into specified file (difference.txt) and you can track the changes
      easily
```
## GitHub CLI commands:
```sh
1. gh issue list
View and filter a repository’s open issues.

2. gh pr status
Check on the status of your pull requests.

3.  gh pr checkout
Check out pull requests locally.

4. gh pr create
Create a new pull request.

5. gh pr checks
View your pull requests’ checks.

6. gh release create
Create a new release.

7.  gh repo view
View repository READMEs.

8. gh alias set
Create a shortcut for a gh command.
```
