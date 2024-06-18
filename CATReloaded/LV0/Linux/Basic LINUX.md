

>[!tip]- Some instruction:
> - tap:
>	- for predicting what you want to type or showing all related to it.
>---
>  - ' . ': 
>	- in the beginning for hiding the file.
>---
> - ctrl + L: 
>	- for hiding instruction above the screen for clean screen.
>---
> - grep: 
>	- -i => for skip sensitivity of letters (A, a).
>---
>>[!tip] grep -rl " " :
>>- for displaying a file name based on its content.
>---
> - ' | ' 
> 	- for making multiple instructions in order.
>---
> - bg :
> 	-for make the process run in the background.
>---
>>[!success] find / -name " ":
>> - for searching in all directories for " ".
>>- you can search in specific location with put the name of the directory before the ' **/** '.
>>- or put ==~== before the ==/== which meaning ==home/urdirectory==.
>---
>>[!success] curl:
>>- show reply of a human readable domain (link), (google.com, yahoo.com, facebook.com).
>>- curl sample.com > file.txt => for putting the output in the file.txt
>---
>>[!success] '> & >>'
>> '>':
>> - for overwrite on a file
>>
>>' >> ':
>> - for adding on a file.
>> - see the curl example.
>---
>>[!caution] tee:
>> - for showing response of instruction like cat or echo in front of you and redirect it to a file.
>>	- curl www.google.com | tee google.txt
>>	- the previous example for showing the response of google.com on the screen and make a copy of the output in the file google.txt
>---
>>[!caution] df -h:
>>- showing hardware informations, -h (human readable).
>---
>>[!caution] top:
>>- for displaying all information about all processes in your computer.
>>- ==ps aux== almost the same but not interactive (info at a moment)
>---
>>[!caution] htop:
>>- the same as pervious but with GUI.
>---
>>[!bug] kill:
>>- for killing any process
>>- you can use "-9" as attribute to ensure killing ?!
>>- you need PID.
>---
>>[!caution] 2>&1
>>- error redirection.
>>- for replacing every error with successful output.
>>- ex:  
>---
>>[!caution] Copying ssh id:
>>- ssh-copy-id username@servername or ip.
>>- used for public machine access. 
>>- the password saved in the .ssh file ?!.
>---
>>[!caution] apropos:
>>- for searching for a command with its usage
>>- ex:   apropos port scanner
>---
>>[!bug]- Changing Users:
>>- w, who:
>>	- displaying the system users.
>>	- w for display the users with last time logged in.
>>
>>>[!caution] Swap between them:
>>>- use:
>>>	- su username => for normal admin
>>>	- sudo su root => for root admin.
>>
>>>[!danger] Execution as Another admin:
>>>- sudo -u username command => execute a command as another user. This is often used for administrative purposes.

>[!caution]- Reading & Modifying Permission:
>- drwxr-xr-x, {d, rwx, r-x, r-x}.
>- it is r w x in order and if a permission of them denied, it is replaced with '-' => (dash).
>
>>[!bug] Parts:
>>- first part => for file type.
>>- second part => for root permission.
>>- third part => for higher user permission.
>>- forth part => for normal user permission.
>
>>[!example] EXAMPLES:
>>- d => directory, '-' for file.
>>- r => read.
>>- w => write.
>>- x => execute.
>
>>[!bug]- Changing Permissions:
>>- chmod - - - filename.
>>- put the number of the authority for {root, high user then normal user}.
>>- ![[Pasted image 20240418060641.png]]
>>- ![[Pasted image 20240418061051.png]]
>>- ![[Pasted image 20240418061157.png]]

>[!caution]- Structure of linux file system:
>- information about all important directory in the system.
>
>>[!danger]- / :
>>- the root directory.
>>- contain only the needed directory in the top level.
>
>>[!caution]- /bin :
>>- available executable files, available to all users.
>
>>[!tip]- /dev :
>>	- for device drivers
>
>>[!bug]- /etc :
>>- supervisor direct for:
>>- host, users, configuration files, disk configuration files.
>>- having apt library with all link resources
>
>>[!caution]- /tmp :
>>- used for temporary files between system boots.
>
>>[!tip]- /mnt :
>>- Used to mount other temporary file systems, such as cdrom and floppy for the CD-ROM drive and floppy diskette drive, respectively
>>- about storage devices.
>

>[!danger]- Advanced Searching instructions:
>
>>[!caution] awk :
>>- for searching a specific word in a file or printing a word by a desired location.
>>	- awk  '/what you want/  {print}'  filename.
>>		- for searching for {what you want}, print the line which include it on the screen from the filename.
>>	- awk '{print $1, $3}' filename:
>>		- for printing first and third word from each line of filename file.
>>	- ==you can use uniq and other commands using | to only show uniq words and so on==
>
>>[!success] cut :
>>- for displaying specific bits or displaying all without a bit (by replacing what you want after -d with a space)
>>	- cut -b 1,2 filename
>>		- for displaying the first 2 characters(bits) on the screen
>>	- cut -d whatyouwant  -f  2,3  filename
>>		- for replacing whatyouwant with a tap then printing the second and third word from filename
>
>>[!tip] grep :
>>- for displaying a content in a file if found or the file name that contain the information required.
>>	- -i
>>		- for skipping small and capital letters.
>>	- -o
>>		- specific search for the entered word
>>	- -rl
>>		- if the info found, just show the file name that contain it.
>>		- r for recursive, for multiple files.
>>	- -e
>>		- it is like or
>>			- grep "thm" -e "cybertalent" /etc/passwd..
>>	- -A num
>>		- for show num of lines after found the needed word.
>>	- B num
>>		- for showing num of lines before the specific word.
>>---- 
>>- grep -i "testing" filename

>[!danger]- Base64 Encryption:
>- for encrypt syntax.
>- most ways you know it by its form...!
>---
>- echo "your syntax" | base64
>	- for encrypt files as a base64
>---
>- echo "encrypted syntax" | base64 -d
>	- for decrypting the file.

>[!caution]- Redirection:
>- for redirect input, output or error.
>- 0 -> input, 1 -> output, 2 -> error.
>- use 2>/dev/null  for redirect undesired errors to null file, like a trash in linux.
>---
>- output redirect:
>	- 1> filename
>		- overwrite with the new data
>			- 1>> just append without replacing the current content of the file.
>	- 2> filename
>		- error redirect with overwrite
>			- 2>> error append without overwrite.
>- fine, grep, etc...  &>> file
>	- for append output and error to file.
>- // // &> file
>	- for overwrite the content of file with the new errors and ouputs.

>[!todo]- Piping:
>- make the output of command as an input to another command.
>	- cat file.txt | grep -i -o "specific word".

>[!success]- Set:
>- for modifying user defined variables like:
>	- ls, history, cat, grep, ....
>- adding variables to the shell by just define them.
>	- x = 5
>- set | less
>	- for show manual file, page by page.
>- there you will find each command location,(address of each command.).
#### mapping.
[[Advanced Kali LINUX|Advanced LINUX Instructions]].
#linux 