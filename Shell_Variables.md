1.Printing Variables
flag: pwn.college{YrvCVzZMwo98qpj4uwopZo4FNIl.ddTN1QDL5cjN0czW}
If we append the variable/argument with $ the echo comment will give us the flag.

2.Setting Variables
flag: pwn.college{US-EacwbqO-QirmdvtPoCG6GD5b.dlTN1QDL5cjN0czW}
Here we assign the values COLLEGE to the variable PWN.

3.Multi-Word Variables
flag:pwn.college{UuFMVJGYmzEgB61f388b3ksgn0-.dBjN1QDL5cjN0czW}
Here to assign multiple words to a single variable without having the problem with space we enclose the whole values in double quotes.

4. Exporting Variables
flag:pwn.college{4vQMZcre_ks7t8Lu-of8z4_GYag.dJjN1QDL5cjN0czW}
In this challenge we need to invoke /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported.
The export command is used for security reasons.
~$ export PWN
~$ PWN=COLLEGE
~$ COLLEGE=PWN
~$ /challenge/run

5.Printing Exported Variables
flag: pwn.college{M8bC4_fCtOxSfz44vPeEivIcHpz.dhTN1QDL5cjN0czW}
The env command is used to print all the exported values

6. Storing Command Output
   flag: pwn.college{wxxk0gyloNjOdukMJBCYuxXj1bs.dVzN0UDL5cjN0czW}
   Here we assign the ouput of a command to a variable using $()
   ~$ PWN=$(/challenge/run)
   ~$ cat $PWN


7.Reading Input
flag: pwn.college{wLPL9W-uP2PNPQCy2Sy6_uLxuad.dhzN1QDL5cjN0czW}
The read command is used tot ake the imput from the user and the -p is used to prompt.

8.Reading Files
flag: pwn.college{YVD4Ok4rqU7reP_RdKlAPwH6get.dBjM4QDL5cjN0czW}
We can enter the contents of a file into a varible using < command.

