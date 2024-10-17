1.Becoming root with Su<br/>
flag: pwn.college{wfh055emEGaoKmI6X6J4_9-8zzv.dVTN0UDL5cjN0czW}<br/>
~$ su <br/>
Password: hack-the planet<br/>
~$ cat /flag<br/>


2.Other users with su<br/>
flag:pwn.college{MpoHEvG5vISqM0qGaanHNuBhmHW.dZTN0UDL5cjN0czW}<br/>
~$ su zardus<br/>
Password: dont-hack-me<br/>
~$ /challenge/run<br/>


3. Cracking Passwords<br/>
   flag: pwn.college{YJEC9TN35-LgBPAjGGGgwj4V-vG.ddTN0UDL5cjN0czW}<br/>
   Here first we run /challenge/shadow-leak throught the john command which is the leaker file of /challenge/shadow which upon running gives the password "aardvark".<br/>
   upon using this as a root password we can become zardus and then /challenge/run to get the flag.<br/>
   ~$ john /challenge/shadow-leak<br/>
   ~$ su zardus<br/>
    Password: aardvark<br/>

4. Using Sudo<br/>
   flag: pwn.college{Q32ALIemQFepAwa-0Qb6ldw7UVy.dhTN0UDL5cjN0czW}<br/>
   ~$ sudo cat /flag<br/>
   
