# Bandit - Level 0
> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

------------

## Write-up
The purpose of this level is to login to the system and, easily acquire our first flag. To begin with, start by entering the `ssh` behind the bandit0/overthewire address, followed by the approiate port number of 2220 with the `-p` command:

```
root@kali:~# ssh bandit0@bandit.labs.overthewire.org -p 2220
```
After emteromg the address, you will be prompted to enter a password. From the description of the level, we know that the password is bandit0:

```
root@kali:~# ssh bandit0@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password:
```
