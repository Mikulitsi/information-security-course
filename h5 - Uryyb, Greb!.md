# h5 - Uryyb, Greb!

## € Schneier 2015: Applied Cryptography: Chapter 1: Foundations
- The goals of cryptography are privacy, integrity, authentication, and non-repudiation.
- Plaintext means the original information or data in human-readable form.
- Ciphertext means the nonhuman-readable form of the output from applying a cryptographic algorithm to the original data.
- Algorithm means the mathematical method (cipher) for encrypting and decrypting the data.
- Key means the secret parameter (for example, number or string) that specifies how the algorithm operates.
- Cryptosystem means the algorithm, key, and key management processes.

## Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg
- The purpose of encryption is confidentiality. The purpose of signing is authenticity and integrity. Encryption and signing both rely on public/private key pairs.
- Each user first creates their own keypair, public key, which they share with others, and private key, which is considered secret.
- To export and import keys, users share their public keys via files of ASCII-armored text. Once the public key has been imported, it becomes available for encryption or verification.
- After importing a public key from a user, the user must establish trust by verifying and signing the public key of the other user.
- GNU Privacy Guard (gpg) is a specific implementation of PGP and is open-source. gpg is widely used, by example, in the development of the Linux kernel.

## a) Install OpenSSH server, connect to it using 'ssh' client
- I start with installing ssh with command sudo apt-get install ssh. After having installed ssh, I checked its status and that it is active.
<img width="1022" height="905" alt="image" src="https://github.com/user-attachments/assets/18728e78-b97e-4c5f-aba1-12d4d1350613" />

<img width="902" height="365" alt="image" src="https://github.com/user-attachments/assets/e558ee44-7d31-4174-82b5-e9e0c4eff0e1" />

- After having installed and checked the status of ssh, I started it with the command sudo systemctl start ssh and then connected to the localhost.
- In the end I checked again the status of ssh and whether it was active.
<img width="1230" height="785" alt="image" src="https://github.com/user-attachments/assets/207ad81c-1977-41d1-9917-aec804307df9" />

## b) Automate SSH connection using public keys
- Started with generating a public key for myself with the command ssh-keygen.
<img width="787" height="397" alt="image" src="https://github.com/user-attachments/assets/d98b4e27-464d-42dd-ac47-02e216431eb7" />

- I copied the public key and in the end ran ssh mikael@localhost.
<img width="1177" height="423" alt="image" src="https://github.com/user-attachments/assets/f322bb5c-8bd1-4c5f-af26-612f8a5326dd" />

## c) Password manager
- I'm going to use Pass - the standard unix password manager as my password manager. I install it with command sudo apt-get install pass.
<img width="1367" height="873" alt="image" src="https://github.com/user-attachments/assets/a66a5a1d-b0e1-493e-be45-03fa6ca1c984" />

- After running command gpg --gen-key it asks for a name and email. After you've done that it asks to input a passphrase.
<img width="801" height="602" alt="image" src="https://github.com/user-attachments/assets/c10635ab-fe37-4f67-b8cc-6f97a901f41f" />

- When typing your password, it shows the strength of your password. The fuller your bar is, the stronger it is.
<img width="390" height="302" alt="image" src="https://github.com/user-attachments/assets/dd3e5e5f-e04d-4ac5-b5fc-0c35d47a37bf" />

<img width="742" height="350" alt="image" src="https://github.com/user-attachments/assets/f7fbf3c3-c305-4527-a03c-543145de618c" />

- You have to run command pass init your-gpg-id to initiate a password store. After that you can use pass generate your-gpg-id (length of characters) to get a random generated password in the length that you want.
<img width="482" height="296" alt="image" src="https://github.com/user-attachments/assets/4b511663-041c-43fb-af44-a447ac63c32b" />

<img width="378" height="60" alt="image" src="https://github.com/user-attachments/assets/27273110-db3a-4cfd-a158-9e4f5076d969" />


## s) Alternative (ETAOIN)
HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG        
I presume DHHP://HIYWLMYCTAIA.OWG is a link and from which I can presume these letters:
-  D = H
-  H = T
-  P = P
-  O = C
-  W = O
-  G = M
        
Now the text is:          
THMT'B TT. KOU'YI ACR OSSTCTMJJK M COQINYIMLIY! MB KOU BII, BTMPJI BUNBTTUHTOA CTPHIYB CMA NI NYOLIA RTTH SYIEUIACK MAMJKBTB. BII KOU MT HTTP://TIYOLMYCTAIA.COM
              
Now I guess that KOU'YI means you're so now all the changed letters are:
-  D = H
-  H = T
-  P = P
-  O = C
-  W = O
-  G = M
-  K = Y
-  U = U
-  Y = R
-  I = E
            
I'd also have to guess now that THMT'B TT is THAT'S IT which would mean following changes from the original text:
- B = S
- D = H
- G = M
- H = T
- I = E
- K = Y
- M = A
- O = C
- P = P
- T = I
- U = U
- W = O
- Y = R

- HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG
- THAT'S IT. YOU'RE AOR OSSICIAJJY A COQENREALER! AS YOU SEE, SIMPJE SUNSTITUTIOA CIPHERS CAA NE NROLEA RITH SREEUEACY AAAJYSIS. SEE YOU AT HTTP://TEROLARCIAEA.COM

Still need to understand what these letters have to be changed to?
- A = ?
- R = ?
- S = ?
- J = ?
- Q = ?
- L = ?
- N = ?
- E = ?
- C = ?

Well firstly, I'd guess OSSICIAJJY is officially so that would reveal that S is F and J is L:
- HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG
- THAT'S IT. YOU'RE AOR OFFICIALLY A COQENREALER! AS YOU SEE, SIMPLE SUNSTITUTIOA CIPHERS CAA NE NROLEA RITH FREEUEACY AAALYSIS. SEE YOU AT HTTP://TEROLARCIAEA.COM

AAALYSIS must be Analysis and that would give A = N
- HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG
- THAT'S IT. YOU'RE NOR OFFICIALLY A COQENREALER! AS YOU SEE, SIMPLE SUNSTITUTION CIPHERS CAN NE NROLEN RITH FREEUENCY ANALYSIS. SEE YOU AT HTTP://TEROLARCIAEN.COM

Then I guess that NOR is NOW and FREEUENCY is FREQUENCY so R = W and E = Q
- HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG
- THAT'S IT. YOU'RE NOW OFFICIALLY A COQENREALER! AS YOU SEE, SIMPLE SUNSTITUTION CIPHERS CAN NE NROLEN WITH FREQUENCY ANALYSIS. SEE YOU AT HTTP://TEROLARCIAEN.COM

SUNSTITUTION must be SUBSTITUTION which would give letters N = B:
- HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG
- THAT'S IT. YOU'RE NOW OFFICIALLY A COQEBREALER! AS YOU SEE, SIMPLE SUBSTITUTION CIPHERS CAN BE BROLEN WITH FREQUENCY ANALYSIS. SEE YOU AT HTTP://TEROLARCIAEN.COM

I guess that COQEBREALER is CODEBREAKER and BROLEN is BROKEN. This would give letters:
- Q = D
- L = K

- HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG
- THAT'S IT. YOU'RE NOW OFFICIALLY A CODEBREAKER! AS YOU SEE, SIMPLE SUBSTITUTION CIPHERS CAN BE BROKEN WITH FREQUENCY ANALYSIS. SEE YOU AT HTTP://TEROKARCIAEN.COM

And now I'm ready to make the final guess about the whole text which would be:

- THAT'S IT. YOU'RE NOW OFFICIALLY A CODEBREAKER! AS YOU SEE, SIMPLE SUBSTITUTION CIPHERS CAN BE BROKEN WITH FREQUENCY ANALYSIS. SEE YOU AT HTTP://TEROKARVINEN.COM

## t) Voluntary bonus, easy

# Sources
- https://cyberpanel.net/blog/debian-enable-ssh
- https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys-on-debian-11
- https://wiki.debian.org/PasswordManagement
- https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec006
- https://www.passwordstore.org/
- https://ryan.himmelwright.net/post/setting-up-pass/
- https://terokarvinen.com/2023/pgp-encrypt-sign-verify/
- https://terokarvinen.com/information-security/
