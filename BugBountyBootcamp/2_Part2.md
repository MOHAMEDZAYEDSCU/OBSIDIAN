
## How internet works ??

- ![[Pasted image 20240724225746.png]]

- encryption of the data while be sent through http protocol
- web ports the logical gates of data
- session management

----

## Security features :

- base64 in http header
- Http request and response
- sessions and cookies

---
### Token-Based Authentication:
- system stores this info directly in a token instead of a server-side
- it use encryption or encoding to protect the token from forgery
- or you can use a token signature
	- ![[Pasted image 20240724233741.png]]
	- ![[Pasted image 20240724233753.png]]

- JWT -> java script object notation web token
	- very popular and secure, use base64url-encoded
	- it use signature, header and payload
		- signature -> validate the user hasn't modify the token
		- payload -> contain the user credentials
		- header -> identify the algorithm used to generate the signature

----

>[!caution]- CIA Meaning
> ![[0xEthical Hacking#Info Sec|CIA Meaning]]

----

>[!caution]- Final note on taking notes :
>- Organize your notes of the target because it may have very large scopes
>- you can spot a weird behaviors taht aren't exploitable ??
>	- you'll need to combine with other behavior in an attack later to make the vulnerability
>- always take a good notes about any new features, minor bugs ans suspicious endpoints that you find
>- Make a progress file of your hacking progress
>	- it will have the exploitable features, and sub-domain scanned