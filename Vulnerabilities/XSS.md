
>[!caution] What it is ?
>- an injection class vulnerability
>- allow you to put a malicious code on the website and when a user open it, it will be executed on his device. so it is attacking the client not the server.
>---
>- you are try to put a code to be executed when anyone view it so you put it in the server website and wait ...
>----
>- a lot of libraries prevent xss and other vulnerabilities but nothing is 100%


>[!tip]- How to find it ?
>- URL :
>	- query strings
>	- fragments -> part of the url
>---
>- Input fields :
>	- search boxes
>	- comment section
>	- login forms
>---
>- Cookies :
>	- session Cookies -> if isn't secure
>---
>- File Uploads :
>	- HTML Files -> that can be executed
>	- Image Metadata -> scripts hidden in image metadata that can be executed


---

>[!todo]- Types of XSS ?
>
>>[!caution]- Stored XSS :
>>>[!danger] Description :
>>>- The malicious script is permanently stored on the target server, such as in a database, a comment field, or in forum posts.
>>---
>>>[!caution]- How it work ?
>>>- The attacker injects malicious code, which is then stored by the application. When a victim later requests the affected page, the stored script is delivered as part of the response.
>>---
>>>[!caution]- Example :
>>>- An attacker posts a comment containing a script on a blog. Every user who views the comment will execute the script.
>---
>>[!caution]- Reflected XSS :
>>>[!danger] Description :
>>>- The malicious script is reflected (بيسمع) off a web server, such as in an error message, search result, or any other response that includes input data immediately.
>>---
>>>[!caution]- How it work ?
>>>- The attacker tricks the victim into making a request to the server with malicious script as part of the input (e.g., a crafted URL). The server reflects the input back to the user without proper sanitization
>>>- you just make the user do something with the crafted link you gave him because of the payload it contain and the server execute it.
>>---
>>>[!caution]- Example :
>>>- An attacker sends a malicious link to a victim. When the victim clicks the link, the server reflects the malicious script back, and the victim’s browser executes it.
>>>---
>>>- ![[Pasted image 20240726102016.png]]
>>>- ![[Pasted image 20240726102037.png]]
>---
>>[!caution]- DOM XSS :
>>>[!danger] Description :
>>>- The vulnerability exists in the client-side code rather than the server-side code. The attack is executed within the Document Object Model (DOM) of the web page.
>>---
>>>[!caution]- How it work ?
>>>- The attacker manipulates the DOM environment in the victim’s browser, causing the browser to execute malicious scripts. This often involves insecure JavaScript handling client-side inputs.
>>---
>>>[!caution]- Example :
>>>- An attacker manipulates the fragment identifier in the URL (e.g., `example.com/page#<script>...`). The ***client-side*** script processes this input insecurely, leading to execution of the malicious script.
>>>- 