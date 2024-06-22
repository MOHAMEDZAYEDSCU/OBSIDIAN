>[!caution]- About:
>- a form that allow to show the apps development stages and changes.
>---
>- Version Control :
>	- control the development process of your files.
>	- if there are multiple users work on the same files, it allow you to review the code first then merge it.
>---
>- Git by "linus travers" :
>	- the linux founder.
>---
>>[!tip]- Has 3 Types :
>>>[!caution]- Local Version Control :
>>>- your own version inside your local machine.
>>>- just for you and do whatever you want.
>>---
>>>[!todo]- Central Version Control :
>>>- Active modification for online source code or server source code
>>>- you don't has a copy of files, you work direct on the original file.
>>>- need an active communication
>>>	- maybe inside the company if the system belong to it.
>>---
>>>[!quote]- Distributed Version Control :
>>>- you download or clone copy of the system files to you local system.
>>>- if there are modification on the system files or any mistakes on your local files, it doesn't affect the original data.
>>>- allow you to modify the original files by only the modification needed not all the file.
>>>- use :
>>>	- push and pull requests.
>>>- like Central version control but with your desires.
>>>	- you control who will access the files and modify them.

---

>[!tip]- How it Work :
>>[!caution]- Tracking Versions? :
>>>[!todo]- In Past :
>>>- in the beginning, the control version take a snap shot of your project.
>>>- by adding any modification, it just take the new line.
>>>	- the difference between the original and modified one.
>>>---
>>>>[!quote] now if you want to run a old version ? v5 for example ..
>>>>- you will run the the first version until you reach the required version.
>>>>	- build the system step by step, incremental.
>>---
>>>[!danger]- Current Git :
>>>- Take a snap shot of all the modified file and store it
>>>	- even if it just a character, it will take the whole file !!!!!!!!!!

---

>[!todo]- Git Architecture :
>- Git Repository = Version control
>	- because it allow you to track all version of the app or system being developed.
>	- One Repo Contain many directories.
>---
>- Git Working Directory = Working Tree (when uploading file online, see Git Arch):
>	- the ==folder== that you are working in its files.
>---
>- you need to track everything. 
><br>
>- OS independent 
>	- changing operating system doesn't affect the process.
><br>
>- Track History :
>	- who modified the code
>	- the time of modification
>	- the modification.
><br>
>---
>>[!caution]- Git Arch :
>>- The Tracking control version change some names to be able to avoid mistakes and conflicts...
>>	- File -> Blob
>>		- has the file content & type, size and other metadata about it
>>	- Directory -> Tree
>>		- the directory & ~~~~~ about it.
>>- it make some:
>>	- encryption
>>	- compression for speed and save memory as possible.
>>	- portable
>>---
>>- Those infos stored in hidden file called :
>>	- .git
>>		- ==.git = repo== means:
>>			- the file that contain all the versions and the modification occurred during the development process.
>---
>>[!faq]- Git Hash_SHA1 :
>>- the git use SHA1(secure hash algorithm) for encrypt and secure your data, but it add (null char, type & size) to the file to generate the cipher text.
>>	- echo "{blob(file type ??)} {file-size}{\\0}{file content}" | shasum
>>		- the original algorithm that git use with manual modification
>>	- echo "{file content}" | git hash-object --stdin
>>		- the prepared git algorithm
>---
>>[!caution]- Three Tree Architecture:
>>- submitting your modification over 2 stages not 1.
>>- the commit is added (الاعتماد) 
>>- just consider it as a second chance to re-watch and validate your code before pushing it to the Repository. (that not the reason but funny conclusion)
>>---
>>- The main reason :
>>	- When you need to make a change in files and is related to each other so you commit them with a single modification as a single version not a version for each file modified.
>>		- you have change your phone number, it is submitted in multiple files, so changing your phone number just will modify all other files and will be considered as single modification.
>>	- be used to be careful, if your project is a life project.






















