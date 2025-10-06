# h7 - February2025!

## Schneier 2015: Applied Cryptography:

### 2.3 One-Way Functions 
- It is easy to compute one-way functions, but they are also computationally difficult to invert.
- The analogy of a plate that was smashed into pieces illustrates how easy it is to go one way but how hard it is to go the other way.
- One-way means that no efficient way to invert the function is known.
- One-way functions could not be used directly to encrypt information because we would not be able to recover the original information.
- Trapdoor one-way functions have knowledge that is secret, which allows this function to be inverted, and that forms the basis of public key cryptography.

### 2.4 One-Way Hash Functions
- One-way hash functions are easy to compute but hard to invert.
- They take some input data, which can be of variable length and source an output called hash.
- The goal was simply to create a unique fingerprint that could also allow you to check data integrity without returning the original data.
- A good hash function should resist attacks finding two inputs with a matching hash value (a collision) or reversing the hash back to its input, while still displaying output that is uniformly distributed and appears random.


## a) Install Hashcat

I ran `sudo apt-get update` to update the packages lists for upgrades and packages and this brought in updates from different repositories, including the security and backports identified in the output.
<img width="632" height="577" alt="image" src="https://github.com/user-attachments/assets/02972000-8758-4fbb-8f2f-62d9d82bf58e" />

I ran `sudo apt-get -y install hashid hashcat wget`. System handled the dependencies while installing the packages. It also took care of installing other packages automatically.
<img width="1461" height="823" alt="image" src="https://github.com/user-attachments/assets/3842ddc0-816b-4c60-aad2-397c955bb446" />

By running `tar xf rockyou.txt.tar.gz`, I was able to extract the file `rockyou.txt`. Then, I typed `head rockyou.txt` to see the first few lines of the `rockyou.txt` file. In this file I was presented with list of passwords. 
<img width="1857" height="612" alt="image" src="https://github.com/user-attachments/assets/cfe3df2c-18bb-4583-843b-b5e5ad652510" />

I crack the hash `6b1b28b016dff46e6fa35684be6acc96`. I executed `hashcat -m 0 '6b1b28b016dff46e6fa35684be6acc96' rockyou.txt -o solved` which uses the MD5 hash type (mode 0) and dictionary attack (mode 0) for the dictionary `rockyou.txt`.
<img width="1555" height="637" alt="image" src="https://github.com/user-attachments/assets/38d2105a-f3d0-410a-a8c9-36787fdd5230" />

<img width="792" height="767" alt="image" src="https://github.com/user-attachments/assets/18911264-179f-409f-b17d-2fc4dff7568c" />

Hashcat completed the entire process quickly, cracking the hash and revealing the password to be `summer`.
<img width="406" height="53" alt="image" src="https://github.com/user-attachments/assets/e7860582-2065-4407-872c-e9babd6626cb" />



## b) Crack this hash

I used the hashid command to crack hash `d595b2086532422bbe654bc07ea030df`.
<img width="1916" height="1017" alt="image" src="https://github.com/user-attachments/assets/66ad73dc-79dd-4d2c-855c-43940247834b" />

I ran `hashcat -m 0 'd595b2086532422bbe654bc07ea030df' rockyou.txt -o solved` to crack the hash. However after taking couple of minutes, the process got aborted due to no password candidates received in stdin mode. I then noticed that I input the command incorrectly with having left out `rockyou.txt -o solved` from the command.
<img width="787" height="415" alt="image" src="https://github.com/user-attachments/assets/cb8883bf-7f55-4222-9764-281cb99c16d0" />

Once I ran the command correctly, it cracked the hash quickly and at the end using `cat solved`, it revealed the password as `disobey`.
<img width="1501" height="522" alt="image" src="https://github.com/user-attachments/assets/c040d060-d9a8-4699-bea4-9b7a02a79364" />

<img width="972" height="481" alt="image" src="https://github.com/user-attachments/assets/dda55561-f610-4d51-b6de-8e6f43bc9806" />



## Voluntary m) Compile John the Ripper, Jumbo version

I tried to run the command `sudo apt-get -y install micro bash-completion git build-essential libssl-dev zlib1g zlib1g-dev zlib-gst libbz2-1.0 libbz2-dev atool zip wget` as it was told in `Karvinen 2023`, however that command refused to work. I tried to fix it by removing `zlib-gst` from the command and that helped as it started to install.
<img width="1917" height="980" alt="image" src="https://github.com/user-attachments/assets/c95756b1-c6af-429a-a5fb-70369c6197ed" />

I downloaded John the Ripper, Jumbo version by Git cloning the whole project. I ran `git clone --depth=1 https://github.com/openwall/john.git` to do that
<img width="792" height="376" alt="image" src="https://github.com/user-attachments/assets/04e675a1-473a-41fc-9f94-42b72e984d2c" />

I went to the `john/src` directory using `cd john/src` and executed `./configure` to set up a build environment. Finally, I executed `make -s clean && make -sj4` to clean and build the source with 4 jobs running parallel.
<img width="816" height="696" alt="image" src="https://github.com/user-attachments/assets/5be8cdae-6278-41e2-9cee-fd59ad1d3ecf" />

<img width="415" height="763" alt="image" src="https://github.com/user-attachments/assets/d5fbf8cb-26d1-468c-bd91-cf9725e73485" />

I ran `wget https://TerokKarvinen.com/2023/crack-file-password-with-john/tero.zip` to download a ZIP file named `tero.zip`. I extracted the hash with `zip2john tero.zip > tero.zip.hash` and used `john tero.zip.hash` to crack the password. The process loaded 1 password hash `(PKZIP [32/64])`, and successfully cracked the password `butterfly`.
<img width="1858" height="557" alt="image" src="https://github.com/user-attachments/assets/a194273b-15ee-41c2-a6dc-c04a869af20a" />

I unzipped `tero.zip` with `unzip tero.zip`, creating a `secretFiles` directory, and confirmed the cracked password by checking `cat secretFiles/SECRET.md`, which revealed the secret content. It showed that the tutorial was completed.
<img width="1412" height="681" alt="image" src="https://github.com/user-attachments/assets/9e63b03a-fd84-4450-8e02-453118bfebdd" />


# Sources
- Karvinen 2022: Cracking Passwords with Hashcat - https://terokarvinen.com/2022/cracking-passwords-with-hashcat/
- Karvinen 2023: Crack File Password With John - https://terokarvinen.com/2023/crack-file-password-with-john/
- Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions
