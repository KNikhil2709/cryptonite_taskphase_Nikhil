1. Chaining with semicolons<br/>
flag: pwn.college{g_zetumH-akxAgZaZ2YZx4W-ShM.dVTN4QDL5cjN0czW}<br/>
~$  /challenge/pwn ; /challenge/college<br/>
We chain 2 commands using ;.<br/>

2.Your First Shell Script<br/>
flag: pwn.college{szi4XLpqKWWXIWZ-Q7wrY00A-5M.dFzN4QDL5cjN0czW}<br/>
First we creat a file x.sh using touch commans=d and then we use nano and open a text editor where we typing the commands /challenge/pwn and /challenge/college and save it and then exit it.<br/>
We get back to command line.<br/>
Here we use bsh x.sh to get the flag.<br/>

3.Redirecting Script Output<br/>
flag: pwn.college{Ymo1OUZfuxwS4rgX5ahAA4LNB_W.dhTM5QDL5cjN0czW}<br/>
~$ nano p.sh<br/>
~$ bash p.sh | /challenge/solve <br/>

4.Executable Shell Scripts<br/>
flag: pwn.college{YnJcJ6ziVufSMPrEKUHPdGHFO5B.dRzNyUDL5cjN0czW}<br/>
~$ touch s2.sh<br/>
~$ nano s2.sh<br/>
~$ chmod +x s2.sh<br/>
~$ ./s2.sh<br/>
