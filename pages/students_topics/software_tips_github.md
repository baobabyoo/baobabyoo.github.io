---
layout: default
title: Github
parent: Software Tips
grand_parent: To my students
nav_order: 1
---

### 1. General user
[Github](https://github.com/) is an online interface for programmers to maintain the versions of their codes, to share the codes to their colleagues, or to co-develop. It is getting more and more important to at least know some basic commands of using it.
{: .fs-2 }

To download the publicly available codes, you can simply enter the following command to the Linux command line, for example:
{: .fs-2 }

```
git clone https://github.com/baobabyoo/almica.git
```
{: .fs-2 }

You can find the web address of the codes you want to download by going to its Github webpage, e.g., `https://github.com/baobabyoo/almica` (you may know it by searching it, via sharing from your friends/colleagues, or suggestions of chatGPT). Click the green button `<> Code` then you will find the HTTPS, SSH, or Github CLI links (I mostly only use the former two).
{: .fs-2 }

### 2. Developer

To behave as a code developer (e.g., to be authenticated to edit/upload/delete codes/repositories or to own a private repository), you first need to register an account. Then you will need some setups.
{: .fs-2 }

#### 2.1 setting SSH Key

Login to your github account. Click the icon on the top right of the webpage to find the **Settings** tab. Find the **SSH and GPG keys** tab on the left and click it. If you have never done this, please carefully follow the guide [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to generate it and paste the public key to github. If you have done this before, the Linux commands you want to use are provided below:
{: .fs-2 }

```
# generating ssh keys
ssh-keygen -t ed25519 -C "your_email@example.com"

# prompt the SSH public keys
cat ~/.ssh/id_ed25519.pub
```
{: .fs-2 }

Remember to copy the public key to the github page (i.e., clicking **New SSH Key**).
{: .fs-2 }

In Linux, you can manually activate the SSH key agent by entering `eval "$(ssh-agent -s)"` in the command line, and then add your SSH private key to the agent by typing `ssh-add ~/.ssh/id_ed25519`. I normally set *alias* to make it easier to do these, e.g., in `~/.bashrc`, including
{: .fs-2 }

```
alias sshstart='eval "$(ssh-agent -s)"'
alias sshgit='ssh-add ~/.ssh/id_ed25519'
```
{: .fs-2 }

After setting these up, you can *git clone* your private repositories if you choose the *SSH* link in `<> Code`.
{: .fs-2 }

#### 2.2 setting Developer token

This is alternative to setting SSH keys. In **Settings**, instead of going to *SSH and GPG keys*, click **Developer settings** and then click **Personal access token**. Click **Token (classic)** then you can find **Generate new token** on the upper right. Copy this token to the clipboard or any place you can conveniently copy and paste.
{: .fs-2 }

Then in any connection (e.g., http), when the prompted message request you to enter your username and password, you can enter your username this token, instead of your password (using your own password will not work).
{: .fs-2 }

#### 2.3 Some commands

```
# Pushing a code to your own github repository
git add ./code.py
git commit -m "first commit"
git branch -M main
git checkout <branch>
git remote add origin git@github.com:YOURID/myPythonPackage.git
git push -u origin main

# Reset the url to push
git remote set-url origin git@github.com:User/UserRepo.git

# removing files (do the following and commit as usual)
git rm filename

# resetting identity
git config --global user.name "YOUR USERNAME"
git config --global user.email "YOUR EMAIL"

# list information
git config --list

# catch the token in my computer
$ git config --global credential.helper cache
```
{: .fs-2 }
