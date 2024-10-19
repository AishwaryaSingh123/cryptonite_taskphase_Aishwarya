# Variable Printing
## Printing Variable
### Description: 
We need to get the flag by printing contents of variable flag
### Thought Process:
We will use echo $Variable_Name to print the contents of the variable as $ is used for variable expansion
### Solution:
```
echo $FLAG
```
After entering this we get the flag 
##
## Setting Variables
### Description:
Initialize a variable PWN with COLLEGE to get the flag.
### Thought Process:
To initialize, we will use = operator with no space on either side and remebering that letters cases are correct.
### Solution:
```
PWN=COLLEGE
```
After entering this, we got the flag
##
## Multi-word variables 
### Description:
Initialize PWN variable with COLLEGE YEAH.
### Thought process:
We need to use "" as otherwise = operator do not read anything after space.
### Solution:
```
PWN="COLLEGE YEAH"
```
After entering this, we get the flag
## 
## Exporting Variables
### Description:
To invoke /challenge/run after initializing PWN variable with value COLLEGE and exporting it and COLLEGE variable with PWN value and not exporting it
### New Things
$ sh where $ is the prompt of sh, a minimal shell implementation that invoked a child subshell
### Thought process:
We need tto add export while initializing PWN and not while initializing COLLEGE variable
### Solution:
```
export PWN=COLLEGE
COLLEGE=PWN
/challenge/run
```
After running these command, I got the flag
##
## Printing exported variable 
### Description:
To print the exported variable FLAG
### Thought process:
We need too use env instead of echo to print the flag
### Solution:
```
env $FLAG
```
After running this, we got the flag
## 
## Storing Command Output
### Description:
Store output of /challenge/run in PWN and display it
### New Things:
' ' are an old way of soring output in it but this has the disadvantage of not being able to nest
### Thought process:
$() will be used to store the output in the variable 
### Solution:
```
PWN=$(/challenge/run)
echo $PWN
```
After running this, the flag was displayed.
##
## Reading Input
### Description:
Read input COLLEGE in the variable PWN
### Thought process:
We need to use read bulletin with -p argument to accept prompt from user
### Solution:
```
read -p "INPUT: " PWN
```
then the output was INPUT: and then I entered COLLEGE in the input and I got the flag
##
## Reading FIles
### Description:
To read /challenge/read_me into the PWN environment variable
### Thought process
Using < and read to input the file in PWN variable
### Solution
```
read PWN < /challenge/read_me
```
After running this, we got the flag
