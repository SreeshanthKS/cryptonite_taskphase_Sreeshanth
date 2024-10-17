## 1. Listing Process 

FLAG --- pwn.college{wLbO9r1jX2OFr4Be0LHdEV3Bbkd.dhzM4QDLxYjN0czW}

CODE --- 
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 04:58 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 04:58 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 04:58 ?        00:00:00 /challenge/21228-run-10952
root          72      68  0 04:58 ?        00:00:00 sleep 6h
hacker        81       1  2 04:59 ?        00:00:00 /nix/store/bmmjbvb8hishfrg78ygjlynpq3ikpl39-nodejs-20.15.1/bin/node /nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-s
hacker       104      81 14 04:59 ?        00:00:05 /nix/store/bmmjbvb8hishfrg78ygjlynpq3ikpl39-nodejs-20.15.1/bin/node /nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-s
hacker       145     104  9 04:59 ?        00:00:02 /nix/store/bmmjbvb8hishfrg78ygjlynpq3ikpl39-nodejs-20.15.1/bin/node --dns-result-order=ipv4first /nix/store/3v4hdb2gmp
hacker       163     104  2 04:59 ?        00:00:00 /nix/store/bmmjbvb8hishfrg78ygjlynpq3ikpl39-nodejs-20.15.1/bin/node /nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-s
hacker       223     163  0 04:59 pts/1    00:00:00 /run/dojo/bin/bash --init-file /nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/
hacker       339     163  0 04:59 ?        00:00:00 /bin/sh -c "/nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/out/vs/base/node/cp
hacker       340     339  0 04:59 ?        00:00:00 /nix/store/1xhds5s320nfp2022yjah1h7dpv8qqns-bash-5.2p32/bin/bash /nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-serv
hacker       343     340  0 04:59 ?        00:00:00 sleep 1
hacker       345     223  0 04:59 pts/1    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/21228-run-10952
Yahaha, you found me! Here is your flag:
pwn.college{wLbO9r1jX2OFr4Be0LHdEV3Bbkd.dhzM4QDLxYjN0czW}
Now I will sleep for a while (so that you could find me with 'ps')

## 2. Killing Processess 

FLAG --- pwn.college{k653MniKcD9Z5xjzfbFJ0pko4r2.dJDN4QDLxYjN0czW}

CODE --- 
hacker@processes~killing-processes:~$ ps -ef | grep /challenge/dont_run
hacker      1944     225  0 06:10 pts/1    00:00:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ kill 225
hacker@processes~killing-processes:~$ kill 1944
bash: kill: (1944) - No such process
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{k653MniKcD9Z5xjzfbFJ0pko4r2.dJDN4QDLxYjN0czW}

## 3. Interrupting Process 

FLAG --- pwn.college{oK5KM_Jyi9JuxPGlgKK83y9LvgG.dNDN4QDLxYjN0czW}

CODE --- 
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{oK5KM_Jyi9JuxPGlgKK83y9LvgG.dNDN4QDLxYjN0czW}

## 4. Suspending Process 

FLAG --- pwn.college{YZZ8tbYtS9R9oFrnY34PDsp6ado.dVDN4QDLxYjN0czW}

CODE ---
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         263     214  0 08:24 pts/1    00:00:00 bash /challenge/run
root         265     263  0 08:24 pts/1    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         263     214  0 08:24 pts/1    00:00:00 bash /challenge/run
root         420     214  0 08:25 pts/1    00:00:00 bash /challenge/run
root         422     420  0 08:25 pts/1    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{YZZ8tbYtS9R9oFrnY34PDsp6ado.dVDN4QDLxYjN0czW}

## 5. Resuming Processess 

FLAG --- pwn.college{A5MwUu5_gyU8xg4atnQyCZ5eUhi.dZDN4QDLxYjN0czW}

CODE --- 
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{A5MwUu5_gyU8xg4atnQyCZ5eUhi.dZDN4QDLxYjN0czW}
Don't forget to press Enter to quit me!

Goodbye!

## 6. Backgrounding Processess

FLAG --- pwn.college{MpIvSzUDzxeJPOumaN4qWmHEP_4.ddDN4QDLxYjN0czW}

CODE ---
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         220 S+   bash /challenge/run
root         222 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         220 S    bash /challenge/run
root         325 S    sleep 6h
root         499 S+   bash /challenge/run
root         501 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{MpIvSzUDzxeJPOumaN4qWmHEP_4.ddDN4QDLxYjN0czW}

## 7. Foregrounding Processes

FLAG --- pwn.college{soILdI3NoHD8wA36PTY7WqhHV5R.dhDN4QDLxYjN0czW}

CODE --- 
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{soILdI3NoHD8wA36PTY7WqhHV5R.dhDN4QDLxYjN0czW}

## 8. Starting Backgrounded Processes

FLAG --- pwn.college{cTQ2991w4YO91C_jsR7n_MMP6N4.dlDN4QDLxYjN0czW}

CODE --- 
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 274



hacker@processes~starting-backgrounded-processes:~$ Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{cTQ2991w4YO91C_jsR7n_MMP6N4.dlDN4QDLxYjN0czW}

## 9. Process Exit Codes

FLAG --- pwn.college{4hLgPI8kQT8e2pk3lWfW6gkGhj7.dljN4UDLxYjN0czW}

CODE --- 
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
52
hacker@processes~process-exit-codes:~$ /challenge/submit-code 52
CORRECT! Here is your flag:
pwn.college{4hLgPI8kQT8e2pk3lWfW6gkGhj7.dljN4UDLxYjN0czW}
