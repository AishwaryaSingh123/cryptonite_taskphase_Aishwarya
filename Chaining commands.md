# Chaining Commands
## Chaining with Semicolons
### Description
In this challenge, we need to execute multiple commands (/challenge/pwn and /challenge/college)
### Thought Process
By chaining commands, we need to chain commands using semicolons (;)
### Solution
```
/challenge/pwn; /challenge/college
```
After  running this,we get the flag
##
## Your First Shell Script
### Description
In this challenge, we need to write a shell script and make it executable.
### Thought Process
We need to use .sh suffix to create shell script.
### Solution
```
nano x.sh
chmod u+x x.sh
bash x.sh
```
##
## Redirecting Script Output
### Description
In this challenge, we learned how to redirect script output and use piping.
### Thought Process
We redirected the output of a script to another command.
### Solution
```
bash x.sh | /challenge/solve
```
After running this, I got the flag.
##
## Executable Shell Scripts
### Description
In this challenge, we learned how to create and execute an executable shell script.
### Thought Process
We created a script, modified its permissions, and executed it.
### Solution
```
nano script.sh
ls -l script.sh
chmod o+x script.sh
./script.sh
```
After executing these command, we get the flag
