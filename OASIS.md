FLAGGED
The flag was the description of #rules in the disocrd server
FLAG:-OASIS{0H_SN4P_Y0U_F0UND_M3_1N_7H3_D3SCR1P710N}


THIS OR THAT?
We found out that the given sequence of characters represents a XOR Cipher text.
Ciphertext - 036363127c7c60001a117c6463170b
key - ARTEMIS_WHISPER
I used chatgpt to decrypt this since i don't know how to do it
The result was B17W153_MY573RY
Flag:- OASIS{B17W153_MY573RY}


STRING ME TO SLEEP
Flag was present in the file itself. I used ctrl+f command to find the flag
Flag:- OASIS{y0u_fou7d_m3}


GIT GUD
There were many files in the given .git folder.
As i was going through all the text files i came across the logs folder which contained a master text file.
I used chatgpt to extract the flag out where it used git log | grep '    ' | tac | tr -d ' ' | tr -d '\n'
It gave the flag as output.
Flag:- OASIS{g3t_gu663r_4t_g!t!!}
