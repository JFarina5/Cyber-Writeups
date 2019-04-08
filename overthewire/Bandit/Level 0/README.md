# Bandit - Level 0
------------
> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

------------

## Write-up
The purpose of this level is to log in to the system and, easily acquire our first flag. To begin with, start by entering the `ssh` command behind the bandit0/overthewire address, followed by the appropriate port number of 2220 with the `-p` command:

```
root@kali:~# ssh bandit0@bandit.labs.overthewire.org -p 2220
```
After entering the address, you will be prompted to enter a password. From the description of the level, we know that the password is bandit0:

```
root@kali:~# ssh bandit0@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password:
```
Once in the system, we will use the `ls` command in order to see what files and directories are located within this system. Once we use this command, we see that there is one *readme* file:
```
bandit0@bandit:~$ ls
readme
```
In order to view this file, we will use the `cat` command. After using this command, we are presented with the flag for level 0:
```
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```
Thus completing level 0, allowing us to move on to level 1.  
The flag for bandit0 is `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`
