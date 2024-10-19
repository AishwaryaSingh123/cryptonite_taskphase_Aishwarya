# Pondering PATH 
## The PATH Variable
### Description
In this challenge, we learned about the PATH variable, which contains directory paths where the shell searches for executable programs.
### Thought Process
By temporarily emptying the PATH variable, we observed the behavior of a command that attempted to remove a file.
### Solution
```
PATH=' '
/challenge/run
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
```
And we get the flag
##
## Setting PATH
### Description
In this challenge, we learned how to add custom paths to the PATH variable for executing commands.
### Thought Process
By modifying the PATH variable, we were able to successfully run a command.
### Solution
```
PATH='/challenging/more_commands/'
/challenge/run win
```
Running the above set of commands we get the flag
##
## Adding Commands
### Description
In this challenge, we learned how to create and execute a custom command after adjusting file permissions.
### Thought Process
By creating an executable command and modifying the PATH variable, we were able to run it.
### Solution
```
nano win
chmod +x win
PATH='/home/hacker'
/challenge/run
```
Running the above set of command, we get the flag
##
## Hijacking Commands
### Description
In this challenge, we learned how to hijack existing commands by creating a custom version of them.
### Thought Process
By creating our own version of the rm command, we intercepted its execution.
### Solution 
```
nano rm
chmod +x rm
PATH='/home/hacker'
/challenge/run
```
Upon running these command, we get the flag
