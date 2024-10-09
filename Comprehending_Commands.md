Cat: not the pet, but the command!
The cat command is used the contents of a file
command- cat flag


Catting Absolute Paths
We use the absolute flag of /flag since it is not present in the home directory
command- cat /flag

More catting practice
In this challenge we cant use the 'cd' command and can only use the 'cat' command with the absolute path of the 'flag' file, however we dont know the absolute path of the 'flag' file
we must pass the argument to cat with an absolute path of the file to get the flag
command- cat /usr/share/apache2/flag 

Grepping for a needle in a haystack
Since "data.txt" has too much data to go through if we use cat command we can use grep command and get the required conntent only by specifying some characters from it.
command - grep pwn.college /challenge/data.txt

Listing Files
The 'ls' command lists out the contents of a directory
command- ls /challenge
         /challenge/24592-renamed-run-28533

Removing Files
The rm command deltes a particular file.
In this challenge we had to create a file named "delete_me" only to later use rm command and delete it.
command- touch delete_me
          rm delete_me
          /challenge/check

Hidden files
The ls command with the '-a' argument shows us all the files (including the hidden files in a directory)
command-  ls -a / (the file .flag-228627021295 showed up)
          cat /.flag-228627021295


Epic file system Quest
In this challenge we had to use various commands cd,ls,cat and many arguments as well.
we had to keep following instructions given to get the flag.


Making Directories
The 'mkdir' command is used to create directories
command- mkdir /tmp/pwn
         touch /tmp/pwn/college
         /challenge/run

Finding files
The 'find' command finds any file in any search location we want.
The '-name' argument is used to specify that we are searching for a file by its name
We get many files as output some whose permission is denied.
If we cat the contents of all the permissible ones one by one we get the flag in one of them.
command- find / -name flag
         cat usr/lib/jvm/java-11-openjdk-amd64/legal/jdk.zipfs/flag
        
