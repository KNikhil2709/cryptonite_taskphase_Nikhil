1.Learning from Documentatin<br/>
The argument of '--giveflag' should be passed with '/challenge/challenge' command to get the flag<br/>
command -/challenge/challenge --giveflag<br/>


2.Learning Complex Usage<br/>
The argument '--printfile' will be given another argument which is the path of the file it will print.<br/>
Command- /challenge/challenge --printfile /flag<br/>


3.Reading Manuals<br/>
The man command will show the manual of the command we passed as an argument.<br/>
Command- man challenge<br/>
This will show the manual of the challenge command<br/>
The manual tells about the '--oaJsohMJ NUM' function which will give us the flag if NUM=703<br/>
Command- /challenge/challenge --oaJsohMJ 703<br/>

4.Searching Manuals<br/>
Here, we search the entire manual of the arguments. we can search the manual by using '/'<br/>
We can the command '/flag' to try to find the argument<br/>
while going through the corresponding text<br/>
 it shows:<br/>
  --oundujMT<br/>
            This argument will give the flag<br/>

command- /challenge/challenge --oundujMT<br/>



5.Searching for Manuals<br/>
First we us "man man" command<br/>
This opens up the manual for the man page database<br/>
![image](https://github.com/user-attachments/assets/4bed8605-8a98-4722-baf6-4449765ad826)<br/>
The 'man -k [apropos options]' command is the same as the 'apropos' command, hence it looked the most promising<br/>
The apropos command is used to help users find any command using its man pages<br/>

I asked my friend's help and he suggested me this website<br/>
https://www.geeksforgeeks.org/apropos-command-in-linux-with-examples/<br/>

Command- man -k challenge<br/>
          man zsetwfbfws<br/>
          challenge/challenge --zsetwf 213<br/>



6.Helpful Programs<br/>
The "--help" command gives us the program/s documentation.<br/>
This documents let's us know some arguement snecessary for the challenge<br/>
![image](https://github.com/user-attachments/assets/d257fd53-2715-4c8f-b33a-dc1b852470a2)<br/>
Command-    /challenge/challenge -p<br/>
            /challenge/challenge -g 742<br/>


7.Help for Builtins<br/>
Since 'challenge' is a builtin, not a command in this challenge, we can use the 'help' builtin to get some info.<br/>
Command- help challenge<br/>
This gives us info of the function- '--secret VALUE' which will print the flag, if VALUE is correct. It also gives us the right value (oaJsohMJ)<br/>
Command- challenge --secret oaJsohMJ<br/>


