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
>>	- Staging then Commit.
>>		- after the staging, you should know the modified files and then you decide to confirm them by(commit) or modify them again before committing.
>>- Staging :
>>	- make The untracked files to tracked files to know if any modification happened or not.
>>
>><br>
>>
>>- the commit is added (الاعتماد) 
>>- just consider it as a second chance to re-watch and validate your code before pushing it to the Repository. (that not the reason but funny conclusion)
>>---
>>- The main reason :
>>	- When you need to make a change in files and is related to each other so you commit them with a single modification as a single version not a version for each file modified.
>>		- you have change your phone number, it is submitted in multiple files, so changing your phone number just will modify all other files and will be considered as single modification.
>>	- be used to be careful, if your project is a life project.
>---
>>[!todo]- Version in Reality :
>>- how to know versions and track updates of your files?
>>---
>>- there are a file for git that store all the files and its modifications as a blobs, tree and commit.
>>	- all of the previous are hashed values.
>>- for each file modified, there are hashed file for its location in the system
>>- you know if this package of modified files as an one patch(version) by the commit hashed value.
>>	- also stored with all the hashed values in the git folder in the system.
>>	- it is like pointer to the first file of the patch and your end.
>>	- it is wrapper -> border to each version's files.


---

>[!Caution]- Initialization of Git Repo :
>- `git clone https://"$TOKEN"@github.com/"$USER_NAME"/"$REPO_NAME".git`
>- `git config --global user.name "$USER_NAME"`
>- `git config --global user.email "$EMAIL"`
>---
>- you use `--global` for the current user. so if you want to clone another repo it will automatically take the global username and his email.
>- it modify `.gitconfig` file in your home directory.
>---
>`--system` :
>- this will be for all users in the system.
>- it modify in the `/etc/gitconfig` 
>- 

---

>[!Danger]- Commands:
>- `git add {' . ', ' * ', 'filename'}`
>	- for staging files and enable tracking.
>---
>- `git rm --cached {'filename', ' * '}`
>	- for remove staged filed from the staging area.
>	- unstage and remove files from stage area
>---
>- `git status`
>	- to know the status of your files, the changes happened in your repo area.
>	- very important
>	- `-s` for showing U or M for untracked and Modified.
>---
>- `git ls-files`
>	- show the files in the index area(staging area).
>	- you can put `-s` in the end to show the hashed file value
>---
>- `git log`
>	- show the last commit hashed value with the author and date of creation
>---
>- `git cat-file {attribute} {hashedvalue(first 4,5,... char of it would be enough)}`
>>---
>>- `git cat-file -t {hashed_val}`
>>	- for telling the **Type** of the hashed value(blob, tree or commit)
>>- `git cat-file -s $hashed_val`
>>	- for telling the size of the hashed val
>>- `git cat-file -p $hashed_val`
>>	- for Showing the content of the hashed val
>---
>- `git init`
>	- for initializing your local folder as a git repo.
>	- need to use clone with the token and username with it.
>---
>- `git restore`
>	- to restore your files to the last state from the staging area. before adding them to the index(staging area).
>	- if you use `git add .`, the `git restore` won't work.
>		- so you use `git restore --staged filename` first
>			- to restore the last version from the online repo in the staging area.
>			- then `git restore filename` to unchange last modifications
>---
>- `git reset HEAD~$num(1, 2, ..)`
>	- for restoring versions after committing.
>---
>- `git diff hashed_val..HEAD`
>	- to view the difference between 2 versions with the commit you added.
>---
>- `git reflog`
>	- for showing all log and the modification in those logs.
>---

---

>[!todo]- Tags:
>- for bookmarking the important commits.
>- not that important for now ... :<

---

>[!caution]- Branching:
>- if you want to have a parallel working in the same files.
>	- you are testing 2 separate feature in the same file, and you don't want to modify the original file and work in the 2 feature simultaneously.
>- control version, you have all your versions and modifications, so don't worry.
>---
>- first, when you make new branch, the both branches `master & testing` will point to the same file.
>- now if you want to modify the file as `testing`, you will have a version with your modification as a `testing`.
>- if you switch back to the `master` branch, the modification won't affect the current branch.
>---
>- `git switch bran_name`
>	- for switching branches.
>- `git branch bran_name`
>	- for creating new branch
>- `git branch -d bran_name`
>	- for deleting branch
>---
>>[!todo]- Merging Branches:
>>- to make all the modification to the same file. if the modification are in separate branches.
>>---
>>- you need to stop at the branch you want the modification inside it. `master` for example.
>>- `git merge OtherBranch` with the other branch
>>- now all inside the files in the `OtherBranch` will be inside the `master branch`

---

>[!Faq]- Thoughts?!
>- so git is a local version control and be inside your local machine, and save all your files inside your machine. for `git add` & `git commit -m`
>---
>- GITHUB :
>	- online platform that allow you to store files online for online sharing, depend on git.






