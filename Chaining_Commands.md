1. Chaining with semicolons
flag: pwn.college{g_zetumH-akxAgZaZ2YZx4W-ShM.dVTN4QDL5cjN0czW}
~$  /challenge/pwn ; /challenge/college
We chain 2 commands using ;.

2.Your First Shell Script
flag: pwn.college{szi4XLpqKWWXIWZ-Q7wrY00A-5M.dFzN4QDL5cjN0czW}
First we creat a file x.sh using touch commans=d and then we use nano and open a text editor where we typing the commands /challenge/pwn and /challenge/college and save it and then exit it.
We get back to command line.
Here we use bsh x.sh to get the flag.

3.Redirecting Script Output
flag: pwn.college{Ymo1OUZfuxwS4rgX5ahAA4LNB_W.dhTM5QDL5cjN0czW}
~$ nano p.sh
~$ bash p.sh | /challenge/solve 

4.Executable Shell Scripts
flag: pwn.college{YnJcJ6ziVufSMPrEKUHPdGHFO5B.dRzNyUDL5cjN0czW}
~$ touch s2.sh
~$ nano s2.sh
~$ chmod +x s2.sh
~$ ./s2.sh
