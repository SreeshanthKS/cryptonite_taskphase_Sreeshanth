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

#Level11 → Level12

bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'A-MN-Za-mn-z'
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

#Level12 → Level 13

bandit12@bandit:~$ cd /tmp
bandit12@bandit:/tmp$ mktmp -d
Command 'mktmp' not found, did you mean:
command 'mktip' from deb kylin-display-switch (3.0.14-1build1)
command 'mktemp' from deb coreutils (9.4-2ubuntu2)
Try: apt install <deb name>
bandit12@bandit:/tmp$ mketmp -d
Command 'mketmp' not found, did you mean:
command 'mktemp' from deb coreutils (9.4-2ubuntu2)
Try: apt install <deb name>
bandit12@bandit:/tmp$ mktemp -d
/tmp/tmp.7XMuNpn4zO
bandit12@bandit:/tmp$ cp
cp: missing file operand
Try 'cp --help' for more information.
bandit12@bandit:/tmp$ cp data.txt
cp: missing destination file operand after 'data.txt'
Try 'cp --help' for more information.
bandit12@bandit:/tmp$ cp --help
Usage: cp [OPTION]... [-T] SOURCE DEST
or:  cp [OPTION]... SOURCE... DIRECTORY
or:  cp [OPTION]... -t DIRECTORY SOURCE...
Copy SOURCE to DEST, or multiple SOURCE(s) to DIRECTORY.

Mandatory arguments to long options are mandatory for short options too.
-a, --archive                same as -dR --preserve=all
--attributes-only        don't copy the file data, just the attributes
--backup[=CONTROL]       make a backup of each existing destination file
-b                           like --backup but does not accept an argument
--copy-contents          copy contents of special files when recursive
-d                           same as --no-dereference --preserve=links
--debug                  explain how a file is copied.  Implies -v
-f, --force                  if an existing destination file cannot be
opened, remove it and try again (this option
is ignored when the -n option is also used)
-i, --interactive            prompt before overwrite (overrides a previous -n
option)
-H                           follow command-line symbolic links in SOURCE
-l, --link                   hard link files instead of copying
-L, --dereference            always follow symbolic links in SOURCE
-n, --no-clobber             do not overwrite an existing file and do not fail
(overrides a -u or previous -i option). See also
--update; equivalent to --update=none.
-P, --no-dereference         never follow symbolic links in SOURCE
-p                           same as --preserve=mode,ownership,timestamps
--preserve[=ATTR_LIST]   preserve the specified attributes
--no-preserve=ATTR_LIST  don't preserve the specified attributes
--parents                use full source file name under DIRECTORY
-R, -r, --recursive          copy directories recursively
--reflink[=WHEN]         control clone/CoW copies. See below
--remove-destination     remove each existing destination file before
attempting to open it (contrast with --force)
--sparse=WHEN            control creation of sparse files. See below
--strip-trailing-slashes  remove any trailing slashes from each SOURCE
argument
-s, --symbolic-link          make symbolic links instead of copying
-S, --suffix=SUFFIX          override the usual backup suffix
-t, --target-directory=DIRECTORY  copy all SOURCE arguments into DIRECTORY
-T, --no-target-directory    treat DEST as a normal file
--update[=UPDATE]            control which existing files are updated;
UPDATE={all,none,older(default)}.  See below
-u                           equivalent to --update[=older]
-v, --verbose                explain what is being done
-x, --one-file-system        stay on this file system
-Z                           set SELinux security context of destination
file to default type
--context[=CTX]          like -Z, or if CTX is specified then set the
SELinux or SMACK security context to CTX
--help        display this help and exit
--version     output version information and exit

ATTR_LIST is a comma-separated list of attributes. Attributes are 'mode' for
permissions (including any ACL and xattr permissions), 'ownership' for user
and group, 'timestamps' for file timestamps, 'links' for hard links, 'context'
for security context, 'xattr' for extended attributes, and 'all' for all
attributes.

By default, sparse SOURCE files are detected by a crude heuristic and the
corresponding DEST file is made sparse as well.  That is the behavior
selected by --sparse=auto.  Specify --sparse=always to create a sparse DEST
file whenever the SOURCE file contains a long enough sequence of zero bytes.
Use --sparse=never to inhibit creation of sparse files.

UPDATE controls which existing files in the destination are replaced.
'all' is the default operation when an --update option is not specified,
and results in all existing files in the destination being replaced.
'none' is similar to the --no-clobber option, in that no files in the
destination are replaced, but also skipped files do not induce a failure.
'older' is the default operation when --update is specified, and results
in files being replaced if they're older than the corresponding source file.

When --reflink[=always] is specified, perform a lightweight copy, where the
data blocks are copied only when modified.  If this is not possible the copy
fails, or if --reflink=auto is specified, fall back to a standard copy.
Use --reflink=never to ensure a standard copy is performed.

The backup suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.
The version control method may be selected via the --backup option or through
the VERSION_CONTROL environment variable.  Here are the values:

none, off       never make backups (even if --backup is given)
numbered, t     make numbered backups
existing, nil   numbered if numbered backups exist, simple otherwise
simple, never   always make simple backups

As a special case, cp makes a backup of SOURCE when the force and backup
options are given and SOURCE and DEST are the same name for an existing,
regular file.

GNU coreutils online help: https://www.gnu.org/software/coreutils/
Full documentation https://www.gnu.org/software/coreutils/cp
or available locally via: info '(coreutils) cp invocation'
bandit12@bandit:/tmp$ cp -b
cp: missing file operand
Try 'cp --help' for more information.
bandit12@bandit:/tmp$ cp data.txt /tmp/tmp.7XMuNpn4zO
cp: cannot stat 'data.txt': No such file or directory
bandit12@bandit:/tmp$ cd
bandit12@bandit:~$ cp data.txt /tmp/tmp.7XMuNpn4zO
bandit12@bandit:~$ cd /tmp/tmp.7XMuNpn4zO
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
data.txt
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ mv data.txt data
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ xxd -r data > binary
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ mv binary binary.gz
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ gzip -d binary.gz
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ mv binary [binary.bz](http://binary.bz/)
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ bzip2 -d [binary.bz](http://binary.bz/)
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ file binary
binary: gzip compressed data, was "data4.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ tar -xf binary
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data  data5.bin
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ tar -xf data5.bin
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data  data5.bin  data6.bin
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ mv data6.bin [data6.bz](http://data6.bz/)
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ bzip2 -d [data6.bz](http://data6.bz/)
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data  data5.bin  data6
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ tar -xf data6
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data  data5.bin  data6  data8.bin
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ mv data8.bin data8.gz
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ gzip -d data8.gz
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ ls
binary  data  data5.bin  data6  data8
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ file data8
data8: ASCII text
bandit12@bandit:/tmp/tmp.7XMuNpn4zO$ cat data8
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

#Level 13 → Level 14

bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private -p 2220 bandit14@localhost
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

!!! You are trying to log into this SSH server with a password on port 2220 from localhost.
!!! Connecting from localhost is blocked to conserve resources.
!!! Please log out and log in again.

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

bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

#Level 14 → Level 15

bandit14@bandit:~$ nc localhost -p 30000
usage: nc [-46CDdFhklNnrStUuvZz] [-I length] [-i interval] [-M ttl]
[-m minttl] [-O length] [-P proxy_username] [-p source_port]
[-q seconds] [-s sourceaddr] [-T keyword] [-V rtable] [-W recvlimit]
[-w timeout] [-X proxy_protocol] [-x proxy_address[:port]]
[destination] [port]
bandit14@bandit:~$ nc localhost 30000

Wrong! Please enter the correct current password.
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

#Level 15 → Level 16

## bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1

## Certificate chain
0 s:CN = SnakeOil
i:CN = SnakeOil
a:PKEY: rsaEncryption, 4096 (bit); sigalg: RSA-SHA256
v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun 8 03:59:50 2034 GMT

## Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN = SnakeOil
issuer=CN = SnakeOil

## No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits

## SSL handshake has read 2103 bytes and written 373 bytes
Verification error: self-signed certificate

## New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 4096 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)

---

Post-Handshake New Session Ticket arrived:
SSL-Session:
Protocol  : TLSv1.3
Cipher    : TLS_AES_256_GCM_SHA384
Session-ID: 0FF844F35872AAD953918A45A76EABD31AFF260394F865703496E4053517487D
Session-ID-ctx:
Resumption PSK: AB07F1B42126FDE20D9A9DD86CF33D71EA34A5CD6A563833E3C64059686243A0148E709E15201466EF304703872D2375
PSK identity: None
PSK identity hint: None
SRP username: None
TLS session ticket lifetime hint: 300 (seconds)
TLS session ticket:
0000 - c0 c6 3d 9e 22 a9 6f a8-d6 08 ea 57 e8 ec 3e f7   ..=.".o....W..>.
0010 - b0 3b 55 7b af a7 8c 09-2f b2 fe 03 4a db fd 5a   .;U{..../...J..Z
0020 - e1 13 0b 92 32 6f 96 82-0f da f4 71 74 ce d8 fe   ....2o.....qt...
0030 - 4a 7a 2e 42 68 8b f2 fe-dc 71 2a 26 22 65 df da   [Jz.Bh](http://jz.bh/)....q*&"e..
0040 - c9 ae 8c b1 80 2a 81 c0-36 c3 a2 2a 40 59 77 f9   .....*..6..*@Yw.
0050 - ea bd 6b a2 bf 49 27 03-d6 45 d4 3a e3 f4 44 e0   ..k..I'..E.:..D.
0060 - 70 aa 09 f9 1d b5 a0 b7-16 22 df 73 36 fe 06 93   p........".s6...
0070 - c0 af 5c c2 c9 24 0d 62-6a ce 1a 12 3a 9b da 60   ..\..$.bj...:..     `0080 - d3 e6 b9 bb b3 e9 5e 07-bf 11 0e b2 31 81 82 ce   ......^.....1...     0090 - f2 28 cc 92 cf 86 7d cd-8b d2 e0 c5 09 02 6d 48   .(....}.......mH     00a0 - 30 bb e6 e7 b5 b0 34 e9-a8 63 bf 2e 5f 62 3e 76   0.....4..c.._b>v     00b0 - d6 89 5e 2a 8d 50 34 26-0c 1c f7 bb b9 95 63 83   ..^*.P4&......c.     00c0 - a7 2d 02 09 91 bb 6f 36-2b 3c 6b 9d f9 2d 19 be   .-....o6+<k..-..     00d0 - 79 94 91 60 d5 3e e6 87-98 66 77 04 9e c7 0b 74   y..`.>...fw....t

```
Start Time: 1729490309
Timeout   : 7200 (sec)
Verify return code: 18 (self-signed certificate)
Extended master secret: no
Max Early Data: 0

```

---

## read R BLOCK

Post-Handshake New Session Ticket arrived:
SSL-Session:
Protocol  : TLSv1.3
Cipher    : TLS_AES_256_GCM_SHA384
Session-ID: 0CBDC48073EA38F0549FE53964C118849CB1950D3F449683EE1FB002D7DD73E7
Session-ID-ctx:
Resumption PSK: 7EDE1177F908D7E5DC08F7511C7E4FEB55A6B53D6EEA1F46A575FC8B621EB88DF9B26854D88CAF9969779C69423CC401
PSK identity: None
PSK identity hint: None
SRP username: None
TLS session ticket lifetime hint: 300 (seconds)
TLS session ticket:
0000 - c0 c6 3d 9e 22 a9 6f a8-d6 08 ea 57 e8 ec 3e f7   ..=.".o....W..>.
0010 - c5 8f 93 0b 79 1f 63 94-5b af 4a fe 15 9f 63 26   ....y.c.[.J...c&
0020 - 5b 8d d8 62 87 2b 40 ba-95 f8 29 85 a6 ab 9f 4b   [..b.+@...)....K
0030 - 5d 1d 9a 7e 7c ee 0e 84-5f 58 32 7e ed c8 5f 6c   ]..~|..._X2~..*l
0040 - d7 94 8e 39 58 41 b9 b3-e7 35 8e ed 1a 70 b7 a9   ...9XA...5...p..
0050 - 7e b1 11 ba 1e 39 b2 fe-9d 47 67 1b df 59 81 52   ~....9...Gg..Y.R
0060 - 2b a2 ae 5e c8 d4 f7 86-ee 18 e1 7c a5 f9 d5 1d   +..^.......|....
0070 - 73 f0 89 76 f3 24 d1 2a-82 fd c9 5e fb e4 80 94   s..v.$.*...^....
0080 - 8a a7 06 4c 7f 58 04 1e-97 1e 6d fc b5 2e e6 35   ...L.X....m....5
0090 - 87 73 40 57 27 43 b6 42-98 ab 2a 2a 8e 37 ef 37   .s@W'C.B..**.7.7
00a0 - a5 35 39 7c 06 30 42 87-e6 ca b8 28 09 fc be 5f   .59|.0B....(...*
00b0 - 32 8e fa 7a 02 99 1e 9f-8d d0 10 af c2 18 76 2d   2..z..........v-
00c0 - d3 55 b6 38 66 80 2f 0c-7d 90 3d 14 71 49 c1 22   .U.8f./.}.=.qI."
00d0 - e4 74 fe a3 53 bf 88 0a-77 5c c7 1b f1 be 4c ee   .t..S...w\....L.

```
Start Time: 1729490309
Timeout   : 7200 (sec)
Verify return code: 18 (self-signed certificate)
Extended master secret: no
Max Early Data: 0

```

---

read R BLOCK
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

#Level16 → Level 17

root@DESKTOP-DCDALLM:~# ssh -i priv.key bandit17@localhost -p 2220
Warning: Identity file priv.key not accessible: No such file or directory.
ssh: connect to host localhost port 2220: Connection refused
root@DESKTOP-DCDALLM:~# ssh [bandit16@bandit.labs.overthewire.org](mailto:bandit16@bandit.labs.overthewire.org) -p 2220
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

[bandit16@bandit.labs.overthewire.org](mailto:bandit16@bandit.labs.overthewire.org)'s password:

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

bandit16@bandit:~$ cd /tmp/rand_ssh
bandit16@bandit:/tmp/rand_ssh$ ls -l
total 4
-r-------- 1 bandit16 bandit16 1613 Oct 21 17:28 priv.key
bandit16@bandit:/tmp/rand_ssh$ ssh -i priv.key bandit17@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit16/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit16/.ssh/known_hosts).
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

!!! You are trying to log into this SSH server with a password on port 2220 from localhost.
!!! Connecting from localhost is blocked to conserve resources.
!!! Please log out and log in again.

Load key "priv.key": error in libcrypto
bandit17@localhost: Permission denied (publickey).
bandit16@bandit:/tmp/rand_ssh$ vim private.key
bandit16@bandit:/tmp/rand_ssh$ vim private.key
bandit16@bandit:/tmp/rand_ssh$ ls -l
total 8
-rw-rw-r-- 1 bandit16 bandit16 1666 Oct 21 17:41 private.key
-r-------- 1 bandit16 bandit16 1613 Oct 21 17:28 priv.key
bandit16@bandit:/tmp/rand_ssh$ chmod u=r
chmod: missing operand after ‘u=r’
Try 'chmod --help' for more information.
bandit16@bandit:/tmp/rand_ssh$ chmod u=r private.key
bandit16@bandit:/tmp/rand_ssh$ chmod g-rw private.key
bandit16@bandit:/tmp/rand_ssh$ chmod o-r private.key
bandit16@bandit:/tmp/rand_ssh$ ls -l
total 8
-r-------- 1 bandit16 bandit16 1666 Oct 21 17:41 private.key
-r-------- 1 bandit16 bandit16 1613 Oct 21 17:28 priv.key
bandit16@bandit:/tmp/rand_ssh$ ssh -i private.key bandit17@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit16/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit16/.ssh/known_hosts).
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

!!! You are trying to log into this SSH server with a password on port 2220 from localhost.
!!! Connecting from localhost is blocked to conserve resources.
!!! Please log out and log in again.

Load key "private.key": error in libcrypto
bandit17@localhost: Permission denied (publickey).
bandit16@bandit:/tmp/rand_ssh$ client_loop: send disconnect: Connection reset by peer
root@DESKTOP-DCDALLM:~#
root@DESKTOP-DCDALLM:~#
root@DESKTOP-DCDALLM:~# ssh [bandit16@bandit.labs.overthewire.org](mailto:bandit16@bandit.labs.overthewire.org) -p 2220
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

[bandit16@bandit.labs.overthewire.org](mailto:bandit16@bandit.labs.overthewire.org)'s password:

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

bandit16@bandit:~$ cd /tmp/rand_ssh
bandit16@bandit:/tmp/rand_ssh$ ls -l
total 8
-r-------- 1 bandit16 bandit16 1666 Oct 21 17:41 private.key
-r-------- 1 bandit16 bandit16 1613 Oct 21 17:28 priv.key
bandit16@bandit:/tmp/rand_ssh$ vim private.key
bandit16@bandit:/tmp/rand_ssh$ ls -l
total 8
-r-------- 1 bandit16 bandit16 1613 Oct 21 18:16 private.key
-r-------- 1 bandit16 bandit16 1613 Oct 21 17:28 priv.key
bandit16@bandit:/tmp/rand_ssh$ ssh -i private.key bandit17@localhost -p 2220
kex_exchange_identification: read: Connection reset by peer
Connection reset by 127.0.0.1 port 2220
bandit16@bandit:/tmp/rand_ssh$ ssh -i private.key bandit17@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit16/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit16/.ssh/known_hosts).
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

!!! You are trying to log into this SSH server with a password on port 2220 from localhost.
!!! Connecting from localhost is blocked to conserve resources.
!!! Please log out and log in again.

Load key "private.key": error in libcrypto
bandit17@localhost: Permission denied (publickey).
bandit16@bandit:/tmp/rand_ssh$ cd/tmp
-bash: cd/tmp: No such file or directory
bandit16@bandit:/tmp/rand_ssh$ cd
bandit16@bandit:~$ cd /tmp
bandit16@bandit:/tmp$ ssh -i private.key bandit17@localhost -p 2220

#Level17 → Level 18

## bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< ktfgBvpMzWKR5ENj26IbLGSblgUG9CzB

> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
bandit17@bandit:~$ exit
> 

#Level18 → Level 19

root@DESKTOP-DCDALLM:~# cat /etc/shells

# /etc/shells: valid login shells

/bin/sh
/bin/bash
/usr/bin/bash
/bin/rbash
/usr/bin/rbash
/usr/bin/sh
/bin/dash
/usr/bin/dash
/usr/bin/tmux
/usr/bin/screen
root@DESKTOP-DCDALLM:~# ssh [bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org) -p 2220 -t "/bin/sh"
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

[bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org)'s password:

$
$
$ x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
/bin/sh: 3: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO: Permission denied
$
$ exit
Connection to [bandit.labs.overthewire.org](http://bandit.labs.overthewire.org/) closed.
root@DESKTOP-DCDALLM:~# ssh [bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org) -p 2220 -t "/bin/sh"
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

[bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org)'s password:
$
$ ls
readme
$ cat readme
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

#Level19 → Level 20

bandit19@bandit:~$ ls
bandit20-do
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
Example: ./bandit20-do id
bandit19@bandit:~$ ./bandit20-do ls /etc/bandit_pass
bandit0  bandit10  bandit12  bandit14  bandit16  bandit18  bandit2   bandit21  bandit23  bandit25  bandit27  bandit29  bandit30  bandit32  bandit4  bandit6  bandit8
bandit1  bandit11  bandit13  bandit15  bandit17  bandit19  bandit20  bandit22  bandit24  bandit26  bandit28  bandit3   bandit31  bandit33  bandit5  bandit7  bandit9
bandit19@bandit:~$ ./bandit20-do ls /etc/bandit_pass/bandit20
/etc/bandit_pass/bandit20
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
bandit19@bandit:~$ exit
logout
Connection to [bandit.labs.overthewire.org](http://bandit.labs.overthewire.org/) closed.
root@DESKTOP-DCDALLM:~# ssh [bandit20@bandit.labs.overthewire.org](mailto:bandit20@bandit.labs.overthewire.org) -p 2220
_                     _ _ _
| |__   __ _ _ __   *| () |
| ' \ /  `| '_ \\ / _` | | __|
| |) | (| | | | | (| | | |*
|*.**/ \**,*|*| |*|\**,*|*|\**|

```
                  This is an OverTheWire game server.
        More information on <http://www.overthewire.org/wargames>

```

[bandit20@bandit.labs.overthewire.org](mailto:bandit20@bandit.labs.overthewire.org)'s password:

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

