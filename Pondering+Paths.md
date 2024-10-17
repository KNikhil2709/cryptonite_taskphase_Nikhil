1.THE ROOT<br/>
The flag is captured captured by invoking the "pwn" program using its absolute path.<br/>
command- /pwn<br/>


2.Program and Absolute Paths<br/>
Invoking "challenge" directory and "run" program in the terminal will give us the flag for this challenge.<br/>
command- /challenge/run<br/>


3.Position THY Self<br/>
By changing directory(cd /directoryname) to "etc" directory and then invoking the "challenge" directory with "run" program will give us the flag.<br/>
command- cd /etc<br/>
        /challenge/run<br/>


4.Positon Elsewhere<br/>
By first invoking "/challenge/run" provides with the location of the directory i.e., /proc/301. By changing directory to /proc/301 and then invoking /challenge/run.<br/>
command- cd /proc/301.<br/>
        /challenge/run<br/>
        

5.Position Yte Elsewhere<br/>
This challenge is similar to the previous challenge. The only difference is that the directory path is longer than the previous one.<br/>
command- cd /usr/share/zoneinfo/posix/Asia<br/>
         /challenge/run<br/>


6.Implicit Relative Paths, From /:
The challenge wants us to invoke using / command, so "cd /" will open the home directory and the invoking "challenge/run" would give us the flag.
command- cd /
         challenge/run


8.Explicit Relative Paths, From /:<br/>
 A relative path must used with /. While invoking "/challenge/run", start the command with "." to remain in the same directory(./challenge/run).<br/>
command- cd /<br/>
         ./challenge/run<br/>


9.Implicit Relative Paths<br/>
The program must be invoked from the challenge directory rather than the home directory. After changing directory, just using the naked command "run" would result in an error since  will search for programs with same name outside of the current directory as well. "./run" would search for programs in the current directory.<br/>
command- cd /challenge<br/>
         ./run<br/>


Home Sweet Homw
In this challenge we will first create a file having a single character("t") as its name with the "touch" command and then invoke the file in /challenge/run using ~ prompt which repesents home/hacker in pwn.college. "~/.t" would be the argument for /challenge/run.
command- touch t
         /challenge/run ~/t
