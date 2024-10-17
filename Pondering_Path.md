1. The PATH Variable
flag: pwn.college{U2RyJ7OdzEqwhOrqnLS3dY_0cF5.dZzNwUDL5cjN0czW}
~$  PATH=""
~$ /challenge/run

2. Setting Path
flag: pwn.college{QX93eYz2JB1zIfrqWCQh4m7De8m.dVzNyUDL5cjN0czW}
~$ ls /challenge/more_commands/
~$ PATH=/challenge/more_commands/
~$ /challenge/run

3.Adding Commands
flag:pwn.college{wJcwe1O_ag6EVISR08sbP4kL6ab.dZzNyUDL5cjN0czW}. 
~$ touch win
~$ nano win
~$ chmod u+x win
~$ PATH=/home/hacker
~$ /challenge/run

4.Hijacking Commands
flag: pwn.college{AZHhOB0rd99aHl7WL6ZMZLSstZs.ddzNyUDL5cjN0czW}
In this challenge, we need to trick /challenge/run into printing the flag by changing the rm comamnd.
we use nano command and open rm command and write
"read FLAG < /flag
echo $FLAG"
~$ nano rm
~$ chmod o+x rm
~$ PATH=~/
~$ /challenge/run
