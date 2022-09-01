[<=== Back](../README.md)

## [Intro to Password Hashing](https://auth0.com/blog/hashing-passwords-one-way-road-to-security/)
*by Dan Arias*

> The gist of authentication is to provide users with a set of credentials, such as username and password, and to verify that they provide the correct credentials whenever they want access to the application.

A simple way of storing usernames and passwords is to use a table in a database that maps a username with a password. However, storing passwords as *cleartext* is not secure - it is the equivalent of writing them down on a digital piece of paper.

Instead of storing passwords as cleartext, a much more secure approach is to use a hash function to encrypt passwords.

> It is easy and practical to compute the hash, but "difficult or impossible to re-generate the original input if only the hash value is known"

Performing a SHA-256 (Secure Hash Algorithm) function on the given password input transforms the random-size input into a fixed-size bit string.

Code Example: 
```
from hashlib import sha256
h = sha256()
h.update(b'python1990K00L')
hash = h.hexdigest()
print(hash)
```
hashed output: `d1e8a70b5ccab1dc2f56bbf7e99f064a660c08e361a35751b9c483c88943d082`

## [Why you should use BCrypt to hash passwords](https://danboterhoven.medium.com/why-you-should-use-bcrypt-to-hash-passwords-af330100b861)
*by Daniel Boterhoven*

Plaintext passwords are obviously a bad idea, but even hashed passwords, and salted hashed passwords can be hacked, given enough time.

> Using a Key Factor, BCrypt is able to adjust the cost of hashing. With Key Factor changes, the hash output can be influenced. In this way, BCrypt remains extremely resistant to hacks, especially a type of password cracking called *rainbow table*. 

Basically the Key Factor slows down the hash function, causing it to use more resources, thus making it more difficult to hack. 
The Key Factor is the number of iterations of the hashing algorithm that are performed for each password.

## [jBCrypt](https://www.mindrot.org/projects/jBCrypt/)

*jBCrypt* is a Java implementation of OpenBSD's Blowfish password hashing code.

jBCrypt API:
```
// Hash a password for the first time
String hashed = BCrypt.hashpw(password, BCrypt.gensalt());

// gensalt's log_rounds parameter determines the complexity
// the work factor is 2**log_rounds, and the default is 10
String hashed = BCrypt.hashpw(password, BCrypt.gensalt(12));

// Check that an unencrypted password matches one that has
// previously been hashed
if (BCrypt.checkpw(candidate, hashed))
	System.out.println("It matches");
else
	System.out.println("It does not match");
  ```
