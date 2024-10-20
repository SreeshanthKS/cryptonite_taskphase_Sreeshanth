#Level 0

root@DESKTOP-DCDALLM:~# ssh [bandit0@](mailto:bandit0@bandit.labs.overthewire.org)**bandit.labs.overthewire.org**-p 2220
The authenticity of host '[[bandit.labs.overthewire.org](http://bandit.labs.overthewire.org/)]:2220 ([16.16.163.126]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[[bandit.labs.overthewire.org](http://bandit.labs.overthewire.org/)]:2220' (ED25519) to the list of known hosts.
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

[bandit0@bandit.labs.overthewire.org](mailto:bandit0@bandit.labs.overthewire.org)'s password:

```
  ,----..            ,----,          .---.
 /   /   \\         ,/   .`|         /. ./|
/   .     :      ,`   .'  :     .--'.  ' ;

```

.   /   ;.  \   ;    ;     /    /__./ \ : |
.   ;   /  `; .'___,/    ,' .--'.  '   \\' .   ;   |  ; \\ ; | |    :     | /___/ \\ |    ' '   |   :  | ; | ' ;    |.';  ; ;   \\  \\;      :   .   |  ' ' ' :`----'  |  |  \   ;       `|   '   ;  \\; /  |     '   :  ;   .   \\    .\\  ;    \\   \\  ',  /      |   |  '    \\   \\   ' \\ |     ;   :    /       '   :  |     :   '  |--"      \\   \\ .'        ;   |.'       \\   \\ ;   www.`---` ver     '---' he       '---" [ire.org](http://ire.org/)

Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

- -[ Playing the games ]--

This machine might hold several wargames.
If you are playing "somegame", then:

```
* USERNAMES are somegame0, somegame1, ...
* Most LEVELS are stored in /somegame/.
* PASSWORDS for each level are stored in /etc/somegame_pass/.

```

Write-access to homedirectories is disabled. It is advised to create a
working directory with a hard-to-guess name in /tmp/.  You can use the
command "mktemp -d" in order to generate a random and hard to guess
directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
restricted so that users cannot snoop on eachother. Files and directories
with easily guessable or short names will be periodically deleted! The /tmp
directory is regularly wiped.
Please play nice:

```
* don't leave orphan processes running
* don't leave exploit-files laying around
* don't annoy other players
* don't post passwords or spoilers
* again, DONT POST SPOILERS!
  This includes writeups of your solution on your blog or website!

```

- -[ Tips ]--

This machine has a 64bit processor and many security-features enabled
by default, although ASLR has been switched off.  The following
compiler flags might be interesting:

```
-m32                    compile for 32bit
-fno-stack-protector    disable ProPolice
-Wl,-z,norelro          disable relro

```

In addition, the execstack tool can be used to flag the stack as
executable on ELF binaries.

Finally, network-access is limited for most levels by a local
firewall.

- -[ Tools ]--

For your convenience we have installed a few useful tools which you can find
in the following locations:

```
* gef (<https://github.com/hugsy/gef>) in /opt/gef/
* pwndbg (<https://github.com/pwndbg/pwndbg>) in /opt/pwndbg/
* gdbinit (<https://github.com/gdbinit/Gdbinit>) in /opt/gdbinit/
* pwntools (<https://github.com/Gallopsled/pwntools>)
* radare2 (<http://www.radare.org/>)

```

- -[ More information ]--

For more information regarding individual wargames, visit
http://www.overthewire.org/wargames/

For support, questions or comments, contact us on discord or IRC.

Enjoy your stay!

#Level 0 —→ Level 1

bandit0@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit1 bandit0 438 Sep 19 07:08 readme
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

#Level 1 → Level 2

bandit1@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit2 bandit1 33 Sep 19 07:08 -
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx

#Level 2 → Level 3

bandit2@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit3 bandit2 33 Sep 19 07:08 spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

#Level 3 → Level 4

bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ find
.
./...Hiding-From-You
bandit3@bandit:~/inhere$ cat Hiding-From-You
cat: Hiding-From-You: No such file or directory
bandit3@bandit:~/inhere$ cat ./...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
bandit3@bandit:~/inhere$ exit

#Level 4 → Level 5

bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ ls -l
total 40
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file00
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file01
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file02
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file03
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file04
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file05
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file06
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file07
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file08
-rw-r----- 1 bandit5 bandit4 33 Sep 19 07:08 -file09
bandit4@bandit:~/inhere$ cat ./-file00
p&y,(jo.at:uf^@bandit4@bandit:~/inhere$ cat ./-file01
iR,Λ:Y?%ABͩbandit4@bandit:~/inhere$ cat ./-file02
3       )Ʈ#Y-6cIR-$:bandit4@bandit:~/inhere$ cat ./-file03
/qGi,2Yb
dbandit4@bandit:~/inhere$ cat ./-file04
ۙrOxh0~ey
c~hnG1bandit4@bandit:~/inhere$ cat ./-file05
}ߓߤW>#lkdܮyEbandit4@bandit:~/inhere$ cat ./-file06
60]\$1%o@b/bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

#Level 5 → Level 6

bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ find -readable -size 1033c !-executable
-bash: !-executable: event not found
bandit5@bandit:~/inhere$ find -readable -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

#Level 6 → Level 7

bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/root’: Permission denied
find: ‘/snap’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1984388/task/1984388/fd/6’: No such file or directory
find: ‘/proc/1984388/task/1984388/fdinfo/6’: No such file or directory
find: ‘/proc/1984388/fd/5’: No such file or directory
find: ‘/proc/1984388/fdinfo/5’: No such file or directory
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/etc/polkit-1/rules.d’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/etc/stunnel’: Permission denied
find: ‘/etc/xinetd.d’: Permission denied
find: ‘/etc/credstore.encrypted’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/credstore’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/var/log/amazon’: Permission denied
find: ‘/var/log/unattended-upgrades’: Permission denied
find: ‘/var/log/chrony’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/apparmor/2425d902.0’: Permission denied
find: ‘/var/cache/apparmor/baad73a1.0’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/udisks2’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/boot/lost+found’: Permission denied
find: ‘/sys/kernel/tracing’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/systemd/propagate/systemd-udevd.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-resolved.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-networkd.service’: Permission denied
find: ‘/run/systemd/propagate/irqbalance.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-logind.service’: Permission denied
find: ‘/run/systemd/propagate/chrony.service’: Permission denied
find: ‘/run/systemd/propagate/polkit.service’: Permission denied
find: ‘/run/systemd/propagate/ModemManager.service’: Permission denied
find: ‘/run/systemd/propagate/fwupd.service’: Permission denied
find: ‘/run/systemd/propagate/bolt.service’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/log/journal/ec2dd69f90c4a6285216f71caca9bbca’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/screen/S-bandit27’: Permission denied
find: ‘/run/screen/S-bandit28’: Permission denied
find: ‘/run/screen/S-bandit24’: Permission denied
find: ‘/run/screen/S-bandit17’: Permission denied
find: ‘/run/screen/S-bandit12’: Permission denied
find: ‘/run/screen/S-bandit29’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/screen/S-bandit1’: Permission denied
find: ‘/run/screen/S-bandit31’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-bandit22’: Permission denied
find: ‘/run/screen/S-bandit19’: Permission denied
find: ‘/run/screen/S-bandit30’: Permission denied
find: ‘/run/screen/S-bandit33’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit16’: Permission denied
find: ‘/run/screen/S-bandit0’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11028’: Permission denied
find: ‘/run/user/11024’: Permission denied
find: ‘/run/user/11027’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11032’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11026’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11021’: Permission denied
find: ‘/run/user/11022’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/8004’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11019’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11017’: Permission denied
find: ‘/run/user/11033’: Permission denied
find: ‘/run/user/11010’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/udisks2’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

#Level 7 → Level 8

bandit7@bandit:~$ grep millionth data.tx
grep: data.tx: No such file or directory
bandit7@bandit:~$ grep millionth data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

#Level 8 → Level 9

bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

#Level9 → Level 10

bandit9@bandit:~$ strings data.txt | grep =
}========== the
p\l=
;c<Q=.dEXU!
3JprD========== passwordi
qC(=
~fDV3========== is
7=oc
zP=
~de=
3k=fQ
~o=0
69}=
%"=Y
=tZ~07
D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
N=~[!N
zA=?0j

#Level 10 → Level 11

bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

