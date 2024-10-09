Learning from Documentatin
The argument of '--giveflag' should be passed with '/challenge/challenge' command to get the flag
command -/challenge/challenge --giveflag


Learning Complex Usage
The argument '--printfile' will be given another argument which is the path of the file it will print.
Command- /challenge/challenge --printfile /flag


Reading Manuals
The man command will show the manual of the command we passed as an argument.
Command- man challenge
This will show the manual of the challenge command
The manual tells about the '--oaJsohMJ NUM' function which will give us the flag if NUM=703
Command- /challenge/challenge --oaJsohMJ 703

Searching Manuals
Here, we search the entire manual of the arguments. we can search the manual by using '/'
We can the command '/flag' to try to find the argument
while going through the corresponding text
 it shows:
  --oundujMT
            This argument will give the flag

command- /challenge/challenge --oundujMT



Searching for Manuals
First we us "man man" command
This opens up the manual for the man page database
![image](https://github.com/user-attachments/assets/4bed8605-8a98-4722-baf6-4449765ad826)
The 'man -k [apropos options]' command is the same as the 'apropos' command, hence it looked the most promising
The apropos command is used to help users find any command using its man pages

I asked my friend's help and he suggested me this website
https://www.geeksforgeeks.org/apropos-command-in-linux-with-examples/

Command- man -k challenge
          man zsetwfbfws
          challenge/challenge --zsetwf 213



Helpful Programs
The "--help" command gives us the program/s documentation.
This documents let's us know some arguement snecessary for the challenge
![image](https://github.com/user-attachments/assets/d257fd53-2715-4c8f-b33a-dc1b852470a2)
Command-    /challenge/challenge -p
            /challenge/challenge -g 742


Help for Builtins
Since 'challenge' is a builtin, not a command in this challenge, we can use the 'help' builtin to get some info.
Command- help challenge
This gives us info of the function- '--secret VALUE' which will print the flag, if VALUE is correct. It also gives us the right value (oaJsohMJ)
Command- challenge --secret oaJsohMJ


