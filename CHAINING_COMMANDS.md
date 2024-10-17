## 1. Chaining With Semicolons 

Run /challenge/pwn and then /challenge/college, chaining them with a semicolon.

FLAG --- pwn.college{IQP42W94EtdQTcfFqM_-MBusx_N.dVTN4QDLxYjN0czW}

CODE ---
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn;/challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{IQP42W94EtdQTcfFqM_-MBusx_N.dVTN4QDLxYjN0czW}

## 2. Your First Shell Script
Run /challenge/pwn and then /challenge/college, but this time in a shell script called x.sh, then run it with bash!

FLAG --- pwn.college{0YNkZ14YOCLAMxU1B88JzhFnBWc.dFzN4QDLxYjN0czW}

CODE ---
hacker@chaining~your-first-shell-script:~$ echo "/challenge/pwn;/challenge/college" > x.sh
hacker@chaining~your-first-shell-script:~$ ls
COLLEGE  Desktop  PWN  college  error  instructions  my-flag  myflag  not-the-flag  pwn  pwn_output  random  the-flag  tmp  x  x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{0YNkZ14YOCLAMxU1B88JzhFnBWc.dFzN4QDLxYjN0czW}

## 3. Redirecting Script Output

FLAG --- pwn.college{46Wo29flG9YR-WoWj57gaRLxhCc.dhTM5QDLxYjN0czW}


CODE ---
hacker@chaining~redirecting-script-output:~$ echo "/challenge/pwn;/challenge/college" > x.sh
hacker@chaining~redirecting-script-output:~$ ls
COLLEGE  Desktop  PWN  college  error  instructions  my-flag  myflag  not-the-flag  pwn  pwn_output  random  the-flag  tmp  x  x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh > /challenge/solve
No shenanigans with bash options yet, please! Just run your script with 'bash 
x.sh'.
bash: /challenge/solve: Permission denied
hacker@chaining~redirecting-script-output:~$ bash x.sh
It looks like you are not piping this script out to /challenge/solve! Remember 
to pipe the output of your script into /challenge/solve using '|'.
hacker@chaining~redirecting-script-output:~$ x.sh | /challenge/solve
bash: x.sh: command not found
The data piped from /challenge/pwn did not match what I expected. I 
re-randomize the data every time you input a new line to the shell, so you must 
get it right in one shot! Make sure to pipe the output from your script to 
/challenge/solve.
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{46Wo29flG9YR-WoWj57gaRLxhCc.dhTM5QDLxYjN0czW}

## 4. Executable Shell Scripts

FLAG ---pwn.college{4OyZwKzOT6LLteITNmh7N2zQ2-q.dRzNyUDLxYjN0czW}

CODE ---
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > x.sh
hacker@chaining~executable-shell-scripts:~$ ls
COLLEGE  Desktop  PWN  college  error  instructions  my-flag  myflag  not-the-flag  pwn  pwn_output  random  the-flag  tmp  x  x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
bash: ./x.sh: Permission denied
hacker@chaining~executable-shell-scripts:~$ chmod u+rwx ./x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{4OyZwKzOT6LLteITNmh7N2zQ2-q.dRzNyUDLxYjN0czW}
 
