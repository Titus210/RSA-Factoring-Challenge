## 	RSA  Algorithm
***
###	Introduction
This is assymetric cryptography algorithm which works with two keys:
-	__ Public Key__: <br/>
This key is used for encryption and is well known.
-	__Private Key__: <br/>
This key is used for decryption and is only known to the user who owns the key. <br/>
###	Examples
1. Client computer sends data to server to request for a data.
2. Server encrypting data using clients key and sends encrypted data.
3. Client receives and decrypts data.
Public key consists of two numbers where one is multiple of two large prime numbers. Private key is derived from two large numbers any factorization of two numbers makes the private key compromised.<br/>
Encryption and decription depends on size of  key doubling , and tripling the number makes it increase exponentially hence secured.
### 	Implementation
Generation of Public key.
1.	Select two numbers i.e x =20 and y = 60 <br/>
	First part of key : z =  x * y = 1200
2.	Get an exponential  integer  and is not a factor of z <br/>
> 1 < e <Φ(z)  <br/>
Generating  private key: 
1. We calculate Φ(z):<br/>
	such that Φ(z) = (x-1)(y-1) so Φ(z) = 1121
2. Calculate private key j: <br/>
	j = (k * Φ(z) + 1 ) / e <br/> where k = 2 <br/>
	hence j = 2243
#### Encryption

