1.FLAGGED<br/>
The flag was the description of #rules in the disocrd server<br/>
FLAG:-OASIS{0H_SN4P_Y0U_F0UND_M3_1N_7H3_D3SCR1P710N}<br/>


2.THIS OR THAT?<br/>
We found out that the given sequence of characters represents a XOR Cipher text.<br/>
Ciphertext - 036363127c7c60001a117c6463170b<br/>
key - ARTEMIS_WHISPER<br/>
I used chatgpt to decrypt this since i don't know how to do it<br/>
The result was B17W153_MY573RY<br/>
Flag:- OASIS{B17W153_MY573RY}<br/>


3.STRING ME TO SLEEP<br/>
Flag was present in the file itself. I used ctrl+f command to find the flag<br/>
Flag:- OASIS{y0u_fou7d_m3}<br/>


4.GIT GUD<br/>
There were many files in the given .git folder.<br/>
As i was going through all the text files i came across the logs folder which contained a master text file.<br/>
I used chatgpt to extract the flag out where it used git log | grep '    ' | tac | tr -d ' ' | tr -d '\n'<br/>
It gave the flag as output.<br/>
Flag:- OASIS{g3t_gu663r_4t_g!t!!}<br/>
