## GDB BabyStep 1

Thought Process - 
Here I first thought abouthow to debug the file, and I decided to go with the hint of using gdb debgguer. I installed it by using the command "apt install gdb". After this I got the file to debug to the prompt by 
doing wget which gets the mentioned file through it's address.
After that I ran gdb debugger0_a to use the debugger and then ran the command disassemble main to get all the details of the file and they I spotted to eax register next to which I had flag details.

FLAG --- picoCTF{549698}

CODE ---
root@DESKTOP-DCDALLM:~# wget https://artifacts.picoctf.net/c/512/debugger0_a
--2024-12-23 16:49:33--  https://artifacts.picoctf.net/c/512/debugger0_a
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:2241:ea00:16:5ec5:2840:93a1, 2600:9000:2241:5a00:16:5ec5:2840:93a1, 2600:9000:2241:9200:16:5ec5:2840:93a1, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|2600:9000:2241:ea00:16:5ec5:2840:93a1|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16472 (16K) [application/octet-stream]
Saving to: ‘debugger0_a’

debugger0_a                   100%[=================================================>]  16.09K  --.-KB/s    in 0.05s

2024-12-23 16:49:39 (342 KB/s) - ‘debugger0_a’ saved [16472/16472]

root@DESKTOP-DCDALLM:~# gdb debugger0_a
GNU gdb (Ubuntu 12.1-0ubuntu1~22.04.2) 12.1
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from debugger0_a...
(No debugging symbols found in debugger0_a)
(gdb) disassemble main
Dump of assembler code for function main:
   0x0000000000001129 <+0>:     endbr64
   0x000000000000112d <+4>:     push   %rbp
   0x000000000000112e <+5>:     mov    %rsp,%rbp
   0x0000000000001131 <+8>:     mov    %edi,-0x4(%rbp)
   0x0000000000001134 <+11>:    mov    %rsi,-0x10(%rbp)
   0x0000000000001138 <+15>:    mov    $0x86342,%eax
   0x000000000000113d <+20>:    pop    %rbp
   0x000000000000113e <+21>:    ret
End of assembler dump.
(gdb) disassemble main

## ARMssembly 1

FLAG --- picoCTF{00000D2A}

CODE ---

func:
        sub     sp, sp, #32
        str     w0, [sp, 12]
        mov     w0, 79
        str     w0, [sp, 16] ## (sp+16) = 79
        mov     w0, 7
        str     w0, [sp, 20] ## (sp+20) = 7
        mov     w0, 3
        str     w0, [sp, 24] ## (sp+24) = 3
        ldr     w0, [sp, 20] ## w0 =(sp+20)= 7
        ldr     w1, [sp, 16]## w1 = (sp+16) = 79
        lsl     w0, w1, w0  ## w0 = 79<<7 = 10112
        str     w0, [sp, 28] ##      (sp+28) = 10112
        ldr     w1, [sp, 28]## w1 = (sp+28) = 10112
        ldr     w0, [sp, 24] ## w0 = (sp+24) = 3
        sdiv    w0, w1, w0   ## w0= 10112//3= 3370
        str     w0, [sp, 28] ## (sp+28)=3370
        ldr     w1, [sp, 28] ## w1= (sp+28) = 3370
        ldr     w0, [sp, 12]## w0= x
        sub     w0, w1, w0  ## w0 = 3370-x
        str     w0, [sp, 28]
        ldr     w0, [sp, 28]
        add     sp, sp, 32

main:
        stp     x29, x30, [sp, -48]!
        add     x29, sp, 0
        str     w0, [x29, 28]
        str     x1, [x29, 16]
        ldr     x0, [x29, 16]
        add     x0, x0, 8
        ldr     x0, [x0]
        bl      atoi
        str     w0, [x29, 44]
        ldr     w0, [x29, 44]
        bl      func
        cmp     w0, 0
        bne     .L4
        adrp    x0, .LC0
        add     x0, x0, :lo12:.LC0
        bl      puts
        b       .L6


## VAULT DOOR 3

  Thought Process - 
  Here I opened the given java file and I just iterated through the loops and solved for the flag

  FLAG --- picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_1fb380}

  CODE ---
  char[] buffer = new char[32];
        int i;
        // jU5t_a_s1mpl3_an    
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        } 
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }   // 4 r m 4 u 1 b 8
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        } // an 4gr4m_4_u_1fb380  ---- now on joing the two halfs we get "jU5t_a_s1mpl3_an4gr4m_4_u_1fb380"
        String s = new String(buffer);
