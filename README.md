#### electronic_Digital_signature
##Implement an application for organizing an EDS (electronic digital signature) of a file, encrypting it and sending it to a correspondent by email. On the side of the correspondent, it is necessary to decrypt this file and check the EDS. This laboratory work is done in Python.


## The code generates an RSA key pair, signs a file using the private key, saves the public key to a file, encrypts a file using AES encryption, sends the encrypted file via email as an attachment, decrypts the encrypted file, verifies the digital signature of the decrypted file using the public key.

## To be more specific, the code performs the following operations:

# Generates an RSA key pair of size 2048 and public exponent 65537.
# Reads the contents of a file named "file_to_sign.txt".
# Computes a digital signature for the contents of the file using the private key, using PSS padding with SHA-256 hash.
# Saves the public key to a file named "public_key.pem".
# Reads the contents of a file named "file_to_encrypt.txt".
# Derives a 256-bit key from a passphrase "my_password" using PBKDF2 with HMAC-SHA256 and a random salt of length 16, using 100000 iterations.
# Generates a random initialization vector (IV) of length 16 for AES-CBC encryption.
# Encrypts the file using AES-CBC encryption with the derived key and IV.
# Saves the encrypted data to a file named "encrypted_file.bin".
# Sends an email with the encrypted file attached as a binary MIME application to the recipient email address, using Gmail's SMTP server on port 465 over SSL/TLS.
# Reads the contents of the encrypted file.
# Decrypts the encrypted data using AES-CBC decryption with the derived key and IV.
# Saves the decrypted data to a file named "decrypted_file.txt".
# Reads the public key from the file "public_key.pem".
# Reads the contents of the decrypted file.
# Verifies the digital signature of the decrypted file using the public key, using PSS padding with SHA-256 hash. If the digital signature is valid, it prints "Digital signature is valid". Otherwise, it prints "Digital signature is not valid".
