# Pondering paths

## The Root
To get the flag in pwn program by using / operator
### Thought process
/ can be used to access the file using the absolute path.
### Solution
'''
/pwn
'''
Running this we got the flag

## Program and absolute paths
To get the flag in challenge directory in run program
### Thought process
Using the absolute path and / operator we can execute files.
### Solutions
'''
/challenge/run
'''
Executing this we get the flag.

## Position thy self
Use cd to get to the correct directory to run the run command in challenge file
### Thought process
First running the /challenge/run command to get to know the correcct directory.
Then going to that directory using cd and again running the run file to get the flag
### Solution
'''
/challenge/run
cd /user/share/doc/fontconfig
/challenge/run
'''
running this we get the flag.

## Position elsewhere
To run the run file in challenge directory in some other directory using cd
### Thought process:
Typing /challenge/run in the terminal we were told that we are not in the current directory and we  got the address of the directory.
Using cd we get to the directory and run the run file in challege directory
### Solution
'''/challenge/run
cd /usr/share/build-essential
/challenge/run
'''

## Position yet elsewhere
To collect the flag by executing the /challenge/run program from a specific path. 
### Thought process
I needed to navigate to the /etc directory. After running /challenge/run, 
I received the message: "You are not currently in the /etc directory." 
### Solution
'''
cd /etc
/challenge/run
'''
## Implicit Relative Paths, from /
To run /challenge/run using a relative path while in the root directory
### Thought process
 I recognized that relative paths do not start with /.
Given the hint that the path starts with "c," I deduced the relative path to be challenge/run.
### Solution
'''
cd /
challenge/run
'''

## Explicit Relative Paths, from /
Using explicit relative path to get to file in which /challenge/run command .
### Thought process
Again, to run challenge/run using . as part of the relative path from the root directory, I understood that . refers to the current directory.
I navigated to the root directory.
### Solution
'''
cd /
./challenge/run
'''

## Implicit Relative Path
To collect the flag by executing run program using a relative path while having a current working directory of /challenge
### Thought Process
First we have to navigate there using relative path and run the run file.
### Solution
'''
cd /challenge
./run
'''

## Home Sweet Home
To collect the flag by executing /challenge/run command by specifying a file path as an argument that must be an absolute path that is inside home directory.
Before expansion argument must be 3 character or less.
### Thought process
To execute /challenge/run with an absolute path as an argument, constrained to three characters or less within my home directory, I used ~, which stands for /home/hacker.
### Solution
'''
/challenge/run ~/f
'''
