# GitLab

## List
- [What is GitLab](#What-is-GitLab) 
- [Starting Config](#Starting-Configuration)
- [Push Local Files](#Push-existed-project)
- [Fork a Project](#Fork-a-project)
- [Setup SSH Key](#Setup-SSH-Key)
- [GitLab Runner](#GitLab-Runner)
- [GitLab CI/CD](#GitLab-CICD)

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

## Fork a project
```
A fork is a copy of a project.
Forking a pro/repo allows you to make changes without affecting the original project
```
- First click the 'fork' button in repo, if no available namespace, create your group then fork.
- Then go to 'Merge Requests' to merge into the original project

## Setup SSH Key
- SSH - Secured Shell
    + Used for authentication
    + By setting ssh key you can connect to GitLab server without using username and password each time

- Generate SSH key (Mac: use terminal. Windows: use putty or git bash)
```
ssh-keygen
```
- Login to GitLab > Account > Settings > SSH Keys > Copy 'id_rsa.pub' and paste in 'Key' > Add Key

## GitLab Runner
- What is GitLab Runnber
    + Used in GitLab CI
        * Open source continuous integration service included with GitLab
    + Used to run jobs & send results back to GitLab
## GitLab CI&CD
- What is GitLab CI/CD
    + GitLab CI is an open source CI service included with GitLab Since ver-8.0
    + Continuous Integration: DEV > Application Test > Integration Test
    + Continuous Delivery:    DEV > Application Test > Integration Test > Acceptance Test
    + Continuous Deployment:  DEV > Application Test > Integration Test > Acceptance Test > Production
- Add .gitlab-ci.yml in the root folder of your project/repo
```
demo_job_1:
     tags:
       - ci
     script:
       - echo Hello World
```
- Commit and push file to gitlab repo
- Create GitLab runner for the project
- Start the runner
- Make any change in the project > commit > push
