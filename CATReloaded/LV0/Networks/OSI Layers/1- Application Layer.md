>[!faq]- What is it?
>- is the end user interface like:
>	- Browser and mail client.
>- it has 2 major protocols
>	- DNS
>	- HTTP.

## DNS Protocol:
[[Terminologies of Computer Science#Terminologies|DNS meaning]]
>[!faq]- How it work?
>- first, search in local domain for the IP Address.
>- if not found, it go to the DNS local server
>- then to internet root then top level domain server.
>- it search for the ip and give it to the DNS local server then to you
#### Domain structure:
- top level domain (.com, .edu, .gov).
- second level domain (google, yahoo, facebook)
- sub-domain (mail, login).
#### DNS Record types:
- in windows you have a tool named, nslookup -type={your flag with the domain name}.
- ![[Pasted image 20240412102940.png]]
## HTTP Protocol:

>[!faq]- What is it?
>- hyper text transfer protocol.
>- responsible for web traffic on world wide web.
>- operate on TCP (accuracy) 80.
>- **stateless** connection, mean when you login to website and exit it, it will not remember you and u should enter your data again.
>
>>[!tip]- Methods:
>>- used to retrieve data from website.
>>
>>>[!example]
>>>- GET -> Ask for data from the web server
>>>- Post -> Send data to the webserver.
>>>	- more secure than GET.
>>>	- submit the data to the server, not retrieve them
>
>>[!caution]- Status code:
>>- 200: success.
>>- 300: redirect.
>>- 400: not found, client errors
>>- 500: server errors

>[!danger]- Cookies:
>- the information send to the http header to make the website remembering you.

