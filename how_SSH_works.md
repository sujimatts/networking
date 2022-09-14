
## SSH
SSH servers can authenticate clients using two methods.

And the two popular ways are:

```Password-based``` - Password-based authentication is the default method used for authentication for OpenSSH installed clients. It is the most basic ssh authentication but not the most secure one.

```Key-based``` - Key-based authentication improves the system security even further by generating SSH key pairs, which proves to be a reliable and secure alternative.

## Types of Encryption
### Symmetric encryption - same key is used for both encryption/decryption
###  assymentric encryption 
  - seperate keys used for encryption/decryption
  - public/private key pairs
  - public key is used to encrypt and private key is used to decrypt [it canonly be decrypted using private key]

### Flow
  1. client sends SSH connect request along with public key
  2. Server verifies the public key [it exists or not. If not exists it is added to knows_hosts file]
  3. Server creates a new symemtric key and encrypts it with public key and send it back to client
  4. Client decrypts with private key and gets the symemtric key
  5. client sends back the symmetric key encrypted with server public key
  6. server verifies the symemtric key and if it matches secure conenction established (ssh tunnel)

Youtube: https://www.youtube.com/watch?v=y2SWzw9D4RA

### Passwordless login
READ: https://www.tecmint.com/ssh-passwordless-login-using-ssh-keygen-in-5-easy-steps/

 1. create ssh keys  ssh-keygen -t rsa
 2. Copy public keys to remote server .ssh/.authorized_keys
