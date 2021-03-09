# CyberSpaceKe The CSPKE CryptoFREE VAULT

We had an awesome CTF competition which was hosted by CyberSpaceKe that  was held at Afralti Conference & Guest House located in Nairobi Kenya. There were a number of challenges to tackle within the 12 hours that the CTF was live, although am going to cover on how I solved the crypto challange only on this writeup..

Firstly, we have to know how RSA works. A comprehensive description on how RSA works can be found here — https://en.wikipedia.org/wiki/RSA_(cryptosystem)

for this challenge we are provided with a .zip file

on extracting the crypto.zip, we get three files, a README.txt, setup.py and crypto.py

My first step was to read the content of the readme file but it did not explain much. It only explained the padding method used and how to install the dependencies and how to run the script XD

My next move was to run the setup.py "python3 setup.py install" that installs the packages needed for the challenge.

lets dive into the actual challenge ;p

running the crypto.py, we are provided with public key, private key and the encrypted flag.. "easy one" XD

we are provided, with the exponent, modulus and the secret(private key) which makes decrypting the flag even more easy

in RSA; m(message) = ( c ^ d ) % n

where C is the ciphertext in our case the ecrypted flag
d is the private key, the secret value that was provided from the script
n is the modulus

I decided to write a python code to decrypt the flag using the pow() method in python

m = pow(encryptedFlag, privateKey, modulus)..

on running the script, we get the flag;p
