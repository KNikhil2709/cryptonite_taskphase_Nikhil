THE ROOT
The flag is captured captured by invoking the "pwn" program using its absolute path.
command- /pwn


Program and Absolute Paths
Invoking "challenge" directory and "run" program in the terminal will give us the flag for this challenge.
command- /challenge/run


Position THY Self
By changing directory(cd /directoryname) to "etc" directory and then invoking the "challenge" directory with "run" program will give us the flag.
command- cd /etc
        /challenge/run


Positon Elsewhere
By first invoking "/challenge/run" provides with the location of the directory i.e., /proc/301. By changing directory to /proc/301 and then invoking /challenge/run.
command- cd /proc/301.
        /challenge/run
        

Position Yte Elsewhere
This challenge is similar to the previous challenge. The only difference is that the directory path is longer than the previous one.
command- cd /usr/share/zoneinfo/posix/Asia
         /challenge/run


Implicit Relative Paths, From /:
The challenge wants us to invoke using / command, so "cd /" will open the home directory and the invoking "challenge/run" would give us the flag.
command- cd /
         challenge/run


Explicit Relative Paths, From /:
 A relative path must used with /. While invoking "/challenge/run", start the command with "." to remain in the same directory(./challenge/run).
command- cd /
         ./challenge/run


Implicit Relative Paths
The program must be invoked from the challenge directory rather than the home directory. After changing directory, just using the naked command "run" would result in an error since  will search for programs with same name outside of the current directory as well. "./run" would search for programs in the current directory.
command- cd /challenge
         ./run


Home Sweet Homw
In this challenge we will first create a file having a single character("t") as its name with the "touch" command and then invoke the file in /challenge/run using ~ prompt which repesents home/hacker in pwn.college. "~/.t" would be the argument for /challenge/run.
command- touch t
         /challenge/run ~/t
