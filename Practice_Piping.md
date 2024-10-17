1.Redirecting Output<br/>
The '>' character redirects the output of any command to any file we desire.<br/>
Command- echo PWN > COLLEGE<br/>
Here we're redirecting the output of 'echo' which is "PWN" to the file 'COLLEGE'. If the file COLLEGE didnt already exist then '>' will create the file<br/>


2.Redirecting More Ouput<br/>
Since we '>' character will redirect the output of any command to any file we can use it to redirect the flag value to a file and then read it from there<br/>
Command- /challenge/run > myflag<br/>
This gives an error saying we need to redirect it to the file- '/home/hacker/myflag'<br/>
Command- /challenge/run > ~/myflag<br/>
         cat ~/myflag<br/>


3.Appending Output<br/>
The '>>' character works the same way as the '>' character but it appends the data instead of creating a new output file<br/>
In this challenge the flag has been split into 2 parts and must be added to the 'the-flag' file<br/>
In order to get both the parts without losing the first one, we need to use '>' first followed by '>>'<br/>
Command- /challenge/run > ~/the-flag<br/>
         /challenge/run >> ~/the-flag<br/>


4.Redirecting Errors<br/>
FD describes the communication channel-<br/>
0=stdin 1=stdout 2=stderr<br/>
we can use multiple in the same command<br/>
we need to redirect the output to 'myflag' and rhe errors to 'instructions'<br/>
Command- /challenge/run >myflag 2>instructions<br/>
         cat myflag<br/>


5.Redirecting Input<br/>
We need to redirect the PWN file to '/challenge/run' and PWN must contain the value 'COLLEGE'<br/>
first we need to change the value in PWN to COLLEGE and then redirect it into the program<br/>
Commnad- echo COLLEGE > PWN<br/>
        /challenge/run < PWN<br/>


6.Grepping Stored Results<br/>
In this challenge we need to redirect the output of /challenge/run to /tmp/data.txt and then use 'grep' to find the flag in it<br/>
-grep is a command used for searching and matching text patterns in files contained in the regular expressions.<br/>
Command- /challenge/run > /tmp/data.txt<br/>
         grep -i "pwn.college" /tmp/data.txt<br/>

  I used this link for reference:https://www.geeksforgeeks.org/grep-command-in-unixlinux/<br/>

This grep command searches for the string "pwn.college" in the file and will output the line it is in.<br/>
the '-i' argument enables to search for a string case insensitively in the given file.<br/>
The above commands will give us the flag as the output.<br/>


7.Grepping Live Output<br/>
The | operator connects the stout of the command on the left to the stdin of the command on the right.<br/>
We need to run '/challenge/run' and grep its output real time to give us the flag<br/>
Command- /challenge/run | grep -i "pwn.college"<br/>
this will put the flag value in 'myflag' which can then be accessed<br/>


8.Grepping errors<br/>
Since the | operator only redirects the stdout and not the stderr, we need to use the >& operator, which redirects a file descriptor to another file descriptor.<br/>
Hence, we can have a two-step process to grep through errors.<br/>
First we redirect standard error to standard output and then pipe it to grep too search for the flag<br/>

Command - /challenge/run 2>&1 | grep -i "pwn.college"<br/>


9.Duplicating piped data with tee<br/>
In this challenge we need to use tee to intercept the data and find out how to run the command to get the flag.<br/>
To do this we will use tee to store the error given by the command into a file and then hopefully the error stored will give us a clue.<br/>
/challenge/pwn | tee pwn_output | /challenge/college<br/>

Command- Usage: /challenge/pwn --secret [SECRET_ARG]<br/>

SECRET_ARG should be "AybjGsm8"<br/>

The error now tells us what we need to do to get the flag, hence-<br/>
Command-   /challenge/pwn --secret AybjGsm8 | /challenge/college<br/>


10.Writing to Multiple Programs<br/>
'>(command)' is process substitution, which creates named pipes that send the output directly to the command's input Since we need to direct the output of '/challenge/hack' into both '/challenge/the' and '/challenge/planet' at the same time, we need to use process substitution<br/>
Command-   /challenge/hack | tee >( /challenge/the ) >( /challenge/planet)<br/>
