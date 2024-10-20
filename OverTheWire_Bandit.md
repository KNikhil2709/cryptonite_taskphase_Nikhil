1. L0-L1
    ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If<br/>
   Command:- cat readme<br/>

2. L1-L2<br/>
   263JGJPfgU6LtdEvgfWU1XP5yac29mFx<br/>
   Command:- cat ./-<br/>
   Similar to previous Question.<br/>

3. L2-L3<br/>
   MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx<br/>
   Command:- ~$ cat ./"spaces in this filename"<br/>

4.L3-L4<br/>
 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ<br/>
 Command:-~$ cd /inhere<br/>
  ~/inhere~$ ls -al<br/>
  ~/inhere~$ cat ...Hiding-From-You<br/>
First we go to the direcotry and list all hidden files and get the password by catting the appropriate file.<br/>

5.L4-L5<br/>
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw<br/>
In this level we learn about the command "file /*" which gives us the desc about the contents of the files.<br/>
using this we find that file07 is in human readable form.<br/>
Command:- ~$ file inhere/*<br/>
          ~$ cat inhere/-file07<br/>

6.L5-L6<br/>
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG<br/>
Here we use "-size (size)" command to find the file of specific size.<br/>
Command:- ~$ cd inhere<br/>
          ~$ find -size 1033c<br/>
          ~$ cat ./maybehere07/.file2<br/>


7. L6-L7<br/>
   morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj<br/>
   Command:- ~$ find / -user bandit7 -group bandit6 -size 33c<br/>
             ~$ cat /var/lib/dpkg/info/bandit7.password<br/>
Similar to Previous Question, but here we get a lot of files which fit the descriptions provided with permission denied and we need to find the one with permission is not denied.<br/>

8. L7-L8<br/>
   dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc<br/>
   Command:- ~$ grep "millionth *" data.txt<br/>
   This level was simple. we just use prep "millionth" and a * to find the passsword.<br/>
   
9.L8-L9<br/>
  4CKMh1JI91bUIZZPXDqGanal4xvAg0JM<br/>
  Command:-sort data.txt | uniq -u<br/>
  The sort command is used to put duplicate text adjacent to each other and the uniq -u command will filter out the lines which occur more than once.<br/>

10. L9-L10<br/>
    FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey<br/>
    Command:- strings data.txt | grep '===='<br/>

    Coomand:-strings data.txt | grep '===='

   
