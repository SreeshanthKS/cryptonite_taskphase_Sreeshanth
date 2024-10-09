#1 THE ROOT 

Here we have been given a filesystem '/' which contains the file 'pwn' , so we just have to access it.

PROGRAM: 
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{wLbWnblfBP0fc9BZJRQuU2nuNFq.dhzN5QDLxYjN0czW}
.
.
.
#2 PROGRAM AND ABSOLUTE PATHS

In this program we have to basically run the path '/challenge/run' to obtain the flag 

FLAG -- pwn.college{UHe2tSOkhWs2eEW_G9tTIX9PtbD.dVDN1QDLxYjN0czW}

CODE -- 
hacker@paths~program-and-absolute-paths:~$ /challenge/run
.
.
.
#3 POSITION THY SELF 

This program is teaching us how to 'cd' in to the directory and here we have to 'cd' into the directory in which the /challenge/path is resting and then obtain the 'flag'

FLAG --- pwn.college{UdZiQhkx7F1AOYDbEVGNd1-YnyE.dZDN1QDLxYjN0czW}

CODE --- 
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /etc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd/etc 
bash: cd/etc: No such file or directory
hacker@paths~position-thy-self:~$ cd /etc
hacker@paths~position-thy-self:/etc$ /challenge/run
.
.
.
#4 POSITION ELSEWHERE

We are gonna be doing the same thing as the last one 

FLAG --- pwn.college{IK2H3eIgiit_TGATwG6sjh9Pnz9.ddDN1QDLxYjN0czW}

CODE ---
hacker@paths~position-elsewhere:~$ /challenge/run 
Incorrect...
You are not currently in the /proc/216 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /proc/216
hacker@paths~position-elsewhere:/proc/216$ /challenge/run]
.
.
.
#5 POSITION YET ELSEWHERE

Sigh... We gotta do the same thing as last time again 

FLAG ---pwn.college{MjFCqbM2av-E6u5BKMh5hijLeYi.dhDN1QDLxYjN0czW}

CODE ---
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /sys
hacker@paths~position-yet-elsewhere:/sys$ /ch*/r*
.
.
.
#6 IMPLICIT RELATIVE PATHS, FROM / 

Here we have to cd the '/' first which becomes the cwd (current working directory) and then we run the relative path (in this case 'challenge/run') ,which DOESN'T START WITH A /,to obtain the flag

FLAG --- pwn.college{gQIWVOvK8TgdRcoPVZkwa46AUzR.dlDN1QDLxYjN0czW}

CODE --- 
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
.
.
.
#7 EXPLICIT RELATIVE PATHS , FROM / 

Here we learn about two implicit entries which we can use in paths 
. refers to the same directory and .. refers to the parent directory

In this program we will have to bascially cd into the cwd i.e. '/' and then use '.' in the begining of the next command to access the same directory and run it to obtain the 'flag'

FLAG --- pwn.college{MdHIestvniwGHJzs36qVbncznwb.dBTN1QDLxYjN0czW}

CODE --- 
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
.
.
.
#8 IMPLICIT RELATIVE PATH 

Same as the last one but this time we will be CDing into /challenge and make it the cwd

FLAG ---pwn.college{4Vs9dLB_lKdjk0uXI3kKsWvQOmD.dFTN1QDLxYjN0czW}

CODE ---
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
