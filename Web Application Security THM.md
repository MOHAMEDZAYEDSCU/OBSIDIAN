## Intro:

- There are certain functions that you would expect to be able to do on the web App.
	-  ![[Pasted image 20240503005417.png]]


## Info about Some Types of Attacks:

>[!caution]- identification and authentication failure:
>- The online shop must confirm the user’s identity and authenticate them before they can use the system. However, this step is prone to different types of weaknesses. Example weaknesses include:
>
>	- Allowing the attacker to use brute force, i.e., try many passwords, usually using automated tools, to find valid login credentials.
>	- Allowing the user to choose a weak password. A weak password is usually easy to guess.
>	- Storing the users’ passwords in plain text. If the attacker manages to read the file containing the passwords, we don’t want them to be able to learn the stored password.

>[!caution]- Broken Access Control:
>- Access control ensures that each user can only access files (documents, images, etc.) related to their role or work.
>	- For example, you don’t want someone in the marketing department to access (read) the finance department’s documents. Example vulnerabilities related to access control include:
>---
>- Failing to apply `the principle of the least privilege` and giving users more access permissions than they need. For example, an online customer should be able to view the prices of the items, but they should not be able to change them.
>- Being able to view or modify someone else’s account by using its unique identifier. For example, you don’t want one bank client to be able to view the transactions of another client.
>- Being able to browse pages that require authentication (logging in) as an unauthenticated user. For example, we cannot let anyone view the webmail before logging in.
>---
>>[!tip]- IDOR:
>>- Insecure Direct Object Reference.
>>
>>>[!success] examples:
>>>-  Let’s say that the user has permission to access a photo named `IMG_1003.JPG`. We might guess that there are also `IMG_1002.JPG` and `IMG_1004.JPG`; however, the web application should not provide us with that image even if we figured out its name.
>>>---
>>>- Just providing the correct URL for a user or a product does not necessarily mean the user should be able to access that URL. For instance, consider the product page `https://store.tryhackme.thm/products/product?id=52`. We can expect this URL to provide details about product number `52`. In the database, items would be assigned numbers sequentially. The attacker would try other numbers such as `51` or `53` instead of `52`; this might reveal other retired or unreleased products if the web application is vulnerable.
>>
>>

>[!caution]- Injection:
>- vulnerability in the web application where the user can insert malicious code as part of their input

>[!caution]- Cryptographic Failure:
>- Cryptography focuses on the processes of encryption and decryption of data. Encryption scrambles cleartext into ciphertext.
>---
>- Sending sensitive data in clear text, for example, using HTTP instead of HTTPS. HTTP is the protocol used to access the web, while HTTPS is the secure version of HTTP. Others can read everything you send over HTTP, but not HTTPS.
>- Relying on a weak cryptographic algorithm. One old cryptographic algorithm is to shift each letter by one. For instance, “TRY HACK ME” becomes “USZ IBDL NF.” This cryptographic algorithm is trivial to break.
>- Using default or weak keys for cryptographic functions. It won’t be challenging to break the encryption that used `1234` as the secret key.

..