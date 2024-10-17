## 1. Changing File Ownership 

FLAG --- pwn.college{Is55DJyZGS420WdcegdRrzYg7Xo.dFTM2QDLxYjN0czW}

CODE --- 
hacker@permissions~changing-file-ownership:~$ ls -l
total 48
-rw-r--r-- 1 hacker hacker    4 Oct  9 13:58 COLLEGE
drwxr-xr-x 2 hacker hacker 4096 Oct  3 15:04 Desktop
-rw-r--r-- 1 hacker hacker   17 Oct 15 04:48 PWN
-rw-r--r-- 1 hacker hacker    4 Oct  9 13:58 college
-rw-r--r-- 1 root   hacker   77 Oct  9 16:24 error
-rw-r--r-- 1 hacker hacker  829 Oct  9 14:32 instructions
-rw-r--r-- 1 hacker hacker    0 Oct  9 14:23 my-flag
-rw-r--r-- 1 root   hacker   93 Oct  9 14:32 myflag
lrwxrwxrwx 1 hacker hacker    5 Oct  9 05:55 not-the-flag -> /flag
-rw-r--r-- 1 root   hacker   77 Oct  9 16:24 pwn
-rw-r--r-- 1 root   hacker   77 Oct  9 16:20 pwn_output
-rw-r--r-- 1 hacker hacker   18 Oct 15 04:48 random
-rw-r--r-- 1 hacker hacker  446 Oct  9 14:25 the-flag
drwxr-xr-x 2 hacker hacker 4096 Oct  8 08:20 tmp
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{Is55DJyZGS420WdcegdRrzYg7Xo.dFTM2QDLxYjN0czW}

## 2. Groups and Files 

FLAG --- pwn.college{cLBpJCnLaZmP0pmSJ933NBaJAvl.dFzNyUDLxYjN0czW}

CODE --- 
hacker@permissions~groups-and-files:~$ ls -l
total 48
-rw-r--r-- 1 hacker hacker    4 Oct  9 13:58 COLLEGE
drwxr-xr-x 2 hacker hacker 4096 Oct  3 15:04 Desktop
-rw-r--r-- 1 hacker hacker   17 Oct 15 04:48 PWN
-rw-r--r-- 1 hacker hacker    4 Oct  9 13:58 college
-rw-r--r-- 1 root   hacker   77 Oct  9 16:24 error
-rw-r--r-- 1 hacker hacker  829 Oct  9 14:32 instructions
-rw-r--r-- 1 hacker hacker    0 Oct  9 14:23 my-flag
-rw-r--r-- 1 root   hacker   93 Oct  9 14:32 myflag
lrwxrwxrwx 1 hacker hacker    5 Oct  9 05:55 not-the-flag -> /flag
-rw-r--r-- 1 root   hacker   77 Oct  9 16:24 pwn
-rw-r--r-- 1 root   hacker   77 Oct  9 16:20 pwn_output
-rw-r--r-- 1 hacker hacker   18 Oct 15 04:48 random
-rw-r--r-- 1 hacker hacker  446 Oct  9 14:25 the-flag
drwxr-xr-x 2 hacker hacker 4096 Oct  8 08:20 tmp
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{cLBpJCnLaZmP0pmSJ933NBaJAvl.dFzNyUDLxYjN0czW}

## 3. Fun With Group Names

FLAG --- pwn.college{8SELbCTzmjWT-wiBGsspOSNQwYs.dJzNyUDLxYjN0czW}

CODE ---
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp8557) groups=1000(grp8557)
hacker@permissions~fun-with-groups-names:~$ ls -l
total 48
-rw-r--r-- 1 hacker grp8557    4 Oct  9 13:58 COLLEGE
drwxr-xr-x 2 hacker grp8557 4096 Oct  3 15:04 Desktop
-rw-r--r-- 1 hacker grp8557   17 Oct 15 04:48 PWN
-rw-r--r-- 1 hacker grp8557    4 Oct  9 13:58 college
-rw-r--r-- 1 root   grp8557   77 Oct  9 16:24 error
-rw-r--r-- 1 hacker grp8557  829 Oct  9 14:32 instructions
-rw-r--r-- 1 hacker grp8557    0 Oct  9 14:23 my-flag
-rw-r--r-- 1 root   grp8557   93 Oct  9 14:32 myflag
lrwxrwxrwx 1 hacker grp8557    5 Oct  9 05:55 not-the-flag -> /flag
-rw-r--r-- 1 root   grp8557   77 Oct  9 16:24 pwn
-rw-r--r-- 1 root   grp8557   77 Oct  9 16:20 pwn_output
-rw-r--r-- 1 hacker grp8557   18 Oct 15 04:48 random
-rw-r--r-- 1 hacker grp8557  446 Oct  9 14:25 the-flag
drwxr-xr-x 2 hacker grp8557 4096 Oct  8 08:20 tmp

hacker@permissions~fun-with-groups-names:~$ chgrp grp8557 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{8SELbCTzmjWT-wiBGsspOSNQwYs.dJzNyUDLxYjN0czW}

## 4. Changing Permissions

FLAG---pwn.college{oywfKbYh5qwZguIndQ1NLNtfmAk.dNzNyUDLxYjN0czW}

CODE ---
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-------- 1 root root 58 Oct 17 09:38 /flag
hacker@permissions~changing-permissions:~$ chmod go+rwx
chmod: missing operand after ‘go+rwx’
Try 'chmod --help' for more information.
hacker@permissions~changing-permissions:~$ chmod go+rwx *
hacker@permissions~changing-permissions:~$ ls -l /flag
-r--rwxrwx 1 root root 58 Oct 17 09:38 /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{oywfKbYh5qwZguIndQ1NLNtfmAk.dNzNyUDLxYjN0czW}

## 5. Excecutable Files 

FLAG --- pwn.college{8MLZhBCm15k2LmJNV3HwZ00OXo-.dJTM2QDLxYjN0czW}

CODE ---
hacker@permissions~executable-files:~$ chmod ugo+x /challenge/run
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r-xr-xr-x 1 hacker hacker 32 Jul  4 06:37 /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{8MLZhBCm15k2LmJNV3HwZ00OXo-.dJTM2QDLxYjN0czW}

## 6. Permissions Tweaking Practice

FLAG --- pwn.college{gDCQoL7SlwqxgedY_gCfuKucxH0.dBTM2QDLxYjN0czW}

CODE ---
hacker@permissions~permission-tweaking-practice:~$ /challenge/run
Round 0 (of 8)!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwxr--r-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod u+x /challenge/pwn
NEEDED, BUT UNMET permissions of "/challenge/pwn": rwxr--r-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

CURRENT, INCORRECT permissions of "/challenge/pwn": rwxr--r--
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

You set the permissions incorrectly! Restarting the game!
hacker@permissions~permission-tweaking-practice:~$ chmod ou+x /challenge/pwn
You set the correct permissions!
Round 1 (of 8)!

Current permissions of "/challenge/pwn": rwxr--r-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxr-xr-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod g+x /challenge/pwn
You set the correct permissions!
Round 2 (of 8)!

Current permissions of "/challenge/pwn": rwxr-xr-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": -w-------
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod gou-rx /challenge/pwn
You set the correct permissions!
Round 3 (of 8)!

Current permissions of "/challenge/pwn": -w-------
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-------
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod u+r /challenge/pwn
You set the correct permissions!
Round 4 (of 8)!

Current permissions of "/challenge/pwn": rw-------
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": -w-------
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod u-r /challenge/pwn
You set the correct permissions!
Round 5 (of 8)!

Current permissions of "/challenge/pwn": -w-------
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwxrwx---
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod ug+rwx /challenge/pwn
You set the correct permissions!
Round 6 (of 8)!

Current permissions of "/challenge/pwn": rwxrwx---
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-rw----
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod ug-x /challenge/pwn
You set the correct permissions!
Round 7 (of 8)!

Current permissions of "/challenge/pwn": rw-rw----
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-rw-r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod o+r /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ ls -l /flag
---------- 1 hacker hacker 58 Oct 17 09:52 /flag
hacker@permissions~permission-tweaking-practice:~$ chmod u+r /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{gDCQoL7SlwqxgedY_gCfuKucxH0.dBTM2QDLxYjN0czW}

## 7. Permissions Setting Practice 

FLAG --- pwn.college{Qxt7gCE22R4m2qE_BHmAh9WYE7C.dNTM5QDLxYjN0czW}

CODE ---
hacker@permissions~permissions-setting-practice:~$ /challenge/run
Round 0 (of 8)!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r--rwx--x
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=r,g=rwx,o=x /challenge/pwn
You set the correct permissions!
Round 1 (of 8)!

Current permissions of "/challenge/pwn": r--rwx--x
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": -w-r--rwx
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=w,g=r,o=rwx /challenge/pwn
You set the correct permissions!
Round 2 (of 8)!

Current permissions of "/challenge/pwn": -w-r--rwx
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": --xr-x-w-
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=x,g=rx,o=w /challenge/pwn
You set the correct permissions!
Round 3 (of 8)!

Current permissions of "/challenge/pwn": --xr-x-w-
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": --xrwxrw-
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=x,g=rwx,o=rw /challenge/pwn
You set the correct permissions!
Round 4 (of 8)!

Current permissions of "/challenge/pwn": --xrwxrw-
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw--wx---
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=rw,g=wx,o=- /challenge/pwn
You set the correct permissions!
Round 5 (of 8)!

Current permissions of "/challenge/pwn": rw--wx---
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw---xrw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=rw,g=x,o=rw /challenge/pwn
You set the correct permissions!
Round 6 (of 8)!

Current permissions of "/challenge/pwn": rw---xrw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": -wxr--rw-
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=wx,g=r,o=rw /challenge/pwn
You set the correct permissions!
Round 7 (of 8)!

Current permissions of "/challenge/pwn": -wxr--rw-
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r----x-wx
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod u=r,g=x,o=wx /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ ls -l /flag
---------- 1 hacker hacker 58 Oct 17 10:01 /flag
hacker@permissions~permissions-setting-practice:~$ chmod u+r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{Qxt7gCE22R4m2qE_BHmAh9WYE7C.dNTM5QDLxYjN0czW}

## 8. The SUID Bit 

FLAG ---pwn.college{k6qKuS2NsLBX_4aWOh6bM1m9pv0.dNTM2QDLxYjN0czW}

CODE --- 
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwxr-xr-x 1 root root 155 Jul 12 10:30 /challenge/getroot
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{k6qKuS2NsLBX_4aWOh6bM1m9pv0.dNTM2QDLxYjN0czW}
