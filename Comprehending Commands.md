Challenge 1
Collect the flag by reading the flag file in the home directory using cat.
Thought Process
I used cat to read the contents of the flag file located in the home directory.
Solution:
cat ~/flag
After running this command I got the flag.

Challenge 2:
Retrieve the flag from the /flag file using its absolute path.
Thought Process
The flag was located at /flag, so I used its absolute path with the cat command.
Solution:
cat /flag
After running this command I got the flag

Challenge 3:
Read the flag from an absolute path without changing directories.
Thought Process
I accessed the flag using its absolute path and cat command since I couldn't use cd.
Solution:
cat /opt/binaryninja/flag
After running this command I got the flag

Challenge 4:
Search for the flag in a large file using grep.
Thought Process
I used grep to search for "pwn.college" in the large file to find the flag as flag starts with pwn.college.
Solution:
grep pwn.college /challenge/data.txt
After running this command I got the flag

Challenge 5:
List the contents of a directory using ls.
Thought Process
I used ls to view the files in the /challenge directory.
Solution
ls /challenge
After running this command I found the flag

Challenge 6:
Create two files in /tmp and run /challenge/run to get the flag.
Thought Process
I used touch to create the required files, then executed the program.
Solution
touch /tmp/pwn  
touch /tmp/college  
/challenge/run


Challenge 7:
Delete the delete_me file and run /challenge/check.
Thought Process
I used rm to delete the file and verified the action by running the program.
Solution:
rm ~/delete_me  
/challenge/check

Challenge 8:
Follow clues hidden in various files to find the flag.
Thought Process
I tried to get clues using ls there I found a file hint. I accessed it using cat command to get the flag.
Solution:
cd /  
ls  
cat HINT

Challenge 9:
Create a /tmp/pwn directory, add a file, and run /challenge/run.
Thought Process
I used mkdir and touch to create the directory and file respectively, then executed the program.
Solution:
mkdir /tmp/pwn  
cd /tmp/pwn  
touch college  
/challenge/run

Challenge 10:
To collect the flag by creating a symbolic link to the file located at /flag and using the /challenge/catflag command to read it through the symlink.
Thought Process
I used symbolic links to access different files from different locations.
The ln -s command is used to create a symlink, which can then be accessed like the original file. 
The goal was to create a symlink that points to the /flag file and use the /challenge/catflag to retrieve the flag.
Solution:
ln -s /flag /home/hacker/not-the-flag
bash
/challenge/catflag




