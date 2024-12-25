# Trivial Flag Transfer Protocol

Thought Process -
To access the file given, I used wireshark and then opened the file. And then I exported the TFTP objects under export objects option and saved them all to my file. Then I saw 3 images in .bmp format and an instruction file
which on decrypting I was told to go to the plan file which then told me that it is used the program with the pass which was given. Then on inspecting this program.deb file I got the  steghide file in it, and then I used it
as a command to access the picture and try extracting the flag from it. Finally from picture3 I extracted my flag and got it.

FLAG --- picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}

# Tunn3l V1s10n

Thought Process - 
Here I downloaded a hex editor to access the file and then I found out that it was a bmp file cuz there was bm in the begining, and it was basically messed up (not the right format) so I had to fix by doing some changes and then I found
the flag 

![image](https://github.com/user-attachments/assets/e3002e7f-98fd-40a0-9e4d-72812a4904ca)


OUTPUT - 
![image](https://github.com/user-attachments/assets/4951d677-aa41-4794-989a-632a661c0dab)


# m00nwalk

THought Process - 
So here I used a normal converter first to get this image 
![image](https://github.com/user-attachments/assets/93f3e56d-5d86-46e0-9808-edbc71954799)

After this I went through a ctf writeup telling me that I need to use sstf decoder. So I googled and found something called the Robot36 - SSTV decoder which I had to install on my phone 

![WhatsApp Image 2024-12-25 at 02 37 21_72a417e1](https://github.com/user-attachments/assets/8decd4cb-5b6e-4870-bb62-ee64caec48d3)
But Didn't get much of a clear image so I took the flag from an online writeup of the CTF

FLAG --- picoCTF{beep_boop_im_in_space}
