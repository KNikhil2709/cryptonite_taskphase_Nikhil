1.Cat: not the pet, but the command!<br/>
The cat command is used the contents of a file<br/>
command- cat flag<br/>


2.Catting Absolute Paths<br/>
We use the absolute flag of /flag since it is not present in the home directory<br/>
command- cat /flag<br/>

3.More catting practice<br/>
In this challenge we cant use the 'cd' command and can only use the 'cat' command with the absolute path of the 'flag' file, however we dont know the absolute path of the 'flag' file<br/>
we must pass the argument to cat with an absolute path of the file to get the flag<br/>
command- cat /usr/share/apache2/flag <br/>

4.Grepping for a needle in a haystack<br/>
Since "data.txt" has too much data to go through if we use cat command we can use grep command and get the required conntent only by specifying some characters from it.<br/>
command - grep pwn.college /challenge/data.txt<br/>

5.Listing Files
The 'ls' command lists out the contents of a directory<br/>
command- ls /challenge<br/>
         /challenge/24592-renamed-run-28533<br/>

6.Removing Files<br/>
The rm command deltes a particular file.<br/>
In this challenge we had to create a file named "delete_me" only to later use rm command and delete it.<br/>
command- touch delete_me<br/>
          rm delete_me<br/>
          /challenge/check<br/>

7.Hidden files<br/>
The ls command with the '-a' argument shows us all the files (including the hidden files in a directory)<br/>
command-  ls -a / (the file .flag-228627021295 showed up)<br/>
          cat /.flag-228627021295<br/>


8.Epic file system Quest<br/>
In this challenge we had to use various commands cd,ls,cat and many arguments as well.<br/>
we had to keep following instructions given to get the flag.<br/>


9.Making Directories<br/>
The 'mkdir' command is used to create directories<br/>
command- mkdir /tmp/pwn<br/>
         touch /tmp/pwn/college<br/>
         /challenge/run<br/>

10.Finding files<br/>
The 'find' command finds any file in any search location we want.<br/>
The '-name' argument is used to specify that we are searching for a file by its name<br/>
We get many files as output some whose permission is denied.<br/>
If we cat the contents of all the permissible ones one by one we get the flag in one of them.<br/>
command- find / -name flag<br/>
         cat usr/lib/jvm/java-11-openjdk-amd64/legal/jdk.zipfs/flag<br/>
        
