## 1. REDIRECTING OUTPUT

In this prg we will redirect the output from pWN to COLLEGE using the cmd '>'

FLAG --- pwn.college{An3wxoJGMepM44GSKZIcYsRa7Cz.dRjN1QDLxYjN0czW}

CODE --- 

hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! 
.
.
.
## 2. REDIRECTING MORE OUTPUT

In this prg we will be redirecting the output of /challenge/run to another file /myflag using the same cmd '>'

FLAG --- pwn.college{gtNIJx9qQtume2YzwjdnjTebLda.dVjN1QDLxYjN0czW}

CODE ----
hacker@piping~redirecting-more-output:~$ /challenge/run > ~/myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat ~/myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{gtNIJx9qQtume2YzwjdnjTebLda.dVjN1QDLxYjN0czW}

.
.
.
## 3. APPENDING OUTPUT

When we used to use > cmd it used to create a new output file every time
Instead of that, we can use >> cmd which is an append cmd that appends the output into the file.


FLAG ---pwn.college{4aOtbOyNHbObdvhnlT3VieBrTJs.ddDM5QDLxYjN0czW}

CODE ---
hacker@piping~appending-output:~$ /challenge/run >> ~/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat ~/the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{4aOtbOyNHbObdvhnlT3VieBrTJs.ddDM5QDLxYjN0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
.
.
.
## 4. REDIRECTING ERRORS 

Here we saw about FD i.e., file descriptor number.
Basically when we just used > it meant 1>, which is a default when you put this > empty
And 2> is for Standard errors 
And 0> is for standard input 

In this prg we have to just put standard output to myflag and standard error to instructions 

FLAG ---pwn.college{05dHpkCCOi_FswS6O3ItUV-qdKe.ddjN1QDLxYjN0czW}

CODE ---
hacker@piping~redirecting-errors:~$ /challenge/run > ~/myflag 2> ~/instructions
hacker@piping~redirecting-errors:~$ cat ~/myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{05dHpkCCOi_FswS6O3ItUV-qdKe.ddjN1QDLxYjN0czW}
.
.
.
## 5. REDIRECTING INPUT 

Here, we will practice using /challenge/run, which will require us to redirect the PWN file to it and have the PWN file contain the value COLLEGE

FLAG ---pwn.college{E5ipE_C_eRRuNsr8EqAqWFAa9Ry.dBzN1QDLxYjN0czW}

CODE ---
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{E5ipE_C_eRRuNsr8EqAqWFAa9Ry.dBzN1QDLxYjN0czW}

## 6. GREPPING STORED RESULTS

Here we are gonna be using the knowledge of grepping and stdout together.
We will be redirecting output from one file to another and then grepping that for the flag

FLAG ---pwn.college{QpB629TYzD6KQzoBDMVv118TiYi.dhTM4QDLxYjN0czW} 

CODE ---
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.tx
grep: /tmp/data.tx: No such file or directory
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{QpB629TYzD6KQzoBDMVv118TiYi.dhTM4QDLxYjN0czW}
.
.
.
## 7. GREPPING LIVE OUTPUT 

So, here we learn that we don't have to keep redirecting the output every single time and instead we can directly grep into it using the | cmd which is called 'piping' 

FLAG --- pwn.college{UrGaO3VygT_4gwL7_CnlQc9nB-X.dlTM4QDLxYjN0czW}

CODE ---
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.colleg
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{UrGaO3VygT_4gwL7_CnlQc9nB-X.dlTM4QDLxYjN0czW}
.
.
.
## 8. GREPPING ERRORS
Here we are redirecting the std error to stdout and then piping it out and all in one argument

FLAG --- pwn.college{Y_khlAQ1QnBpaUWOd0Jzp7LVuYm.dVDM5QDLxYjN0czW}

CODE ---
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{Y_khlAQ1QnBpaUWOd0Jzp7LVuYm.dVDM5QDLxYjN0czW}
.
.
.
## 9. DUPLICATING PIPED DATA WITH TEE

Here we learn about the tee cmd to duplicate data flowing through the pipes to any number of files provided on the command line.

FLAG --- pwn.college{UQ7w9LXkqdn3VLoqyvz_Ue6aG9V.dFjM5QDLxYjN0czW}

CODE --- 
acker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "UQ7w9LXk"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret UQ7w9LXk
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee' 
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn  --secret UQ7w9LXk  | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{UQ7w9LXkqdn3VLoqyvz_Ue6aG9V.dFjM5QDLxYjN0czW}








## 10. WRITING TO MULTIPLE PROGRAMS 

In the prg we are doing process substitution thru >cmd which will send the cmd output to the input directly. Here we are directing output of /challenge/hack to /challenge/the and /challenge/planet 

FLAG --- pwn.college{A5PMv1hKIWVsFPrycEGCin_ZkPB.dBDO0UDLxYjN0czW}

CODE---
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
15404945268973973
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{A5PMv1hKIWVsFPrycEGCin_ZkPB.dBDO0UDLxYjN0czW}
.
.
.
## 11. SPLIT-PIPPING STDERR AND STDOUT

Now here we will be combining the knowledge all four previous prgs

So here we are redirecting stdout of /challenge/hack to /challenge/planet and stderr of /challenge/hack to /challenge/the

So first of we will be using > this for stdout and this 2> for std err and >cmd for process substitution i.e. transferring the cmd output to the cmd input

FLAG --- pwn.college{YYtCmVaffBZwm5UuIrZqJPgi7HX.dFDNwYDLxYjN0czW}

CODE ---
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/the) 2> >(/challenge/planet)
Are you sure you're properly redirecting /challenge/hack's standard output into 
'/challenge/planet'?
Are you sure you're properly redirecting /challenge/hack's standard error into 
'/challenge/the'?
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack | tee > >(/challenge/the) 2> >(/challenge/planet)
You must redirect my standard error into '/challenge/the'!
Are you sure you're properly redirecting /challenge/hack's standard output into 
'/challenge/planet'?
Are you sure you're properly redirecting /challenge/hack's standard error into 
'/challenge/the'?
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack | > >(/challenge/the) 2> >(/challenge/planet)
Are you sure you're properly redirecting /challenge/hack's standard output into 
'/challenge/planet'?
You must redirect my standard error into '/challenge/the'!
Are you sure you're properly redirecting /challenge/hack's standard error into 
'/challenge/the'?
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{YYtCmVaffBZwm5UuIrZqJPgi7HX.dFDNwYDLxYjN0czW}


