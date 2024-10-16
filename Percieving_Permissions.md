1. Changing Files ownership
   flag: pwn.college{0Y2umgLqDzYooyjNQxQcPuoUwf_.dFTM2QDL5cjN0czW}
   Here we change the ownership of the /flag file from the root to hacker using the chown command.
   After the ownership is passed we simple had to cat the flag file to get the flag.

2. Groups and Files.
   flag: pwn.college{UO-xmXJuVWLqlWvo_mWla3gOV8_.dFzNyUDL5cjN0czW}
   in this challenge we can change the group of the 'flag' file to 'hacker' in order get permission to read it out.
  ~$ chgrp hacker /flag
  ~$ cat /flag

3.Fun with Group Names
  flag: pwn.college{YzgNgCPNfhecuk7tokbeJyS4hH4.dJzNyUDL5cjN0czW}
  We need to change the group of the flag file to the group of the user. We can find the group of the user using the 'id' command.
Using the id command gives us the output-
uid=1000(hacker) gid=1000(grp1911) groups=1000(grp1911)
~$ chgrp grp1911 /flag
~$ cat /flag

4.Changing Permissions
flag: pwn.college{MBbC9tyeNBbpIoTLHmF8t7ceF_t.dNzNyUDL5cjN0czW}
We can use the 'chmod' command to change the permissions of the files we want.
For the purposes of this challenge we need to change the permissions of the flag file to be read by the public (Since hacker isnt a user nor a part of the group).

5.Executable Files
flag: pwn.college{A5DQQvG9K5YVrjr9Ux0ILsrdhHR.dJTM2QDL5cjN0czW}
Just like the previous but here we have to make it executable.

6. Permission Tweaking Practice
   flag: pwn.college{0RIxjXsb8dYztnHYruRpo-Dnol8.dBTM2QDL5cjN0czW}
   In this program we will be given a set of 8 changes to be made to the /challenge/pwn file in order to unlock chmod permission for the '/flag' file.
    The 8 changes to be made in order are-
    ~$ chmod 200 /challenge/pwn
    ~$ chmod 000 /challenge/pwn
    ~$ chmod 300 /challenge/pwn
    ~$ chmod 200 /challenge/pwn
    ~$ chmod 707 /challenge/pwn
    ~$ chmod 404 /challenge/pwn
    ~$ chmod 606 /challenge/pwn
    ~$ chmod 736 /challenge/pwn

   We are now enabled to chmod the /flag file to get the flag
   ~$ chmod a+r /flag
   ~$ cat /flag

7. Permission Setting Practice
   flag:pwn.college{I5m82S8KOhWCNIvtybANBdfJHT9.dNTM5QDL5cjN0czW}
   This challenge is the same as the previous one but we need to use =.
   = helps us set permissions altogether instead of updating the old ones.

8. The SUID Bit
   flag: pwn.college{ctGEmS6xhbNu4iuUsMnCv55F8Fe.dNTM2QDL5cjN0czW}
   First we give the user the suid or the permission to execute the file as the owner
   Then we execute for the shell to open.
   There if we list out the files we can see not-the-flag in blue.
   Upon using cat function for it we get the flag.
    ~$ chmod u+s /challenge/getroot
    ~$ /challenge/getroot
    ~$ ls
    ~$ cat /not-the-flag
