## C3

FLAg --- picoCTF{adlibs}

Thought Process - 
Here I first wget the ciphertext and the convert.py file. So this convert.py basically converts a plain_text to a cipher_text. So I copied the details of to another .py and then changed the program to make it convert a 
cypher text to a plain text. Now on decyphering the given ciphertext I got another python program which I saved into a .py file and then ran it to get the flag details.

Code ---
root@DESKTOP-DCDALLM:~# wget https://artifacts.picoctf.net/c_titan/47/ciphertext
--2024-12-23 08:54:14--  https://artifacts.picoctf.net/c_titan/47/ciphertext
Resolving [artifacts.picoctf.net](http://artifacts.picoctf.net/) ([artifacts.picoctf.net](http://artifacts.picoctf.net/))... 2600:9000:2241:d400:16:5ec5:2840:93a1, 2600:9000:2241:8400:16:5ec5:2840:93a1, 2600:9000:2241:2000:16:5ec5:2840:93a1, ...
Connecting to [artifacts.picoctf.net](http://artifacts.picoctf.net/) ([artifacts.picoctf.net](http://artifacts.picoctf.net/))|2600:9000:2241:d400:16:5ec5:2840:93a1|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 237 [application/octet-stream]
Saving to: ‘ciphertext.1’

ciphertext.1                  100%[=================================================>]     237  --.-KB/s    in 0s

2024-12-23 08:54:16 (36.5 MB/s) - ‘ciphertext.1’ saved [237/237]

root@DESKTOP-DCDALLM:~# cat ciphertext
DLSeGAGDgBNJDQJDCFSFnRBIDjgHoDFCFtHDgJpiHtGDmMAQFnRBJKkBAsTMrsPSDDnEFCFtIbEDtDCIbFCFtHTJDKerFldbFObFCFtLBFkBAAAPFnRBJGEkerFlcPgKkImHnIlATJDKbTbFOkdNnsgbnJRMFnRBNAFkBAAAbrcbTKAkOgFpOgFpOpkBAAAAAAAiClFGIPFnRBaKliCgClFGtIBAAAAAAAOgGEkImHnIlroot@DESKTOP-DCDALLM:~# wget https://artifacts.picoctf.net/c_titan/47/convert.py
--2024-12-23 08:55:41--  https://artifacts.picoctf.net/c_titan/47/convert.py
Resolving [artifacts.picoctf.net](http://artifacts.picoctf.net/) ([artifacts.picoctf.net](http://artifacts.picoctf.net/))... 2600:9000:2241:ac00:16:5ec5:2840:93a1, 2600:9000:2241:2200:16:5ec5:2840:93a1, 2600:9000:2241:e800:16:5ec5:2840:93a1, ...
Connecting to [artifacts.picoctf.net](http://artifacts.picoctf.net/) ([artifacts.picoctf.net](http://artifacts.picoctf.net/))|2600:9000:2241:ac00:16:5ec5:2840:93a1|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 335 [application/octet-stream]
Saving to: ‘convert.py.1’

convert.py.1                  100%[=================================================>]     335  --.-KB/s    in 0s

2024-12-23 08:55:44 (10.5 MB/s) - ‘convert.py.1’ saved [335/335]

root@DESKTOP-DCDALLM:~# vi convert.py.1
root@DESKTOP-DCDALLM:~# cp convert.py.1 convert2.py.1
root@DESKTOP-DCDALLM:~# vi convert2.py.1
root@DESKTOP-DCDALLM:~# echo abcd | python3 convert.py.1
OBBBdroot@DESKTOP-DCDALLvi convert2.py.1
root@DESKTOP-DCDALLM:~# echo -n "OBBBd" | python3 convert2.py.1
abcd
root@DESKTOP-DCDALLM:~# cat ciphertext | python3 convert2.py.1
#asciiorder
#fortychars
#selfinput
#pythontwo

chars = ""
from fileinput import input
for line in input():
chars += line
b = 1 / 1

for i in range(len(chars)):
if i == b * b * b:
print chars[i] #prints
b += 1 / 1
root@DESKTOP-DCDALLM:~# cat ciphertext | python3 convert2.py.1 > [crypt.py](http://crypt.py/)
root@DESKTOP-DCDALLM:~# cat crypt.py | python2 crypt.py
a
d
l
i
b
s


## CUSTOM ENCRYPTION

FLAG --- picoCTF{custom_d2cr0pt6d_751a22dc}

Thought Process -

It's similar to the last one. Firstly I did wget to get the files and then in the custom_encryption.py file I created functions to decrypt by referring to the given encryption functions and reversed it
and then ran it by inputting the given cipher into the program to decrypt it and get the flag

CODE ---
root@DESKTOP-DCDALLM:~# cat enc_flag.1
a = 94
b = 29
cipher is: [260307, 491691, 491691, 2487378, 2516301, 0, 1966764, 1879995, 1995687, 1214766, 0, 2400609, 607383, 144615, 1966764, 0, 636306,
2487378, 28923, 1793226, 694152, 780921, 173538, 173538, 491691, 173538, 751998, 1475073, 925536, 1417227, 751998, 202461, 347076, 491691]
root@DESKTOP-DCDALLM:~# vi custom_encryption.py.1
root@DESKTOP-DCDALLM:~# python custom_encryption.py.1
a = 94
b = 29
plain is: picoCTF{custom_d2cr0pt6d_751a22dc}
