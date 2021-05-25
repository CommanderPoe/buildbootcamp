### Bitcoin commands used.
---

#### Digital Signatures

`$ testnet signmessage [address] [message]`
Sign a message with a private key.

`$ testnet verifymessage [address] [encoded message] [message]`
verifymessage "address" "signature" “message”. Returns a boolean, if true we can say with certainty that the private key behind the inputed address  is the owner pk.

`$ testnet getnewaddress ‘’ [legacy, segwit … ]`
Returns a new Bitcoin address for receiving payments.

`$ testnet getnewaddress ‘’ [legacy, segwit … ]`
Returns a new Bitcoin address for receiving payments.



#### Checking digital signatures (gpg)

gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys 01EA5486DE18A882D4C2684590C8019E36C2E964
Import a public key

gpg --verify SHA256SUMS.asc
Import a public key


Digital Signatures with python

gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys 01EA5486DE18A882D4C2684590C8019E36C2E964
Import a public key