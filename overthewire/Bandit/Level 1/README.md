# Bandit - Level 1
------------
> The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
------------

## Write-up
We begin this level exactly the same as we did bandit0, with the `ssh` command followed by the bandit1/overthewire address on port 2220:

```
root@kali:~# ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Once again, we are prompted for a password, which we received in bandit0:

```
root@kali:~# ssh bandit1@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit1@bandit.labs.overthewire.org's password: 
```

Once in the system, we run the `ls` command in order to view the files and directories within this level:

```
bandit1@bandit:~$ ls
-
```

We see that there is one file, which is the `-` symbol. This complicates things because a hyphen symbol is interpreted in bash to refer to standard input. In order to view the contents of this file, we will need to run the `cat` command with the relative path of the file. We could also access this file with the absolute path of the file, but a relative path will work since we are still within the home directory:

```
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

Once we open this file, we are presented with the flag for level 2. Thus allowing us to move on to level 2.  
The flag for bandit1 is `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
