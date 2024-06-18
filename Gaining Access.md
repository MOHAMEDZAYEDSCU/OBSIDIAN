>[!caution]- About:
>- after the reconnaisance and scaning, now you need to use the information gained to try to access the target system.

---

>[!tip]- Identification and Authentication Techniques:
>
>- you can each individual or all together.
>---
>>[!caution]- Passwords:
>>- something you know
>
>>[!caution]- Biometric:
>>- something you are.
>
>>[!caution]- Token:
>>- something you have.

>[!Caution]- Passwords:
>- The most common technique
>- the weakest form of protection.
>---
>>[!todo]- Types:
>>- Static Password:
>>	- always remain the same
>>- Dynamic passwords:
>>	- changes after period of time.
>>- Cognitive Password:
>>	- some question about you
>>		- birth date
>>		- mother name
>>		- other personal info.
>---
>>[!success]- How to store Passwords:
>>- You hash the password Then store it in the database
>>- when try to login it use the username with the password then hash them and compare the value appear with the stored one.
>>- too strong and un-reversable.

>[!success]- Dictionary vs Brute Force
>- Dicionary:
>	- it test the passwords you provided.
>- Brute force:
>	- it test all possible combination without giving it any test cases.

>[!tip]- Pre-Computation Attacks Countermeasures:
>- by hashing but with adding salt to the password before the hashing as an addition layer of protection.
>- even if you know the hashing key, you still can't generate the hashed password duo to the lack of the salt added to the password.
>---
>>[!Danger]- Increase Password Security:
>>- first you can't make it:
>>	- your name
>>	- any personal information(birth date, phone number,...)
>>- make it has small, capital and special characters along with number if possible.
>>- try to crack your passwords with tools, testing the security of you passwords.
>>---
>>- if there are very important account, try to change password frequently to increase security.

>[!caution]- Tools:

---

>[!quote]- Biometric:
>- With something you have, like:
>	- finger print
>	- eye id
>	- face id
>---
>- Careful:
>	- it has some errors like:
>		- face id with the your twin brother or unknown person could access it.
>		- finger print, suddenly you can't access with your finger print. maybe sweat or injury ...

---

>[!Danger]- Tokens:
>- Something you have
>- a hardware that help you with the authentication.
>---
>>[!todo]- Drawbacks:
>>- your hardware device can be :
>>	- stolen
>>	- missed
>>	- broken
>>	- battery die.
>>- so be careful while using it.








