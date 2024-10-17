1. The PATH Variable<br/>
flag: pwn.college{U2RyJ7OdzEqwhOrqnLS3dY_0cF5.dZzNwUDL5cjN0czW}<br/>
~$  PATH=""<br/>
~$ /challenge/run<br/>

2. Setting Path<br/>
flag: pwn.college{QX93eYz2JB1zIfrqWCQh4m7De8m.dVzNyUDL5cjN0czW}<br/>
~$ ls /challenge/more_commands/<br/>
~$ PATH=/challenge/more_commands/<br/>
~$ /challenge/run<br/>

3.Adding Commands<br/>
flag:pwn.college{wJcwe1O_ag6EVISR08sbP4kL6ab.dZzNyUDL5cjN0czW}.<br/> 
~$ touch win<br/>
~$ nano win<br/>
~$ chmod u+x win<br/>
~$ PATH=/home/hacker<br/>
~$ /challenge/run<br/>

4.Hijacking Commands<br/>
flag: pwn.college{AZHhOB0rd99aHl7WL6ZMZLSstZs.ddzNyUDL5cjN0czW}<br/>
In this challenge, we need to trick /challenge/run into printing the flag by changing the rm comamnd.<br/>
we use nano command and open rm command and write<br/>
"read FLAG < /flag
echo $FLAG"
~$ nano rm
~$ chmod o+x rm
~$ PATH=~/
~$ /challenge/run
