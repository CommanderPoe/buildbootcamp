### Digital Signatures.
---

#### Signing messages

`$ testnet signmessage [address] [message]`
Sign a message with a private key.

`$ testnet verifymessage [address] [encoded message] [message]`
verifymessage "address" "signature" “message”. Returns a boolean, if true we can say with certainty that the private key behind the inputed address  is the owner pk.

`$ testnet getnewaddress ‘’ [legacy, segwit … ]`
Returns a new Bitcoin address for receiving payments.

`$ testnet getnewaddress ‘’ [legacy, segwit … ]`
Returns a new Bitcoin address for receiving payments.
<br>

##### Checking digital signatures (gpg)

`gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys 01EA5486DE18A882D4C2684590C8019E36C2E964`
Import a public key

`gpg --verify SHA256SUMS.asc`
Import a public key
<br>

##### Digital Signatures with python ECSDA

_Using the python IDLE_.
For this part we are going to be using a library called **[website](https://ofek.dev/bit/index.html)**. Bit is Python’s fastest Bitcoin library and was designed from the beginning to feel intuitive, be effortless to use, and have readable source code. It is heavily inspired by Requests and Keras. 
>`$ pip install bit`
`$ key= bit.PrivateKey.Testnet()`

`$ bit.[Tab]`
`$ key.[Tab]`
to explore available commands within the library.

`$ key` creates a new key.

`$ key.sign('message'.encode())` to encode a message in bytes and sign it. Encoded messages will show a _b'_ in front

`$ key.verify(signature,data)` in bytes, to verify signed tx.

`$ sig2 = sig[:-1] + b'b'` to replace the last char of the key with encoded b... Changing the signature will brake if you try to verify a message you already signed with a different key.
<br>

> `$ key` 
`$ key.to_hex()` 
`$ f= open('file_name.txt', 'w')`
`$ f.write(key.to_hex())`
`$ f.close()`
`$ f= open('secrets.txt', 'r')`
`$ content= f.read()`
`$ key3= key.PrivateKeyTestnet.from_hex(contents)`
`$ key3`
`$ key.address`
`$ key.get_transactions()`

 Creates a new private key, converts it to hex (more readability for humans), creates a new txt file, write the pk inside, close the file to save changes and open the newly created file in read mode, save it to a new variable and pass it to a another variable using the class PrivateKey, finally out of that pk create an address and recevie coins to that address. Get the add on the explorer and if its already mined it will show the hashes.

