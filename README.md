# Generate-RSA-private-and-public-key-pairs-using-the-OpenSSL-and-Hashing
This is the repository created to show encryption,decryption,hashing methods in networking security.<br>
In this we use OpenSSL tool to show encryption and decryption of the file and also we shall work on hashing with SHA and md5.<br>

## OpenSSL
OpenSSL is a commercial-grade utility toolkit for Transport Layer Security (TLS) and Secure Sockets Layer (SSL) protocols. It’s also a general-purpose cryptography library. OpenSSL is licensed under an Apache-style license, which means that you’re free to get it and use it for commercial and non-commercial purposes (subject to some simple license conditions).

##### 1.Generating a private key<br>
A 2048-bit RSA private key, and take a look at it. To generate the key, enter this command into the terminal:<br>
<br>
<img src="encrypt-decrypt and sign-verify using openssl/images_enc_dec/private_key.JPG" width="800" height="400"><br>
The contents of the private key file should look like a large jumble of random characters.<br>
<br>
<img src="encrypt-decrypt and sign-verify using openssl/images_enc_dec/private_key_1.JPG" width="800" height="400"><br>
<br>
##### 2.To create a public key based on a private key, enter the command below<br>
 The public key in the same way that you viewed the private key. It should look like a bunch of random characters, like the private key<br>
<br>
<img src="encrypt-decrypt and sign-verify using openssl/images_enc_dec/public_key.JPG" width="800" height="400"><br>
##### 3.Encryption<br>
We shall create a file secret.txt that consists the content to be encrypted and shall store in secret.enc
<br>
<img src="encrypt-decrypt and sign-verify using openssl/images_enc_dec/secret_file.JPG" width="800" height="400"><br>
To encrypt the file using your public key.This creates the file "secret.enc", which is an encrypted version of "secret.txt".The encrypted file will now be ready to send to whoever holds the matching private key.<br>
<img src="encrypt-decrypt and sign-verify using openssl/images_enc_dec/encrypt_file.JPG" width="800" height="400"><br>
##### 4.Decryption<br>
We must use the private key to decrypt the message, since it was encrypted using the public key.To decrypt the file, this will print the contents of the decrypted file to the screen, which should match the contents of "secret.txt":
<img src="encrypt-decrypt and sign-verify using openssl/images_enc_dec/decrypt.JPG" width="800" height="400"><br>

## Hashing

We shall verify for two hashing programs named MD5 and SHA (SHA1 and SHA256).<br>
<br>

Md5sum is a hashing program that calculates and verifies 128-bit MD5 hashes. As with all hashing algorithms, theoretically, there's an unlimited number of files that will have any given MD5 hash. Md5sum is used to verify the integrity of files.<br>
<br>
Similarly, shasum is an encryption program that calculates and verifies SHA hashes. It's also commonly used to verify the integrity of files.<br>

### MD5

##### 1.Creating a text file containing some data creates a text file called "file.txt" with a single line of basic text in it.<br>
* Generate the MD5 sum for the file and store it<br>
* To print then content of the hashed data <br>
<br>
<img src="Hashing/images/md5.JPG" width="800" height="400"><br>

##### 2.Verifying a valid file<br>
* We can also verify that the hash is correct, and that the original file hasn't been tampered with since the sum was made.<br>
<br>
<img src="Hashing/images/md5_verify.JPG" width="800" height="400"><br>

##### 3.Verifying an invalid file <br>
* The security of this process by showing how even a single-character change to the file results in a different hash.<br>
* Create a copy of the text file, and insert a single space at the end of the file. <br>
* Then generate a new md5sum for the new file. <br>
* The resulting hash is identical to the hash for our original file.txt despite the filenames being different. This is because hashing only looks at the data, not the metadata of the file. <br>
* The data has been modified in the bad_file.txt .<br>
* To see how different the hash of the edited file is, generate a new hash.<br>
* For reference,the contents of the original sum were<br>
<br>
<img src="Hashing/images/bad_file.JPG" width="800" height="400"><br>

### SHA1

The same steps, but for SHA1 and SHA256 hashes using the shasum tool.<br>
SHA256 is more seccure than SHA1 .<br>

##### 1.To create the SHA1 sum and save it to a file and then the file is verified.<br>
<br>
<img src="Hashing/images/sha1.JPG" width="800" height="400"><br>

### SHA256 

Same tool can be used to create a SHA256 sum.<br>

##### 1.To create the SHA256sum <br>
*The "-a" flag specifies the algorithm to use, and defaults to SHA1 if nothing is specified.* <br>
* SHA256's increased security comes from it creating a longer hash that's harder to guess. <br>
* The contents of the file here are much longer than the SHA1 file .<br>
<br>
<img src="Hashing/images/sha_256.JPG" width="800" height="400"><br>





