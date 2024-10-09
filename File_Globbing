#File Gobbling

## Matching with *
change your directory to /challenge, but use globbing to keep the argument you pass to cd to at most four characters!
Once you're there, run /challenge/run for the flag!
### Thought process
Using *, the shell treats it as a wildcard, replacing it with matching filenames.
If no files match, the glob remains unchanged:
The * matches any part of the filename except for / or a leading .
To navigate to /challenge using globbing with at most four characters:
#Solutions
'''
cd /ch*
/challenge/run
'''

##Matching with ?
Change your directory to /challenge, but use the ? character instead of c and l in the argument to cd! Once you're there, run /challenge/run for the flag!
###Thought Process
We have to navigate to /challenge using ? instead of c and l.
###Solutions
'''
cd /?ha??enge
/challenge$ /challenge/run
'''

##Matching with []
 Change your working directory to /challenge/files and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h
##Thought process
The [] wildcard matches specified characters. Therefore putting absh in in in address will help me look in all using 1 command.
###Solution
'''
cd /challenge/files
/challenge/files$ /challenge/run file_[bash]
'''

##Matching paths with []
Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!
###Thought process
Just like we used above we can use [] in files path too.
###Solutions
'''
cd /ch*
/challenge/run
'''

##Mixing globs
To but diversely-named files in /challenge/files.
Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob that will match the files "challenging", "educational", and "pwning"!
###Thought process
The first letters of the file names that we have to match with are non repeating so we can just enter the starting letters in [] and then * ahead it.
###Solution
'''
cd /challenge/files
/challenge/run [cep]*
'''

##Exclusionary globbing
To run all the files that didin't start with p w n
###Thought process 
Using ! excludes specified characters from matching. Thus, [!pwn]* excludes files starting with p, w, or n.
###Solutions:
'''
cd /challenge/files
/challenge/run [!pwn]*
'''
