!!! Titan is under heavy development and not officially available just yet. !!!

Titan - Command line password manager

Password management belongs to the command line, deep into the Unix heartland,
the shell. Titan is written in C.

Titan is simple, Titan is advanced, Titan is adaptable.

Encryption

Titan uses OpenSSL library to perform the encryption. AES encryption is used with 
256 bit keys. Password database is also protected from tampering by using
a keyed-hash message autentication code (HMAC). Unique, cryptographically 
random initialization vector is used during the encryption. New initialization
vector is generated each time the password database is encrypted.

For key derivation, PKCS5_PBKDF2_HMAC is used along with salt and 
SHA256 hash algoritm.

Password storage

Titan uses SQlite for storing the passwords. Database schema is simple and easy
to make compatible with other password managers.

Installation

For example, on Ubuntu:

git clone https://github.com/nrosvall/titan.git
sudo apt-get install libsqlite3-dev
sudo apt-get install libssl-dev
cd titan
make
sudo make install


