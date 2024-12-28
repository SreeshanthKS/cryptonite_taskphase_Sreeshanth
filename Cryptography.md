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

# miniRSA 

"Thought Process- 
I used an online RSA cipher decoder to find the flag by inputting the N,e,c values.
"

Flag---picoCTF{n33d_a_lArg3r_e_606ce004}

![image](https://github.com/user-attachments/assets/6584a9a7-9efd-489f-b0de-5db4d8cc7357)






# EXTRA(0) - Rotation

Thought Process - 
I took the given file, did wget to it in the terminal, and cat-ed out the details of the encrypted.txt.
Then on analyzing the given text, I saw that each letter was just 8 steps away from the actual one. So I went to an online ceaser cypher decoder and decoded the message for the flag.

FLAG --- 	picoCTF{r0tat1on_d3crypt3d_25d7c61b}

# EXTRA(1) - Substitution0

Thought Process- 
So here I again did wget to the given source and cat-ed out the details of message.txt and then I went online to look for a substitution cypher-decoder and decrypted the message to get the flag 

![image](https://github.com/user-attachments/assets/1f116421-c59d-4207-94bd-9cf325cc5977)

FLAG - PICOCTF{5UB5717U710N_3V0LU710N_03055505}

# EXTRA(2) - SUBSTITUTION1

Thought Process - 
I thought it was same as the last one tbh, but no, once I decoded it I got everything in caps and then I reduced the word PICO to pico and then I was still not getting the flag. Then I saw that there was 
a J instead of a Q in frequency, so I tried replacing that and I got the flag!!

FLAG --- picoCTF{FR3QU3NCY_4774CK5_4R3_C001_7AA384BC}

![image](https://github.com/user-attachments/assets/42a4b6d7-f698-4d80-af2b-5761f13b6d98)


# EXTRA(3) - SUBSTITUTION3 

Thought Process - 
It is the same as the last one, I just had to bring down PICO to pico

FLAG --- picoCTF{N6R4M_4N41Y515_15_73D10U5_42EA1770}

# EXTRA(4) - Morse-Code 

Thought Process - 
So, instead of using Audacity decoder, I went for another online decoder in Morsecode.world through which I got the message and converted everything to lowercase and put the underscore in the big gaps in between to get the flag part.

FLAG --- picoCTF{wh47_h47h_90d_w20u9h7}

# EXTRA(5) - Caesar

Thought Process - 
Basically, it's the same as doing a normal caesar cypher decoder using an online decoder called decoder.fr . I cat-ed out the txt document and I got the text to be deciphered.

FLAG --- picoCTF{crossingtherubiconzaqjsscr}



x![image](https://github.com/user-attachments/assets/7f75dafc-794a-4f44-bdd4-9e85b5c912cc)
