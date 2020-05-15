# :star: git-cheatsheet  :star:

This Repository is a guide to all the git commands you need to use in case any of these situations arise

## Basic Commands :v:

- Clone a Repository
```sh
 git clone https://github.com/CodeChefVIT/git-cheatsheet.git

 Replace  url with your required repository url  
```

- Pushing to a Repository
```sh
  git add .
  git commit -m <commit message>
  git push origin master

  To add just one file or a set of files replace the . with your filename in first command
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

## Update forked Repository with original Repository
  
