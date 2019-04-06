# Bandit - Level 2
-------------
> The password for the next level is stored in a file called spaces in this filename located in the home directory
-------------

## Write-UP

For this level we follow the same procedure as the previous levels by using the `ssh` command followed by the appropriate address for this level, which is bandit2/overthewire on port 2220:

```
root@kali:~# ssh bandit2@bandit.labs.overthewire.org -p 2220
```

Once this password for this level is prompted, we enter the flag from the previous level:

```
root@kali:~# ssh bandit2@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit2@bandit.labs.overthewire.org's password: 
```

When in the system, we use the `ls` command to view the contents of this system:

```
bandit2@bandit:~$ ls
spaces in this filename
```

We are presented with quite a strange file name. At first glance we could try to enter the `cat` command against the '*spaces in this filename*' file, which gives us: 

```
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
```

We receive this error because the `cat` command is being used against every argument that is followed by a space. In order to open this file, we must make this phrase one argument. We achieve this by treating this phrase as a string and wrapping it in quotes:

```
bandit2@bandit:~$ cat "spaces in this filename"
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

Now we are able to view the contents of this file and receive our flag for bandit2, allowing us to move on to bandit3.  
The password for bandit 2 is `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`
