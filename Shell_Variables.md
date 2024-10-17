1.Printing Variables<br/>
flag: pwn.college{YrvCVzZMwo98qpj4uwopZo4FNIl.ddTN1QDL5cjN0czW}<br/>
If we append the variable/argument with $ the echo comment will give us the flag.<br/>

2.Setting Variables<br/>
flag: pwn.college{US-EacwbqO-QirmdvtPoCG6GD5b.dlTN1QDL5cjN0czW}<br/>
Here we assign the values COLLEGE to the variable PWN.<br/>

3.Multi-Word Variables<br/>
flag:pwn.college{UuFMVJGYmzEgB61f388b3ksgn0-.dBjN1QDL5cjN0czW}<br/>
Here to assign multiple words to a single variable without having the problem with space we enclose the whole values in double quotes.<br/>

4. Exporting Variables<br/>
flag:pwn.college{4vQMZcre_ks7t8Lu-of8z4_GYag.dJjN1QDL5cjN0czW}<br/>
In this challenge we need to invoke /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported.<br/>
The export command is used for security reasons.<br/>
~$ export PWN<br/>
~$ PWN=COLLEGE<br/>
~$ COLLEGE=PWN<br/>
~$ /challenge/run<br/>

5.Printing Exported Variables<br/>
flag: pwn.college{M8bC4_fCtOxSfz44vPeEivIcHpz.dhTN1QDL5cjN0czW}<br/>
The env command is used to print all the exported values<br/>

6. Storing Command Output<br/>
   flag: pwn.college{wxxk0gyloNjOdukMJBCYuxXj1bs.dVzN0UDL5cjN0czW}<br/>
   Here we assign the ouput of a command to a variable using $()<br/>
   ~$ PWN=$(/challenge/run)<br/>
   ~$ cat $PWN<br/>


7.Reading Input<br/>
flag: pwn.college{wLPL9W-uP2PNPQCy2Sy6_uLxuad.dhzN1QDL5cjN0czW}<br/>
The read command is used tot ake the imput from the user and the -p is used to prompt.<br/>

8.Reading Files<br/>
flag: pwn.college{YVD4Ok4rqU7reP_RdKlAPwH6get.dBjM4QDL5cjN0czW}<br/>
We can enter the contents of a file into a varible using < command.<br/>

