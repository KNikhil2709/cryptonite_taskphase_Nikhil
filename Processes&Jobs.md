1. Listing Processes<br/>
   flag: pwn.college{8nhQbe7FgnA527OA-QZlFk2Vz4K.dhzM4QDL5cjN0czW}<br/>
   We use "ps -ef" command to list all the running programs in the terminal and in the list we find "/challenge/31360-run-2871"<br/>
   Upon running this we get the flag<br/>

2.Killing Processes<br/>
  flag: pwn.college{s_994luynkNhaYpILv-AgtzY4AD.dJDN4QDL5cjN0czW}<br/>
  First we use the "ps -ef" command to list all the runnig programs and then we find that the PID code of /challenge/dont_run is 73.<br/>
  So we use "kill 73" command to stop it.<br/>
  And then upon running /challenge/run we get the flag.<br/>

3.Interrupting Processes<br/>
flag: pwn.college{4HebQ2iWiQqm4zWW96rXXZCUDf9.dNDN4QDL5cjN0czW}<br/>
Upon running /challenge/run<br/>
We ctrl+c to interrup the process to get the flag<br/>

4. Suspending Processes<br/>
flag: pwn.college{8o2o_SwVgzqj_SKMQDYeavR5WoY.dVDN4QDL5cjN0czW}<br/>
We can use Ctrl-Z to suspend a process in the background. This allows us to run the same process multiple times at the same time.<br/>
This is exactly what we need to do for this challenge.<br/>
~$ /challenge/run<br/>
^Z<br/>
~$ /challenge/run<br/>

5. Resuming Processes<br/>
   flag: pwn.college{Q1Hix_BDP97aLg4AdMwfiZj6C3b.dZDN4QDL5cjN0czW}<br/>
   To resume a suspended prgram we use the fg command and use the prgram as it's argument.<br/>
   ~$ /challenge/run<br/>
   ^Z<br/>
   ~$ fg /challenge/run<br/>

6. Backgrounding Processes<br/>
   flag: pwn.college{wLkSyo-7Z6R6eZdqTM7USVftlau.ddDN4QDL5cjN0czW}<br/>
   We can use the 'bg' command to resume a suspended process (and run the program in the background).<br/>
In this challenge we will get the flag if we run the program with the program also being run in the background<br/>
~$ /challenge/run<br/>
^Z<br/>
~$ bg /challenge/run<br/>
~$ /challenge/run


7.Foregrounding Processes<br/>
flag: pwn.college{Ms9yfoEvoOqB1kkXS_Qu8CwMlIO.dhDN4QDL5cjN0czW}<br/>
In this challenge we need to use 'fg' to foreground a process which is already running in the background.<br/>
~$ /challenge/run<br/>
^Z<br/>
~$ bg /challenge/run<br/>
~$ fg /challenge/run<br/>


8. Starting Backgrounded Processes<br/>
   flag: pwn.college{Au-tIiTVNhdLZ8i1EWqHZeIofSL.dlDN4QDL5cjN0czW}<br/>
   We can append '&' to the program to to background a process without having to suspend it first.<br/>
   ~$ /challenge/run & will give us the flag<br/>

9. Process Exit Codes<br/>
    flag: pwn.college{gRcD71DtVnsymy2ylpE3i_8Pc69.dljN4UDL5cjN0czW}<br/>
   In this challenge we need to find the exit code for '/challenge/get-code' and then run '/challenge/submit-code' with that error code as an argument.
   The exit code is stored in '?'<br/>

   ~$ /challenge/get-code<br/>
   ~$ echo $?<br/>
   ~$ /challenge/submit-code 203<br/>
