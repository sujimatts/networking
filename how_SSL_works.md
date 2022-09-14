HTTP(S) - HTTP over SSL

1. Browser send request to https://yahoo.com
2. Yahoo webserver send its public key along with SSL certificate
3. Browser validates the certificate (browsers has inbuilt list of CA public keys)
4. once verified, the certificate can be trusted
5. Lock key in the URL bar indicates that, certificate is valid and belongs to the Yahoo
6. Now browser creates one symmetric key(shared secret)
7. encrypt this key with yahoo public key and send it to yahoo
8. webserver uses private key to decrypt and gets the symmetric key
9. Now on all traffic are encrypted/decrypted with this symmetric key

Note: anyone can create websites and get a SSL certificate. All the sites with https are not legitimate

How to create SSL certificate
1. Generate Private key and CSR (Certificate Signing Request) ##openssl genrsa 
2. Submit the CSR to Your Certificate Authority
3. Use *.crt file and *.key file in webserver hosts configuration (OR certificate.pem and privatekey.pem)
