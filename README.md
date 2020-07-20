# GitLab

## List
- [What is GitLab](#What-is-GitLab) 
- [Starting Config](#Starting-Configuration)
- [Push Local Files](#Push-existed-project)

## What is GitLab

**Git** - Version control system  
to locally track changes in your project/folder and push & pull changes  
from remote repositories like GitHubm BitBucketm GitLab

**GitLab, GitHub, BitBucket** - Cloud Services  
that allow to host your project on a remote repo & have additional features  
to help in SDLC(Software Development Lifecycle) and CI(Continuous Integration), CD(Continuous Deployment)  
e.g:   
- Managing
- Sharing
- Wiki
- Bug tracking
- CI & CD

## Starting Configuration  
- Username  
    + Set up the username in gitlab
    ```git
    git config --global user.name "xxxx"
    ```
    + Show added username
    ```git
    git config --global user.name
    ```
- Email
    + Set up the email
    ```git
    git config --global user.email "xxxx"
    ```
    + Show added email
    ```git
    git config --global user.email
    ```
- Show all your settings
    ```git
    git config --global --list
    ```
 
## Push existed project
- First go into target folder initialize it (A .git file will created)
```git
git init
```
- Check current status (Branch, Commit)
```git
git status
```
- Add File
    + Specific file
    ```git
    git add "xxxx"
    ```
    + Multiple files
    ```git 
    git add .
    ```
- Commit File
```git
git commit -m "Any Msg"
```
- Push Commited Changes (origin can change to your repository's url)
    + If you want to change authentication, in Windows "Credential" delete it or change it
```git
git push -u origin master
```
