# 2420-Assignment-2
## Table of Contents
- [Introduction](#introduction)
- [Project 1](#project-1)
- [Project 2](#project-2)

## Introduction
In this repository, you will find two folders named **project1** and **project2**, each containing shell scripts with distinct functions. **project1** will install packages and set up and new system, and **project2** will allow you to create a new user.

To get started, you need to have git installed in your system.
Use the following command to install git:
```
sudo pacman -S git
```
change to your home directory then use the following command to clone the repository:
```
git clone https://github.com/Abungo-w/2420-assignment-2.git
```
After its done cloning, a folder named 2420-assignment-2 should appear in your home directoy. 

## Project 1
Going into the the **project1** folder, you will find 4 files:
- install-packages: a shell script that will install the packages listed in the _package_ file.
- packages: a file with a list of [packages](#installing-packages) you will install when you run the _setup_ file with the `-i` option.
- sym-links: a shell script that clones a configuration file repository and sets up symbolic links in your home directory
- setup: a shell script that runs _install-packages_ and _sym-links_ scripts

***Caution**: Do not run any file execpt for **setup**. Weird things might happen!

**note**: You can add or remove the packages in the _packages_ file you want to install, but do not remove the **kakoune** and **tmux** package. They are required to use the cloned repository configuration files in the config directory.

You will need to give executable permission to _install-packages_, _sym-links_, and
_setup_ in order to run the script.
Use the following command to give the files permission:
```
chmod +x install-packages sym-links setup
```
***Caution**: Do not run any file execpt for **setup**. Weird things might happen!

### Running the script
Now you are ready to run the setup file. Use the following command to see the options you can do with the _setup_ script:
```
sudo ./setup -h
```
**Note**: if you are the root user you don't need to use the sudo command.

Use the following command for a full setup:
```
sudo ./setup -il
```

### Installing packages
The packages you will be installing:
- kakoune
- tmux
- neovim

**note**: You can add or remove the packages in the _packages_ file you want to install, but do not remove the **kakoune** and **tmux** package. They are required to use the cloned repository configuration files in the config directory.

Use the following command to only install packages:
```
sudo ./setup -i
``` 

## Project 2
Going into the **project2** folder you will find a file named _new-user_.
The _new-user_ file will create a new user with:
- a password
- user's home directory
- contents of the  /etc/skel in their home directory
- option to specify the user's shell.  (/bin/bash will be the defualt shell)
- option to add additional groups to the user. ("wheel" will be the defualt group)

First, You will need to give executable permission to _new-user_ in order to run the script.
Use the following command to give the file permission:
```
chmod +x new-user
```
Use the following command to see the options you can do with the _new-user_ script:
```
sudo ./new-user -h
```
Note: if you are the root user you don’t need to use the sudo command.

Use the following command to create a new user with default setup:
```
sudo ./new-user -u <username>
```
