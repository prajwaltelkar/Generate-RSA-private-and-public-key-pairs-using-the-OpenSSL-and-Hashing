# Generate-RSA-private-and-public-key-pairs-using-the-OpenSSL-and-Hashing
This is the repository created to show encryption,decryption,hashing methods in networking security.<br>
In this we use OpenSSL tool to show encryption and decryption of the file and also we shall work on hashing with SHA and md5.<br>

### OpenSSL
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
