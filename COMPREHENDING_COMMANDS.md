## 1 CAT: NOT THE PET, BUT THE COMMAND 
This CAT function basically works like a read/readlines statement to read and paste whatever is in the file. The file will be passed as an argument to cat

Here we have to basically cat the info from the file named 'flag' to obtain the flag.

FLAG --- pwn.college{8gKSKrodbNw6nUIDJINh5nxqEVe.dFzN1QDLxYjN0czW}

CODE --
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
.
.
.
## 2.CATTNG ABSOLUTE PATHS 

Here we have basically cat into the path '/flag' to obtain the flag/

FLAG --- pwn.college{oT_FR6w28GB4Lk858IkFE3rpI4E.dlTM5QDLxYjN0czW}

CODE --- 
hacker@commands~catting-absolute-paths:~$cat /flag
.
.
.
## 3. MORE CATTING PRACTICE

Here we have to directly cat into the absolute path to get the flag.

FLAG --- pwn.college{UMYmncbntxWPngfCaXuYh8ioV1H.dBjM5QDLxYjN0czW}

CODE --- 
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /lib/jvm/java-1.11.0-openjdk-amd64/flag. Go cat it out **without** 
cding into that directory!
hacker@commands~more-catting-practice:~$ cat /lib/jvm/java-1.11.0-openjdk-amd64/flag
.
.
.
## 4. GREPPING FOR A NEEDLE IN A HAYSTACK

Grep is like cat but it can search and display the content we need 
grep 'item to search' /path/to/file

Now here we have to just grep the flag (which we know, always starts with pwn.college) from the path given and obtain the flag 

FLAG ---pwn.college{s1GHFIJVWCovcUMS12ablXJEZe-.ddTM4QDLxYjN0czW}

CODE --- 
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
.
.
.
## 5. LISTING FILES 

Here we learn how to list all the files present in a directory using the 'ls' command 
In this program we to ls into '/challenge' to see what we have to replace /run with and then run it to obtain the flag 

FLAG --- pwn.college{YDaGdxgt9rGMZD19ovgPodcSfxY.dhjM4QDLxYjN0czW}

CODE ---
hacker@commands~listing-files:~$ ls /challenge
28848-renamed-run-13877  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/28848-renamed-run-13877
.
.
.
## 6. TOUCHING FILES 

Here we will be creating files in a directory using the 'Touch' command 

In this prg we have to create two files 'pwn' and 'college' in the /tmp directory and then /challenge/run to obtain the flag 

FLAG --- pwn.college{8U-3mBtNVgMyVu2zx5nSGiqgr7T.dBzM4QDLxYjN0czW}

CODE --- 
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ ls
bin              tmp.G9qthVCks5              vscode-ipc-d387b74a-b2bc-4345-94da-8a344215fe18.sock
hsperfdata_root  vscode-git-cbbf121b4b.sock  vscode-ipc-e56b7f03-ac13-4c0f-bc48-55abfae2cfd1.sock
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college 
hacker@commands~touching-files:/tmp$ /challenge/run

## 7. REMOVE FILES 

As the title says we gonna be removing files from the directory using the 'rm' command 

In this prg we will be deleting the delete_me file and then running /challenge/check which checks whether the file has been deleted and then prints the flag

FLAG --- pwn.college{cLPQdy4H-mYH_-wWL0YwoDEQqQO.dZTOwUDLxYjN0czW}

CODE ---
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
.
.
.
## 8. HIDDEN FILES 
Lines starting with . character doesn't show up with ls by defualt, so to access them we have to run the command 'ls -a'

In this prg we will be finding the hidden dot-prepended file in / by using the ls -a command 

FLAG ---pwn.college{o_YI4GGZ50ywg6tW6CtErqAsx3-.dBTN4QDLxYjN0czW}

CODE ---
hacker@commands~hidden-files:~$ ls /
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.  ..  .dockerenv  .flag-80962177925134  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~hidden-files:/$ cat .dockerenv
hacker@commands~hidden-files:/$ cat.flag-80962177925134
bash: cat.flag-80962177925134: command not found
hacker@commands~hidden-files:/$ cat .flag-80962177925134

## 9. AN EPIC FILESYSTEM QUEST 

Here we will be using ls and cat to find clues and depending on what clues we move on forward (or not).

FLAG --- pwn.college{EO1kdsjPS7_wQW5THH6auI6X9qG.dljM4QDLxYjN0czW}

CODE ---
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
CLUE  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.  ..  .dockerenv  CLUE  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat CLUE
Congratulations, you found the clue!
The next clue is in: /opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt
hacker@commands~an-epic-filesystem-quest:/opt$ /angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models
bash: /angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ /angr-mangement/
bash: /angr-mangement/: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ /angr-mangement
bash: /angr-mangement: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ cd /angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models
bash: cd: /angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ cd /angr-mangement
bash: cd: /angr-mangement: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ 
hacker@commands~an-epic-filesystem-quest:/opt$ cat delayed
cat: delayed: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models
bash: cd: /angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models: No such file or directory
hacker@commands~an-epic-filesystem-quest:~$ cd /opt
hacker@commands~an-epic-filesystem-quest:/opt$ ls
aflplusplus      binaryninja  capstone  ghidra  kropr    linux    pwn.college  radare2  splitmind  virtiofsd
angr-management  busybox      gef       ida     libslub  pt-dump  pwndbg       rappel   tcpdump
hacker@commands~an-epic-filesystem-quest:/opt$ ls -a
.   aflplusplus      binaryninja  capstone  ghidra  kropr    linux    pwn.college  radare2  splitmind  virtiofsd
..  angr-management  busybox      gef       ida     libslub  pt-dump  pwndbg       rappel   tcpdump
hacker@commands~an-epic-filesystem-quest:/opt$ cat angr-management
cat: angr-management: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt$ cd/opt/angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models
bash: cd/opt/angr-mangement/_internal/jedi/third_party/django-stubs/django-stubs/db/models: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt$ /opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models
bash: /opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt$ ls -a
.   aflplusplus      binaryninja  capstone  ghidra  kropr    linux    pwn.college  radare2  splitmind  virtiofsd
..  angr-management  busybox      gef       ida     libslub  pt-dump  pwndbg       rappel   tcpdump
hacker@commands~an-epic-filesystem-quest:/opt$ cd /opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models
hacker@commands~an-epic-filesystem-quest:/opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models$ ls
INSIGHT       aggregates.pyi  constraints.pyi  enums.pyi        fields     indexes.pyi  manager.pyi  query.pyi        signals.pyi  utils.pyi
__init__.pyi  base.pyi        deletion.pyi     expressions.pyi  functions  lookups.pyi  options.pyi  query_utils.pyi  sql
hacker@commands~an-epic-filesystem-quest:/opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models$ cat INSIGHT
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/scribble-lib/scribble/sigplan/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/angr-management/_internal/jedi/third_party/django-stubs/django-stubs/db/models$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/share/racket/pkgs/scribble-lib/scribble/sigplan/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scribble-lib/scribble/sigplan/compiled$ ls
REVELATION  lang_rkt.dep  lang_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scribble-lib/scribble/sigplan/compiled$ cat REVELATION
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/config/hw/random

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scribble-lib/scribble/sigplan/compiled$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /opt/linux/linux-5.4/include/config/hw/random
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/hw/random$ ls
via.h  virtio.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/hw/random$ ls -a
.  ..  .INFO  via.h  virtio.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/hw/random$ cat .INFO
Tubular find!
The next clue is in: /usr/share/icons/Humanity/places/128
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/hw/random$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/share/icons/Humanity/places/128
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/128$ ls -a
.   SPOILER               desktop.svg          gnome-desktop-config.svg       gnome-fs-desktop.svg  user-bookmarks.svg
..  bookmark-missing.svg  gnome-ccdesktop.svg  gnome-fs-bookmark-missing.svg  other-desktop.svg     user-desktop.svg
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/128$ cat SPOILER
Lucky listing!
The next clue is in: /usr/lib/python3.9/distutils/command

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/128$ cd
hacker@commands~an-epic-filesystem-quest:~$ /usr/lib/python3.9/distutils/command
bash: /usr/lib/python3.9/distutils/command: Is a directory
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/lib/python3.9/distutils/command
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ ls -a
.      __init__.py    bdist_msi.py      build.py       build_py.py       clean.py          install.py           install_headers.py  register.py
..     bdist.py       bdist_rpm.py      build_clib.py  build_scripts.py  command_template  install_data.py      install_lib.py      sdist.py
TRACE  bdist_dumb.py  bdist_wininst.py  build_ext.py   check.py          config.py         install_egg_info.py  install_scripts.py  upload.py
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ cat TRACE
Tubular find!
The next clue is in: /opt/aflplusplus/nyx_mode/QEMU-Nyx/capstone_v4/suite/MC/ARM

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ ls /opt/aflplusplus/nyx_mode/QEMU-Nyx/capstone_v4/suite/MC/ARM
CUE-TRAPPED                        fp-armv8.s.cs                             neon-neg-encoding.s.cs         neont2-cmp-encoding.s.cs         simple-fp-encoding.s.cs
arm-aliases.s.cs                   idiv-thumb.s.cs                           neon-pairwise-encoding.s.cs    neont2-convert-encoding.s.cs     thumb-fp-armv8.s.cs
arm-arithmetic-aliases.s.cs        idiv.s.cs                                 neon-reciprocal-encoding.s.cs  neont2-dup-encoding.s.cs         thumb-hints.s.cs
arm-it-block.s.cs                  load-store-acquire-release-v8-thumb.s.cs  neon-reverse-encoding.s.cs     neont2-minmax-encoding.s.cs      thumb-neon-crypto.s.cs
arm-memory-instructions.s.cs       load-store-acquire-release-v8.s.cs        neon-satshift-encoding.s.cs    neont2-mov-encoding.s.cs         thumb-neon-v8.s.cs
arm-shift-encoding.s.cs            mode-switch.s.cs                          neon-shift-encoding.s.cs       neont2-mul-accum-encoding.s.cs   thumb-shift-encoding.s.cs
arm-thumb-trustzone.s.cs           neon-abs-encoding.s.cs                    neon-shiftaccum-encoding.s.cs  neont2-mul-encoding.s.cs         thumb.s.cs
arm-trustzone.s.cs                 neon-absdiff-encoding.s.cs                neon-shuffle-encoding.s.cs     neont2-neg-encoding.s.cs         thumb2-b.w-encodingT4.s.cs
arm_addrmode2.s.cs                 neon-add-encoding.s.cs                    neon-sub-encoding.s.cs         neont2-pairwise-encoding.s.cs    thumb2-branches.s.cs
arm_addrmode3.s.cs                 neon-bitcount-encoding.s.cs               neon-table-encoding.s.cs       neont2-reciprocal-encoding.s.cs  thumb2-mclass.s.cs
arm_instructions.s.cs              neon-bitwise-encoding.s.cs                neon-v8.s.cs                   neont2-reverse-encoding.s.cs     thumb2-narrow-dp.ll.cs
basic-arm-instructions-v8.s.cs     neon-cmp-encoding.s.cs                    neon-vld-encoding.s.cs         neont2-satshift-encoding.s.cs    thumb2-pldw.s.cs
basic-arm-instructions.s.cs        neon-convert-encoding.s.cs                neon-vst-encoding.s.cs         neont2-shift-encoding.s.cs       vfp4-thumb.s.cs
basic-thumb-instructions.s.cs      neon-crypto.s.cs                          neon-vswp.s.cs                 neont2-shiftaccum-encoding.s.cs  vfp4.s.cs
basic-thumb2-instructions-v8.s.cs  neon-dup-encoding.s.cs                    neont2-abs-encoding.s.cs       neont2-shuffle-encoding.s.cs     vpush-vpop-thumb.s.cs
basic-thumb2-instructions.s.cs     neon-minmax-encoding.s.cs                 neont2-absdiff-encoding.s.cs   neont2-sub-encoding.s.cs         vpush-vpop.s.cs
crc32-thumb.s.cs                   neon-mov-encoding.s.cs                    neont2-add-encoding.s.cs       neont2-table-encoding.s.cs
crc32.s.cs                         neon-mul-accum-encoding.s.cs              neont2-bitcount-encoding.s.cs  neont2-vld-encoding.s.cs
dot-req.s.cs                       neon-mul-encoding.s.cs                    neont2-bitwise-encoding.s.cs   neont2-vst-encoding.s.cs
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ cat CUE-TRAPPED
cat: CUE-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ ls /opt/aflplusplus/nyx_mode/QEMU-Nyx/capstone_v4/suite/MC/ARM/CUE-TRAPPED
/opt/aflplusplus/nyx_mode/QEMU-Nyx/capstone_v4/suite/MC/ARM/CUE-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ cat /opt/aflplusplus/nyx_mode/QEMU-Nyx/capstone_v4/suite/MC/ARM/CUE-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/scipy/constants

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.9/distutils/command$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/lib/python3/dist-packages/scipy/constants
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/constants$ ls -a
.  ..  .ALERT  __init__.py  __pycache__  codata.py  constants.py  tests
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/constants$ cat .ALERT
Tubular find!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl-base/unicore/lib/Vo
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/constants$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/lib/x86_64-linux-gnu/perl-base/unicore/lib/Vo
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl-base/unicore/lib/Vo$ ls -a
.  ..  NUGGET  R.pl  Tr.pl  Tu.pl  U.pl
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl-base/unicore/lib/Vo$ cat NUGGET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
.
.
.
.
.
## 10. MAKING DIRECTORIES

Till now we have been playing with pre-existing directories. Now we will make directories by using the command mkdir

In this program we will be creating the directory '/tmp/pwn' and then cd into and create a file college using the 'touch' cmd and then/challenge/run to obtain the flag

FLAG ---pwn.college{siOHvGHgRB3iwoEJtlrM1fUiFwP.dFzM4QDLxYjN0czW}

CODE  ---
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.G9qthVCks5  vscode-git-617e8a2853.sock  vscode-ipc-c981658f-6de3-4506-9772-38fef648546c.sock  vscode-ipc-cfa535aa-1ec2-42e2-b2e1-f15f94f68c5b.sock
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.G9qthVCks5  vscode-git-617e8a2853.sock  vscode-ipc-c981658f-6de3-4506-9772-38fef648546c.sock  vscode-ipc-cfa535aa-1ec2-42e2-b2e1-f15f94f68c5b.sock
hacker@commands~making-directories:/tmp$ cd /pwn
bash: cd: /pwn: No such file or directory
hacker@commands~making-directories:/tmp$ /pwn
bash: /pwn: No such file or directory
hacker@commands~making-directories:/tmp$ cd
hacker@commands~making-directories:~$ mkdir tmp
hacker@commands~making-directories:~$ /tmp
bash: /tmp: Is a directory
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.G9qthVCks5  vscode-git-617e8a2853.sock  vscode-ipc-c981658f-6de3-4506-9772-38fef648546c.sock  vscode-ipc-cfa535aa-1ec2-42e2-b2e1-f15f94f68c5b.sock
hacker@commands~making-directories:/tmp$ mkdir pwn
mkdir: cannot create directory ‘pwn’: File exists
hacker@commands~making-directories:/tmp$ /pwn
bash: /pwn: No such file or directory
hacker@commands~making-directories:/tmp$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls /tmp/pwn/college
/tmp/pwn/college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{siOHvGHgRB3iwoEJtlrM1fUiFwP.dFzM4QDLxYjN0czW}

.
.
.
## 11. FINDING FILES 

We use the 'find' cmd to search for files and if no argument is entered along with it... it prints all the files 
We can also use paths as arguments or even mention some conditions like find / -name hacker which prints specific files 

In this prg the flag is hidden on a random directory. It's still called flag so we can find it easily this time.

FLAG ---pwn.college{UgL6HR8DEy1zPuwRwQ_eQtfZy_x.dJzM4QDLxYjN0czW}


CODE ---

hacker@commands~finding-files:~$ find
.
./.dbus
./.dbus/session-bus
./.dbus/session-bus/924007f00738404793a6a7c3330a0265-0
./.profile
./.cache
./.cache/fontconfig
./.cache/fontconfig/111d16ad01ec7e96a1fc2ee34d740d2d-x86_64.cache-9
./.cache/fontconfig/3830d5c3ddfd5cd38a049b759396e72e-x86_64.cache-9
./.cache/fontconfig/CACHEDIR.TAG
./.cache/fontconfig/d589a48862398ed80a3d6066f4f56f4c-x86_64.cache-9
./.cache/fontconfig/de156ccd2eddbdc19d37a45b8b2aac9c-x86_64.cache-9
./.cache/fontconfig/91e6fd8df8eae133e8cc910311cd171d-x86_64.cache-9
./.cache/fontconfig/7ef2298fde41cc6eeb7af42e48b7d293-x86_64.cache-9
./.cache/fontconfig/573ec803664ed168555e0e8b6d0f0c7f-x86_64.cache-9
./.cache/fontconfig/d0972c3d32f097851eb916381fc38920-x86_64.cache-9
./.cache/fontconfig/4c599c202bc5c08e2d34565a40eac3b2-x86_64.cache-9
./.cache/fontconfig/c57959a16110560c8d0fcea73374aeeb-x86_64.cache-9
./.cache/sessions
./.local
./.local/share
./.local/share/code-server
./.local/share/code-server/heartbeat
./.local/share/code-server/CachedProfilesData
./.local/share/code-server/CachedProfilesData/__default__profile__
./.local/share/code-server/CachedProfilesData/__default__profile__/extensions.user.cache
./.local/share/code-server/CachedProfilesData/__default__profile__/extensions.builtin.cache
./.local/share/code-server/logs
./.local/share/code-server/logs/20241008T074022
./.local/share/code-server/logs/20241008T074022/ptyhost.log
./.local/share/code-server/logs/20241008T074022/network.log
./.local/share/code-server/logs/20241008T074022/remoteagent.log
./.local/share/code-server/logs/20241008T074022/exthost1
./.local/share/code-server/logs/20241008T074022/exthost1/vscode.git
./.local/share/code-server/logs/20241008T074022/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T074022/exthost1/vscode.github
./.local/share/code-server/logs/20241008T074022/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T074022/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241008T091125
./.local/share/code-server/logs/20241008T091125/ptyhost.log
./.local/share/code-server/logs/20241008T091125/network.log
./.local/share/code-server/logs/20241008T091125/remoteagent.log
./.local/share/code-server/logs/20241008T091125/exthost1
./.local/share/code-server/logs/20241008T091125/exthost1/vscode.git
./.local/share/code-server/logs/20241008T091125/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T091125/exthost1/vscode.github
./.local/share/code-server/logs/20241008T091125/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T091125/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241008T081813
./.local/share/code-server/logs/20241008T081813/ptyhost.log
./.local/share/code-server/logs/20241008T081813/network.log
./.local/share/code-server/logs/20241008T081813/remoteagent.log
./.local/share/code-server/logs/20241008T081813/exthost1
./.local/share/code-server/logs/20241008T081813/exthost1/vscode.git
./.local/share/code-server/logs/20241008T081813/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T081813/exthost1/vscode.github
./.local/share/code-server/logs/20241008T081813/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T081813/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241008T073811
./.local/share/code-server/logs/20241008T073811/ptyhost.log
./.local/share/code-server/logs/20241008T073811/network.log
./.local/share/code-server/logs/20241008T073811/remoteagent.log
./.local/share/code-server/logs/20241008T073811/exthost1
./.local/share/code-server/logs/20241008T073811/exthost1/vscode.git
./.local/share/code-server/logs/20241008T073811/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T073811/exthost1/vscode.github
./.local/share/code-server/logs/20241008T073811/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T073811/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241008T081554
./.local/share/code-server/logs/20241008T081554/ptyhost.log
./.local/share/code-server/logs/20241008T081554/network.log
./.local/share/code-server/logs/20241008T081554/remoteagent.log
./.local/share/code-server/logs/20241008T081554/exthost1
./.local/share/code-server/logs/20241008T081554/exthost1/vscode.git
./.local/share/code-server/logs/20241008T081554/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T081554/exthost1/vscode.github
./.local/share/code-server/logs/20241008T081554/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T081554/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241007T122621
./.local/share/code-server/logs/20241007T122621/ptyhost.log
./.local/share/code-server/logs/20241007T122621/network.log
./.local/share/code-server/logs/20241007T122621/remoteagent.log
./.local/share/code-server/logs/20241007T122621/exthost1
./.local/share/code-server/logs/20241007T122621/exthost1/vscode.git
./.local/share/code-server/logs/20241007T122621/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241007T122621/exthost1/vscode.github
./.local/share/code-server/logs/20241007T122621/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241007T122621/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241008T075300
./.local/share/code-server/logs/20241008T075300/ptyhost.log
./.local/share/code-server/logs/20241008T075300/network.log
./.local/share/code-server/logs/20241008T075300/remoteagent.log
./.local/share/code-server/logs/20241008T075300/exthost1
./.local/share/code-server/logs/20241008T075300/exthost1/vscode.git
./.local/share/code-server/logs/20241008T075300/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T075300/exthost1/vscode.github
./.local/share/code-server/logs/20241008T075300/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T075300/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241007T122159
./.local/share/code-server/logs/20241007T122159/ptyhost.log
./.local/share/code-server/logs/20241007T122159/network.log
./.local/share/code-server/logs/20241007T122159/remoteagent.log
./.local/share/code-server/logs/20241007T122159/exthost1
./.local/share/code-server/logs/20241007T122159/exthost1/vscode.git
./.local/share/code-server/logs/20241007T122159/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241007T122159/exthost1/vscode.github
./.local/share/code-server/logs/20241007T122159/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241007T122159/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241007T122435
./.local/share/code-server/logs/20241007T122435/ptyhost.log
./.local/share/code-server/logs/20241007T122435/network.log
./.local/share/code-server/logs/20241007T122435/remoteagent.log
./.local/share/code-server/logs/20241007T122435/exthost1
./.local/share/code-server/logs/20241007T122435/exthost1/vscode.git
./.local/share/code-server/logs/20241007T122435/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241007T122435/exthost1/vscode.github
./.local/share/code-server/logs/20241007T122435/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241007T122435/exthost1/remoteexthost.log
./.local/share/code-server/logs/20241008T084330
./.local/share/code-server/logs/20241008T084330/ptyhost.log
./.local/share/code-server/logs/20241008T084330/network.log
./.local/share/code-server/logs/20241008T084330/remoteagent.log
./.local/share/code-server/logs/20241008T084330/exthost1
./.local/share/code-server/logs/20241008T084330/exthost1/vscode.git
./.local/share/code-server/logs/20241008T084330/exthost1/vscode.git/Git.log
./.local/share/code-server/logs/20241008T084330/exthost1/vscode.github
./.local/share/code-server/logs/20241008T084330/exthost1/vscode.github/GitHub.log
./.local/share/code-server/logs/20241008T084330/exthost1/remoteexthost.log
./.local/share/code-server/code-server-ipc.sock
./.local/share/code-server/Machine
./.local/share/code-server/coder.json
./.local/share/code-server/coder-logs
./.local/share/code-server/coder-logs/code-server-stdout.log
./.local/share/code-server/coder-logs/code-server-stderr.log
./.local/share/code-server/User
./.local/share/code-server/User/globalStorage
./.local/share/code-server/User/globalStorage/storage.json
./.local/share/code-server/User/globalStorage/vscode.json-language-features
./.local/share/code-server/User/globalStorage/vscode.json-language-features/json-schema-cache
./.local/share/code-server/User/machineid
./.local/share/code-server/User/snippets
./.local/share/code-server/User/customBuiltinExtensionsCache.json
./.local/share/code-server/User/History
./.local/share/code-server/User/History/6d0e5537
./.local/share/code-server/User/History/6d0e5537/WK3E.json
./.local/share/code-server/User/History/6d0e5537/entries.json
./.local/share/code-server/User/settings.json
./.local/share/code-server/User/systemExtensionsCache.json
./Desktop
./.config
./.config/Thunar
./.config/Thunar/uca.xml
./.config/xfce4
./.config/xfce4/xfconf
./.config/xfce4/xfconf/xfce-perchannel-xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xsettings.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/thunar.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml
./.config/xfce4/desktop
./.config/xfce4/desktop/icons.screen0-1008x725.rc
./.config/xfce4/desktop/icons.screen.latest.rc
./.config/xfce4/desktop/icons.screen0-1247x533.rc
./.config/xfce4/xfwm4
./.config/xfce4/panel
./.config/xfce4/panel/launcher-18
./.config/xfce4/panel/launcher-18/17279678682.desktop
./.config/xfce4/panel/launcher-19
./.config/xfce4/panel/launcher-19/17279678683.desktop
./.config/xfce4/panel/launcher-20
./.config/xfce4/panel/launcher-20/17279678684.desktop
./.config/xfce4/panel/launcher-17
./.config/xfce4/panel/launcher-17/17279678671.desktop
./.config/code-server
./.config/code-server/config.yaml
./tmp
./.bash_history
./.bashrc
./.bash_logout
./.ICEauthority
hacker@commands~finding-files:~$ cd /
hacker@commands~finding-files:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~finding-files:/$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.G9qthVCks5’: Permission denied
/usr/local/share/radare2/5.9.5/flag
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/opt/aflplusplus/nyx_mode/libnyx/libnyx/target/release/build/standback-718add4b4ef4c593/out/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/opt/radare2/libr/flag
/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:/$ cd /opt/aflplusplus/nyx_mode/libnyx/libnyx/target/release/build/standback-718add4b4ef4c593/out/flag
bash: cd: /opt/aflplusplus/nyx_mode/libnyx/libnyx/target/release/build/standback-718add4b4ef4c593/out/flag: Not a directory
hacker@commands~finding-files:/$ /opt/aflplusplus/nyx_mode/libnyx/libnyx/target/release/build/standback-718add4b4ef4c593/out/flag
bash: /opt/aflplusplus/nyx_mode/libnyx/libnyx/target/release/build/standback-718add4b4ef4c593/out/flag: Permission denied
hacker@commands~finding-files:/$ /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
bash: /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:/$ cd /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag$ cat flag
cat: flag: No such file or directory
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag$ ls -a
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag$ cat flag.py
"""Describes a way to submit a key to a key server.
"""
from __future__ import absolute_import
from __future__ import division

import os

from pwnlib.args import args
from pwnlib.log import getLogger
from pwnlib.tubes.remote import remote

env_server  = args.get('FLAG_HOST', 'flag-submission-server').strip()
env_port    = args.get('FLAG_PORT', '31337').strip()
env_file    = args.get('FLAG_FILE', '/does/not/exist').strip()
env_exploit_name = args.get('EXPLOIT_NAME', 'unnamed-exploit').strip()
env_target_host  = args.get('TARGET_HOST', 'unknown-target').strip()
env_team_name    = args.get('TEAM_NAME', 'unknown-team').strip()

log = getLogger(__name__)

def submit_flag(flag,
                exploit=env_exploit_name,
                target=env_target_host,
                server=env_server,
                port=env_port,
                team=env_team_name):
    """
    Submits a flag to the game server

    Arguments:
        flag(str): The flag to submit.
        exploit(str): Exploit identifier, optional
        target(str): Target identifier, optional
        server(str): Flag server host name, optional
        port(int): Flag server port, optional
        team(str): Team identifier, optional

    Optional arguments are inferred from the environment,
    or omitted if none is set.

    Returns:
        A string indicating the status of the key submission,
        or an error code.

    Doctest:

        >>> l = listen()
        >>> _ = submit_flag('flag', server='localhost', port=l.lport)
        >>> c = l.wait_for_connection()
        >>> c.recvall().split()
        [b'flag', b'unnamed-exploit', b'unknown-target', b'unknown-team']
    """
    flag = flag.strip()

    log.success("Flag: %r" % flag)

    data = "\n".join([flag,
                      exploit,
                      target,
                      team,
                      '']).encode('ascii')

    if os.path.exists(env_file):
        write(env_file, data)
        return

    try:
        with remote(server, int(port)) as r:
            r.send(data)
            return r.recvall(timeout=1)
    except Exception:
        log.warn("Could not submit flag %r to %s:%s", flag, server, port)
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag$ cat /opt/aflplusplus/nyx_mode/libnyx/libnyx/target/release/build/standback-718add4b4ef4c593/out/flag
pwn.college{UgL6HR8DEy1zPuwRwQ_eQtfZy_x.dJzM4QDLxYjN0czW}
.
.
.
.
.
.
## 12. LINKING FILES 

 Here we will be working with symbolic links (symlinks). This kind of link is created by the command ln with -s as argument 
 It provides a link/connection between two files and the data of the original file would be stored in the linked file too

 Here, in this prg we will have to link /home/hacker/not-the-flag to /flag file and then run the /challenge/catflag

 FLAG --- pwn.college{I48cZ2zWVhUee39SHSQh51Lwtfy.dlTM1UDLxYjN0czW}

 CODE --- 
 hacker@commands~linking-files:~$ cat /challenge/flag 
cat: /challenge/flag: No such file or directory
hacker@commands~linking-files:~$ cat /challenge/catflag
#!/opt/pwn.college/bash

fold -s <<< "About to read out the /home/hacker/not-the-flag file!"
cat /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
ln: failed to create symbolic link '/home/hacker/not-the-flag': File exists
hacker@commands~linking-files:~$ rm /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{I48cZ2zWVhUee39SHSQh51Lwtfy.dlTM1UDLxYjN0czW}
