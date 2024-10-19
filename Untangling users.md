# Untangling Users
## Becoming root with su
### Description
In this challenge, we need to gain the root access.
### Thought process
We will use the su command and switch to the root user by entering the root password
### Solution
```
su
cat /flag
```
after su we have to enter the password given to complete authentication and then I can get the flag.
##
## Other Users with su
### Description
In this challenge, we learned how to switch to another user instead of root by providing a username as an argument to the su command.
### Thought Process
We switched to the user "zardus" to access their privileges and files.
### Solution
```
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
```
After running the command, we get the flag.
## 
## Cracking Passwords
### Description
In this challenge, we learned how to crack passwords for switching to the root user using the John The Ripper tool.
### Thought Process
We used a password hash file and the john command to find the password for the user "zardus".
### Solution
```
john /challenge/shadow-leak
```
After cracking the password, we switch user
```
su zardus
/challenge/run
```
After entering password and running command, we get the flag.
##
## Using sudo
### Description
In this challenge, we will elevate the previlages without switching users
### Thought process
We will use sudo a modification of su command.
### Solution
```
sudo cat /flag
```
After running this, I get the flag.
