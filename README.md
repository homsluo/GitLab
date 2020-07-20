# GitLab

## List
- [What is GitLab](#What-is-GitLab) 
- [Starting Config](#Starting-Configuration)

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
