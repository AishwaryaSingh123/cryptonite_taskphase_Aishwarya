# Permissions and Ownership
## Changing File Ownership
### Description
In this challenge, we learned how to change the ownership of a file using the chown command.
### Thought Process
We started by checking the current ownership of the /flag file to understand who has access and then changed it to our user to gain access.
### Solution
```
ls -l /flag
chown hacker /flag
ls -l /flag
cat /flag
```
After changing the ownership, I successfully got the flag.
##
## Groups and Files 
### Description
This challenge taught us how to change the group ownership of a file using the chgrp command.
### Thought Process
The goal was to determine our user’s group and then change the group ownership of the /flag file to that group.
### Solution
```
chgrp hacker /flag
cat /flag
```
This allowed me to get the flag
##
## Fun with Group Names
### Description
In this challenge, we learned how to identify our own group name using the id command and change the group using the chgrp command.
### Thought Process
I needed to check my group ID and use it to change the group ownership of the /flag file.
### Solution 
```
id
chgrp grp4474 /flag
cat /flag
```
After running this, I successfully got the flag.
##
## Changing Permissions
### Description
This challenge focused on changing file permissions using the chmod command.
### Thought Process
I needed to modify the permissions of the /flag file to allow read, write, and execute access.
### Solution
```
chmod ugo+rwx /flag
cat /flag
```
##
## Executable Files
### Description
In this challenge, we learned how to allow a user to execute a file using the chmod command.
### Thought Process
I needed to make the /challenge/run file executable to run it and access the flag.
### Solution
```
chmod u+x /challenge/run
/challenge/run
```
After executing the command, I got the flag.
##
## Permission Tweaking Practice
### Description
In this challenge, we practiced using the chmod command to adjust file permissions step by step.
### Thought Process
I analyzed the current permissions and made changes to meet the required permissions for the challenge.
### Solution
```
/challenge/run
chmod g+wx,o+wx /challenge/pwn
chmod u-r,g-rx /challenge/pwn 
chmod o-x /challenge/pwn
chmod o+x /challenge/pwn
chmod u+rx,g+rx /challenge/pwn
```
After completing all rounds, I accessed the flag.
## 
## The SUID Bit
### Description
In this challenge, we learned how to add the Set User ID (SUID) using the chmod u+s command.
### Thought Process
Setting the SUID bit would allow the program to run with the privileges of the file owner, enabling us to access restricted operations.
### Solution
```
chmod u+s /challenge/getroot
/challenge/getroot
```
This provided me with a root shell, and I accessed the flag.
