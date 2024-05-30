
# Git

ABOUT

## Installation Guide

The installation guide depends on your operating system.

### Windows

First of all, run the following command on the Command Prompt:
```
git -v
```
If something like `git version xx.yy.zz` appears, where `xx`, `yy` and `zz` are numbers, then you already have Git installed.<br>
Instead, if `git` is not recognized as command or the major version `xx` is not the desired one, then:
- Download the Git installer from the [Git offical webpage](https://gitforwindows.org/ "Install Git on Windows").
- Once the installer has started, follow the instructions as provided in the Git Setup wizard screen until the installation is complete.<br>

### Linux

On Ubuntu 22.04, Git should be already installed. You can check it by running:
```
git --version
```
If the terminal doesn't recognize the command, then install Git through the following command:
```
sudo apt-get update && sudo apt-get install git
```

## Before you start

Before starting using Git, you should configure globally a few properties of your user with:
```
git config --global user.name "your name"
git config--global user.email "your email"
```
From now on, every commit will be identified by the author with the specified name and email.<br>
