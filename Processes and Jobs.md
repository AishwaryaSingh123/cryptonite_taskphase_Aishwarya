# Processes and Jobs
## Listing process
### Description
Run the /challenge/run with different file name 
### Thought process:
We need to use ps to get the list of running process to get the renamed file and run it 
### Solution:
```
ps -ef
/challenge/18603-run-23306
```
After running ps command we get a file named /challenge/18603-run-23306, so we run it to get the flag 
## 
## Killing Process
### Description 
To terminate a specific process named dont_run.
### Thought process
I used ps with grep to find the PID of the dont_run process and then killed it using the kill command.
### Solution 
```
ps -ef | grep dont_run
kill 73
/challenge/run
```
After finding the PID (73) and executing the kill command, I was able to run the subsequent challenge and retrieve the flag.
##
## Interrupting Processes
### Description
We learned to interrupt a running process using Ctrl-C.
### Thought Process
I needed to run a process that would not exit on its own, allowing me to use Ctrl-C to terminate it.
### Solution
```
/challenge/run
^C
```
By stopping the command, we get the flag
##
## Suspending Processes
### Description 
The challenge involved suspending a process with Ctrl-Z and launching it again.
### Thought Process
I had to suspend the current process to allow for another instance of it to run.
### Solution:
```
/challenge/run
^Z
/challenge/run
```
Relaunching the process after suspending it, I get the flag
##
## Resuming Processes
### Description
This challenge required resuming a suspended process in the foreground.
### Thought Process
After suspending the process, I would use the fg command to bring it back to the foreground.
### Solution:
```
/challenge/run
^Z
fg /challenge/run
```
##
## Backgrounding Processes
### Description
We learned to run a suspended process in the background.
### Thought Process
I needed to suspend the process and then background it to launch another instance.
### Solution:
```
/challenge/run
^Z
bg /challenge/run
/challenge/run
```
After suspending the process and running it in the background, I got the flag.
##
## Foregrounding Processes
### Description
The challenge involved bringing a background process back to the foreground.
### Thought Process
After backgrounding the process, I needed to resume it without re-suspending it.
### Solution:
```
/challenge/run
^Z
bg /challenge/run
fg /challenge/run
```
I brought the backgrounded process to the foreground, completing the challenge and receiving the flag.
##
## Starting Backgrounded Processes
### Description
This challenge focused on starting a process directly in the background.
### Thought Process
I needed to run the command with an & to start it in the background immediately.
### Solution:
```
/challenge/run &
```
##
## Process Exit Codes
### Description
The objective was to capture and submit a process exit code.
### Thought Process
I ran a command, noted its exit code, and then submitted it to verify correctness.
### Solution:
```
/challenge/get-code
echo $?
/challenge/submit-code 152
```
