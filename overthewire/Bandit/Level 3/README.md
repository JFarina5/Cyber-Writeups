# Bandit - Level 3
------------
>The password for the next level is stored in a hidden file in the inhere directory.
------------

## Write-up
For this level, we follow the same procedure as previous levels which involves the `ssh` command followed by the appropriate address for bandit3 on port 2220:

```
root@kali:~# ssh bandit3@bandit.labs.overthewire.org -p 2220
```

We enter the password for this level, which was the flag in bandit2:

```
root@kali:~# ssh bandit3@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit3@bandit.labs.overthewire.org's password: 
```

When in the system, we use the `ls` command to view the contents of this system:

```
bandit3@bandit:~$ ls
inhere
```

Once the command is used, we see there is the directory *inhere*. From here we use the command `cd` in order to enter the directory:

```
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ 
```

Once in the directory we can attempt to use the `ls` command the view the contents of this directory, but we are returned with no values:

```
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ 
```

In order to view everything in this directory we can use the `find` command, which returns us with a *hidden* file:

```
bandit3@bandit:~/inhere$ find
.
./.hidden
```

From here we can use the `cat` command to view the contents of this hidden file, which presents us with the flag for this level:

```
bandit3@bandit:~/inhere$ cat ./.hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```

The password for bandit3 is `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`
