## 1. The PATH Variable 
We just have to remove the rm cmd from the PATH variable and run /challenge/run
FLAG --- pwn.college{kw2EVqlZSxtM3c69gs8XmqKiNOd.dZzNwUDLxYjN0czW}

CODE --- 
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{kw2EVqlZSxtM3c69gs8XmqKiNOd.dZzNwUDLxYjN0czW}

## 2. Setting PATH

FLAG ---pwn.college{wASu_cK2PE8yqLBgWYk4E2hwF72.dVzNyUDLxYjN0czW}

CODE ---
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{wASu_cK2PE8yqLBgWYk4E2hwF72.dVzNyUDLxYjN0czW}

## 3. Adding Commands

FLAG --- pwn.college{0Kf1t9pH1_UFe_Rs_I9OJ8A9n8P.dZzNyUDLxYjN0czW}

CODE ---
hacker@path~adding-commands:~$ find / -name cat
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.G9qthVCks5’: Permission denied
/usr/bin/cat
/usr/share/doc/zsh-common/examples/Functions/cat
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
/run/workspace/bin/cat
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
find: ‘/proc/311’: No such file or directory
/opt/busybox/busybox-1.33.2/testsuite/cat
/opt/busybox/busybox-1.33.2/_install/bin/cat
/opt/aflplusplus/nyx_mode/packer/linux_initramfs/rootTemplate/bin/cat
/nix/store/k71apxkm38m3g34k01sb6zhysi0y7gph-coreutils-9.5/bin/cat
/nix/store/hgcmc7ps7wr0sxnbc87g4ba970km2vy4-dojo-workspace-full/bin/cat
/nix/store/a18ji16bi5ws1zksk1jwrx8dir6rdbhi-dojo-workspace-full/bin/cat
/nix/store/h8k7v1w69b9fs60jkx59vkhpy6scwgap-dojo-workspace-full/bin/cat
/nix/store/vapa6rnwfvbm3srldx33nyy2ybz9iqpy-dojo-workspace-full/bin/cat
/nix/store/6sin45s97yp4cfdn3q74drsjd7f4cq1f-dojo-workspace-full/bin/cat
/nix/store/nlxcqrgiszbjqkq86qhnflrbrs4adaac-dojo-workspace-full/bin/cat
/nix/store/cakzg9vppcbxwq046nlbi6xmib3xx4ka-dojo-workspace-full/bin/cat
/nix/store/mjnsl8dps0vn3aaf9wpgk4n830x320a7-dojo-workspace-full/bin/cat
/nix/store/nsh8bjqlami5grymm2mv63plmncga7wk-dojo-workspace-full/bin/cat
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ PATH=~/
hacker@path~adding-commands:~$ chmod u+x win
bash: chmod: command not found
hacker@path~adding-commands:~$ cd /usr/bin
hacker@path~adding-commands:/usr/bin$ chmod u+x win
bash: chmod: command not found
hacker@path~adding-commands:/usr/bin$ /usr/bin/chmod u+x win
/usr/bin/chmod: cannot access 'win': No such file or directory
hacker@path~adding-commands:/usr/bin$ cd
hacker@path~adding-commands:~$ /usr/bin/chmod u+x win
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{0Kf1t9pH1_UFe_Rs_I9OJ8A9n8P.dZzNyUDLxYjN0czW}

## 4. Hijacking Command 

FLAG ---pwn.college{0sql6P4wv83TPZQvWM5qXgIv9Nh.ddzNyUDLxYjN0czW}

CODE ---
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod o+x rm
hacker@path~hijacking-commands:~$ PATH=~/
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{0sql6P4wv83TPZQvWM5qXgIv9Nh.ddzNyUDLxYjN0czW}
