## 1. MACTCHING THE * 

So in the program we will be basically filling the empty spaces....like you don't have to type an entire line of command....
For ex. /challenge is equal to /ch*

FLAG ---pwn.college{sHWXenj--rLrc5GiWO30Nu7UNjE.dFjM4QDLxYjN0czW}

CODE ---
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{sHWXenj--rLrc5GiWO30Nu7UNjE.dFjM4QDLxYjN0czW}
.
.
.
## 2. MATCHING WITH THE ?

Unlike our * argument which access all the missing characters... '?' can only access a single character

Flag --- pwn.college{kd0nqYTyBgrhMuO2LAJuI1qTw2e.dJjM4QDLxYjN0czW}

Code ---

hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kd0nqYTyBgrhMuO2LAJuI1qTw2e.dJjM4QDLxYjN0czW}
.
.
.
## 3. MATCHING WITH []

 The square brackets are essentially a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets.
 So whatever characters we specify within the [] will be accessed individually with the argument attached 
 For Ex:
 file_[ab] would result in file_a and file_b

 FLAG --- pwn.college{4eFPqMwGexysovEa3gYgXNMhkK_.dNjM4QDLxYjN0czW}

CODE ---
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run [absh]
Your expansion did not expand to the requested files (file_a, file_b, file_h, 
and file_s). Instead, it expanded to:
[absh]
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{4eFPqMwGexysovEa3gYgXNMhkK_.dNjM4QDLxYjN0czW}
.
.
.
## 4. MATCHING PATH WITH []

GLOB statements happens on path basis too
Basically, we can expand entire paths using this.

FLAG --- pwn.college{U0whRu9DOfAuzur2D2TRgXdNolg.dRjM4QDLxYjN0czW}

CODE ---

hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{U0whRu9DOfAuzur2D2TRgXdNolg.dRjM4QDLxYjN0czW}
.
.
.
## 5. MIXING GLOBS

This is more practice of whatever we did till now.

FLAGS --- pwn.college{0CyxzoN6R0v8OgyMuJUegVuW6rq.dVjM4QDLxYjN0czW}

CODE ---
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
[cep]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{0CyxzoN6R0v8OgyMuJUegVuW6rq.dVjM4QDLxYjN0czW}
hacker@globbing~mixing-globs:/challenge/files$ 
.
.
.
.
## 6. EXCLUIONARY  GLOBBING 

Unlike last commands like [bash] used to match every single letter in bracket...this time it will exclude every single letter when we use ! or ^ with the letters like [!bash]

FLAG --- pwn.college{odgoqJvwhUYofhiZl55SzBycEzp.dZjM4QDLxYjN0czW}

CODE ---
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]
Your expansion did not expand to the requested files (amazing beautiful 
challenging delightful educational fantastic great happy incredible jovial kind 
laughing magical optimistic queenly radiant splendid thrilling uplifting 
victorious xenial youthful zesty).
Instead, it expanded to:
[!pwn]
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{odgoqJvwhUYofhiZl55SzBycEzp.dZjM4QDLxYjN0czW}
