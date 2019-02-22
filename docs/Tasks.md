## How to send Home work
1. Create fork from the main repository https://github.com/pluhin/sa.it-academy.by
2. Clone forked repository to your workstation
3. Checkout to branch <YOR_GROUP_BRANCH>
4. Create folder with your Name_LastName (As example: In my case name will be `Siarhei_Pishchyk`). This folder will be your report folder.
5. Create folder with name of your homework (Example: `02.Git.Local`)
6. Put your files into it.
7. Make commit and push
8. On WebUI (github) make PR (Pull Request) into main fork and branch <YOR_GROUP_BRANCH> from your fork and your <YOR_GROUP_BRANCH>
9. Wait for review

## 01. CI/CD
Registration on slack and join to the chanel
- https://sa-itacademy-by.slack.com

Please create account on the following git hosting systems
- https://github.com/
- https://gitlab.com/users/sign_in
- https://bitbucket.org 

Install the following applications:

- GIT: https://git-scm.com/downloads
- VirtualBox: https://www.virtualbox.org/wiki/Downloads
- Vagrant: https://www.vagrantup.com/downloads.html
- Visual Studio Code: https://code.visualstudio.com/download

## 02. GIT. Local
Initialize local repository on your laptop. Create the following branches:

- master (init) 
    - 2 commits
- dev (from master) 
    - 2 commits from master + 2 additional 
- features/do_one (from dev)
    - 2 commits from master + 2 additional  form dev + 1 additional
- hotfix/we_gonna_die (from master)
    - 2 commits from master + 1 additional

Pay the following situations:
- Release phase - all commits should be inside master (except hotfix)
- Hotfix deploy - commit from hotfix/we_gonna_die branch should be in master first, then in another branches too

All your commands put into files 02.GIT.Local.md and add to your repository, then prepare PR (Pull Request)
> Use git markup to organize your text/output

**Additional:** Create README.md with project description in your folder on your github repository

## 03. GIT hosting
Github/Gitlab/Bitbucket
- Create remote empty repositories
- Add ssh key(s)
- Synchronise with with your local repository from previous task
- Add project into remote repositories each all, one by one
- Create slack/email integration push/commit events

All your repository urls put into files `03.GIT.Hosting.md` and add to your repository, then prepare PR (Pull Request)

Gitlab CE deployment
- Deploy Gitlab
- Setup access and email notification
- Create project
- Check difference between EE and CE
- Send me invitation by Gitlab notificator 

## 04. Ansible start
Deploy Ansible on any your localhost (Ubuntu/CentOS)
- Setup existing local user to run commands without password 
    - apt/yum upgrade
- Run command for upgrade locally using ansible add-hoc commands

Connect to the remote host
- Using Vagrant deploy two host
    - Ubuntu 18.04
    - CentOS 7.5
- Setup hosts for connection without password
- Allow ansible user upgrade system
    - Create new user
    - Apply sudo rules for its
- Using ansible need to do
    - Connect to the hosts
    - Print out host names and IP
    - Upgrade packages
- Create own inventory with all variables and hierarchie 

Output all your ansible commands (and commands also) put into `04.Ansible.start.md` and add to your repository, then prepare PR (Pull Request)

## 05. Ansible run 
- Create playbook to print out remote host parameters
    - OS/version
    - Mount point/capacity/used
    - RAM/capacity/free
- Playbook for the ansible user
    - Create new user (use module)
    - New user authorisation only by key
    - Add to the sudo:nopasswd for upgrade command
    - Implement test of that

All your  playbook put into folder `05.Ansible run` and create file `05.Ansible run.md` with description of your ansible roles (What it does, examples of command/parametrs) and add to your repository, then prepare PR (Pull Request)
