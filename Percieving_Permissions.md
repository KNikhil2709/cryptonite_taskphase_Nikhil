1. Changing Files ownership<br/>
   flag: pwn.college{0Y2umgLqDzYooyjNQxQcPuoUwf_.dFTM2QDL5cjN0czW}<br/>
   Here we change the ownership of the /flag file from the root to hacker using the chown command.<br/>
   After the ownership is passed we simple had to cat the flag file to get the flag.<br/>

2. Groups and Files.<br/>
   flag: pwn.college{UO-xmXJuVWLqlWvo_mWla3gOV8_.dFzNyUDL5cjN0czW}<br/>
   in this challenge we can change the group of the 'flag' file to 'hacker' in order get permission to read it out.<br/>
  ~$ chgrp hacker /flag<br/>
  ~$ cat /flag<br/>

3.Fun with Group Names<br/>
  flag: pwn.college{YzgNgCPNfhecuk7tokbeJyS4hH4.dJzNyUDL5cjN0czW}<br/>
  We need to change the group of the flag file to the group of the user. We can find the group of the user using the 'id' command.<br/>
Using the id command gives us the output-<br/>
uid=1000(hacker) gid=1000(grp1911) groups=1000(grp1911)<br/>
~$ chgrp grp1911 /flag<br/>
~$ cat /flag<br/>

4.Changing Permissions<br/>
flag: pwn.college{MBbC9tyeNBbpIoTLHmF8t7ceF_t.dNzNyUDL5cjN0czW}<br/>
We can use the 'chmod' command to change the permissions of the files we want.<br/>
For the purposes of this challenge we need to change the permissions of the flag file to be read by the public (Since hacker isnt a user nor a part of the group).<br/>

5.Executable Files<br/>
flag: pwn.college{A5DQQvG9K5YVrjr9Ux0ILsrdhHR.dJTM2QDL5cjN0czW}<br/>
Just like the previous but here we have to make it executable.<br/>

6. Permission Tweaking Practice<br/>
   flag: pwn.college{0RIxjXsb8dYztnHYruRpo-Dnol8.dBTM2QDL5cjN0czW}<br/>
   In this program we will be given a set of 8 changes to be made to the /challenge/pwn file in order to unlock chmod permission for the '/flag' file.<br/>
    The 8 changes to be made in order are-<br/>
    ~$ chmod 200 /challenge/pwn<br/>
    ~$ chmod 000 /challenge/pwn<br/>
    ~$ chmod 300 /challenge/pwn<br/>
    ~$ chmod 200 /challenge/pwn<br/>
    ~$ chmod 707 /challenge/pwn<br/>
    ~$ chmod 404 /challenge/pwn<br/>
    ~$ chmod 606 /challenge/pwn<br/>
    ~$ chmod 736 /challenge/pwn<br/>

   We are now enabled to chmod the /flag file to get the flag<br/>
   ~$ chmod a+r /flag<br/>
   ~$ cat /flag<br/>

7. Permission Setting Practice<br/>
   flag:pwn.college{I5m82S8KOhWCNIvtybANBdfJHT9.dNTM5QDL5cjN0czW}<br/>
   This challenge is the same as the previous one but we need to use =.<br/>
   = helps us set permissions altogether instead of updating the old ones.<br/>

8. The SUID Bit<br/>
   flag: pwn.college{ctGEmS6xhbNu4iuUsMnCv55F8Fe.dNTM2QDL5cjN0czW}<br/>
   First we give the user the suid or the permission to execute the file as the owner<br/>
   Then we execute for the shell to open.<br/>
   There if we list out the files we can see not-the-flag in blue.<br/>
   Upon using cat function for it we get the flag.<br/>
    ~$ chmod u+s /challenge/getroot<br/>
    ~$ /challenge/getroot<br/>
    ~$ ls<br/>
    ~$ cat /not-the-flag<br/>
