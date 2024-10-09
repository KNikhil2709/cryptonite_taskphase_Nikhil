Redirecting Output
The '>' character redirects the output of any command to any file we desire.
Command- echo PWN > COLLEGE
Here we're redirecting the output of 'echo' which is "PWN" to the file 'COLLEGE'. If the file COLLEGE didnt already exist then '>' will create the file


Redirecting More Ouput
Since we '>' character will redirect the output of any command to any file we can use it to redirect the flag value to a file and then read it from there
Command- /challenge/run > myflag
This gives an error saying we need to redirect it to the file- '/home/hacker/myflag'
Command- /challenge/run > ~/myflag
         cat ~/myflag


Appending Output
The '>>' character works the same way as the '>' character but it appends the data instead of creating a new output file
In this challenge the flag has been split into 2 parts and must be added to the 'the-flag' file
In order to get both the parts without losing the first one, we need to use '>' first followed by '>>'
Command- /challenge/run > ~/the-flag
         /challenge/run >> ~/the-flag


Redirecting Errors
FD describes the communication channel-
0=stdin 1=stdout 2=stderr
we can use multiple in the same command
we need to redirect the output to 'myflag' and rhe errors to 'instructions'
Command- /challenge/run >myflag 2>instructions
         cat myflag


Redirecting Input
We need to redirect the PWN file to '/challenge/run' and PWN must contain the value 'COLLEGE'
first we need to change the value in PWN to COLLEGE and then redirect it into the program
Commnad- echo COLLEGE > PWN
        /challenge/run < PWN




Grepping Stored Results
In this challenge we need to redirect the output of /challenge/run to /tmp/data.txt and then use 'grep' to find the flag in it
-grep is a command used for searching and matching text patterns in files contained in the regular expressions.
Command- /challenge/run > /tmp/data.txt
         grep -i "pwn.college" /tmp/data.txt

  I used this link for reference:https://www.geeksforgeeks.org/grep-command-in-unixlinux/

This grep command searches for the string "pwn.college" in the file and will output the line it is in.
the '-i' argument enables to search for a string case insensitively in the given file.
The above commands will give us the flag as the output.




Grepping Live Output
The | operator connects the stout of the command on the left to the stdin of the command on the right.
We need to run '/challenge/run' and grep its output real time to give us the flag
Command- /challenge/run | grep -i "pwn.college"
this will put the flag value in 'myflag' which can then be accessed



Grepping errors
Since the | operator only redirects the stdout and not the stderr, we need to use the >& operator, which redirects a file descriptor to another file descriptor.
Hence, we can have a two-step process to grep through errors.
First we redirect standard error to standard output and then pipe it to grep too search for the flag

Command - /challenge/run 2>&1 | grep -i "pwn.college"




Duplicating piped data with tee
In this challenge we need to use tee to intercept the data and find out how to run the command to get the flag.
To do this we will use tee to store the error given by the command into a file and then hopefully the error stored will give us a clue.
/challenge/pwn | tee pwn_output | /challenge/college

Command- Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "AybjGsm8"

The error now tells us what we need to do to get the flag, hence-
Command-   /challenge/pwn --secret AybjGsm8 | /challenge/college





Writing to Multiple Programs
'>(command)' is process substitution, which creates named pipes that send the output directly to the command's input Since we need to direct the output of '/challenge/hack' into both '/challenge/the' and '/challenge/planet' at the same time, we need to use process substitution
Command-   /challenge/hack | tee >( /challenge/the ) >( /challenge/planet)






