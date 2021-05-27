### Hashing.
---

What a hash function does is takes in data and gives you a fingerprint. Cant be reversed. Practically goes from input to output but not the other way arond.
<br>

##### Hash functions in python.

> `$ import hashlib`
`$ help(hashlib)`

Hashlib is a common interface to many hash functions.
<br>

##### How to hash something?

Check the `hashing.py` script for an explanation on how to check hash of files.


> `$ msg= b'something'`
`$ hashlib.sha256(msg)`
`$ hashlib.sha256(msg).hexdigest()`

Crate a message in bytes _b'_ then pass the method `.sha256(msg)` to the hashlib and finally pass another method to `.hexgdigest()` to get a hexadecimal number. For each one of a new message you will get a different fingerprint.
<br>

##### Python scripts with hash

Check `hashing.py` for a complete script on comparing hashes.

`xxd filename`
creates a hex dump of a given file or standard input. It can also convert a hex dump back to its original binary form.
`xxd -b filename`
Does the same but encoded with zeros and ones.
<br>

##### Check a hash of a file using the command line

`sha256sum filename`
will also give us the hash of the file
<br>
