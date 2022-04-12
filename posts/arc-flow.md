---
title: 'Arcanist Flow'
date: '2019-01-29'
readTime: '3'
---

If you are using Arcanist and Phabricator then it might be confusing of the step you need to do with the work flow. You can refer to the official documentation [here](https://secure.phabricator.com/book/phabricator/article/arcanist/). This is a suggested flow of to use git and arc togther to get the code version up to date. 

Work in branches!


#### Working in a new branch
First off make sure you are working in branches so you don't step on other people toes and work separately on your own branch that will be separate than the most up to date working code.
1. Making and checking out to a new branch. Name the branch the name of the feature you are working on.
```
git checkout -b newBranch
```
2. Code!
3. Add the changes
```
git add .
```
4. Make a commit message of what you did.
```
git commit -m ‘what you did’
```
5. If you don’t want to merge the changes to master but want to save your progress, push it up to the branch. ( It is better to do the next step instead )
```
git push origin yourBranchName
```
6. If you want it to land the changes onto master and combine your code with the code on master, start the code review process.
	

#### Code Review Process
7. 
``` 
arc diff
```
  - Now you will be thrown into vim
  - Commands you would need to know: i (key) for insert, esc (key) to exit, :wq to write and quit.
  - Under the reviewers column, navigate to the the empty space on the bottom of that column and type i (key) for insert and then type #staff  #your-project-name under the reviewer column.
  - Exit and write and quit
    - esc (key) to exit 
    - :wq  to write and quit
8. If the code gets approved, land the approved code onto the master branch 
```
git fetch origin master
```
```
git rebase origin/master
```

  - If merge conflicts 
    1. Go to each file and fixed the conflict
    2. Remove conflict syntax 
    3. Communicate with your team to help with conflicts
    4. After conflicts are resolved
    5. 
    ``` 
    git add .
    ```
    6. Do not do a commit here
    7. git rebase --continue
    8. Continue  to next step
  - arc land
9. If it gets rejected, redo steps 3-9 until approved.
10. When done with the branch and feature
  - Arc will already remove your branch so you do not have to.


#### Get the most up to date code from a branch, most likely master.
1. Go to the master local branch
  - 
  ```
  git checkout master
  ```
2. Fetch the code from phabacators master to your local master on your machine.
  - 
  ```
  git fetch origin master
  ```
3. Combine your code with what is on master
  - 
  ``` 
  git rebase origin/master
  ```
  - There will be conflicts you have two options
  - If you don’t care about your code or changes then do a git stash
    - If merge conflicts
      - Go to each file and fixed the conflict
      - Remove conflict syntax 
      - Communicate with your team to help with conflicts
      - After conflicts are resolved
      - 
      ```
      git add .
      ```
      - Do not do a commit here
      - 
      ```
      git rebase --continue
      ```
      - Continue  to next step
- Now you have the most up to date code.
```
git checkout -b newBranch
```


#### Common Problems and Solutions
- If your arc command did not work or did not prompt anything, retry the command until it does.
- If you see a dragon in your terminal, that probably means you tried to push out doing a code review. You can land your changes after you start the code review process.
