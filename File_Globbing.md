1.Matching with *<br/>
The glob * will be used in this challenge.<br/>
When the shell encounters the * glob it treats it as a wildcard and will replace that argument with any file that mathces the pattern<br/>
For example if we give it the argument '/ch*', then all files starting with 'ch' will be taken<br/>
Command- cd /ch*<br/>
        /challenge$ /challenge/run<br/>


2.Matching with ?<br/>
Here'?' matches only one character unlike '*'<br/>
Command- cd /?ha??enge<br/>
         $ /challenge/run<br/>  


3.Matching with []<br/>
The [] matches the character with any of the characters given inside the brackets.<br/>
Command- cd /challenge/files<br/>
         /challenge/files$ /challenge/run file_[asdf]<br/>


4.Matching paths with []<br/>
Here we use path of the file as an arguments for the globs.<br/>
Command- /challenge/run /challenge/files/file_[bash]<br/>

5.Mixing Globs<br/>
We need to match the files- "challenging", "educational", "pwing"<br/>
The only common characters in all 3 files are 'i' and 'n'<br/>
on running the 'ls' command we find that the files in '/challenge/files' are-<br/>

amazing   beautiful    challenging    delightful     educational <br/>
fantastic great   happy    incredible   jovial    kind    laughing <br/>
magical    nice      optimistic    pwning     queenly   radiant <br/>
splendid   thrilling   uplifting victorious     wonderful    xenial  <br/>  
youthful zesty<br/>

Since all of the file names start with a different letter and we need to run the files "challenging", "educational", "pwing", we can use the argument '[pec]*', this argument will use all the files starting with p,e or c<br/>
Command- cd/challenge/files<br/>
         /challenge/run [cep]*<br/>



6.Exclusionary Globbing<br/>
The ^ character in [] will invert the functionality of the glob and use the files which dont have the characters entered, since we need to use the files not starting with p,w,n, our argument will be- [^pwn]*<br/>
Command- cd /challenge/files<br/>
        /challenge/files$ /challenge/run [^pwn]*<br/>
