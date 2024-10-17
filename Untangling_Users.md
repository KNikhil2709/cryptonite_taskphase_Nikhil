
1.Becoming root with Su
flag: pwn.college{wfh055emEGaoKmI6X6J4_9-8zzv.dVTN0UDL5cjN0czW}
~$ su 
Password: hack-the planet
~$ cat /flag


2.Other users with su
flag:pwn.college{MpoHEvG5vISqM0qGaanHNuBhmHW.dZTN0UDL5cjN0czW}
~$ su zardus
Password: dont-hack-me
~$ /challenge/run


3. Cracking Passwords
   flag: pwn.college{YJEC9TN35-LgBPAjGGGgwj4V-vG.ddTN0UDL5cjN0czW}
   Here first we run /challenge/shadow-leak throught the john command which is the leaker file of /challenge/shadow which upon running gives the password "aardvark".
   upon using this as a root password we can become zardus and then /challenge/run to get the flag.
   ~$ john /challenge/shadow-leak
   ~$ su zardus
    Password: aardvark

4. Using Sudo
   flag: pwn.college{Q32ALIemQFepAwa-0Qb6ldw7UVy.dhTN0UDL5cjN0czW}
   ~$ sudo cat /flag
   
