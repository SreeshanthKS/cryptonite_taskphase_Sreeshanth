## 1. Becoming Root with SU

FLAG --- pwn.college{Ai8GeqT8SW-l1agxHS-We_yy9lP.dVTN0UDLxYjN0czW}

CODE---
hacker@users~becoming-root-with-su:~$ su
Password: 
Hsu: Authentication failure
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{Ai8GeqT8SW-l1agxHS-We_yy9lP.dVTN0UDLxYjN0czW}

## 2. Other Users With SU

FLAG --- pwn.college{AfdeIFTl0FWTAXSBd3unWV6dt18.dZTN0UDLxYjN0czW}

CODE --- 
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ cat /flag
cat: /flag: Permission denied
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{AfdeIFTl0FWTAXSBd3unWV6dt18.dZTN0UDLxYjN0czW}

## 3. Cracking Passwords

FLAG --- pwn.college{oOdmzrwwpGUyzp8l_2xnYlHtKFI.ddTN0UDLxYjN0czW}

CODE ---
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:02 28% 1/3 0g/s 285.1p/s 285.1c/s 285.1C/s sudraz!..bzardus
0g 0:00:00:06 76% 1/3 0g/s 288.4p/s 288.4c/s 288.4C/s 9999945..Z9999932
0g 0:00:00:10 91% 1/3 0g/s 247.1p/s 247.1c/s 247.1C/s zardus999991978..zardus2002
0g 0:00:00:15 0% 2/3 0g/s 258.3p/s 258.3c/s 258.3C/s meggie..seattle
0g 0:00:00:17 0% 2/3 0g/s 261.9p/s 261.9c/s 261.9C/s keller..nation
0g 0:00:00:19 1% 2/3 0g/s 265.0p/s 265.0c/s 265.0C/s samsung..britney
0g 0:00:00:20 1% 2/3 0g/s 266.4p/s 266.4c/s 266.4C/s rosita..help
0g 0:00:00:21 1% 2/3 0g/s 267.5p/s 267.5c/s 267.5C/s nina..Joanna
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04599g/s 267.8p/s 267.8c/s 267.8C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ 
hacker@users~cracking-passwords:~$ 
hacker@users~cracking-passwords:~$ 
hacker@users~cracking-passwords:~$ 
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{oOdmzrwwpGUyzp8l_2xnYlHtKFI.ddTN0UDLxYjN0czW}

## 4. Using Sudo
Sudo access will be used to read the flag.
FLAG --- pwn.college{AaxuJ-D-qEG7bOaq1YgMYCiZSxz.dhTN0UDLxYjN0czW}

CODE ---
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{AaxuJ-D-qEG7bOaq1YgMYCiZSxz.dhTN0UDLxYjN0czW}
