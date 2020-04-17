# Simple Bash Commands
Collection of simple bash commands to get started with Terminal

#### NOTE 1:
> ~ --> This symbol means we are in User's Home directory <br />
> $ --> This symbol means we are in Root Directory <br />
> [Command] + [K] --> Clears out Terminal Screen <br />
> [Control] + [C] --> Break / Exit from application within Terminal

#### NOTE 2:
* In order to change the shell, please use the following command 
 
`chsh -s /bin/bash` (Bash By Default)
`chsh -s /bin/zsh` (Zsh by Default)

## Basics

**Command : `who am i`** <br />
Shows Username, Terminal ID, Date & Time

![image](https://user-images.githubusercontent.com/2145211/38342077-0e3815ba-384a-11e8-9693-aa3c0b1bcfd5.png)

**Command : `whoami`** <br />
Shows Username only

![image](https://user-images.githubusercontent.com/2145211/38342095-2e0b1874-384a-11e8-8686-fc10070cb3da.png)

**Command : `exit`** <br />
Exits terminal Window

**Command : `clear`** <br />
Clears the terminal Window

**Command : `history`** <br />
Provides history of all past commands you have typed in the shell

![image](https://user-images.githubusercontent.com/2145211/38342227-1567f246-384b-11e8-866f-44e2a247dd42.png)

`History n` --> Only lists the last n commands <br />

**Command : `echo`** <br />
Prints the text

`echo "Hello World"` --> Prints Hello world text <br />

**Command : `alias`** <br />
Give a pseudonym to another command

`alias cdul = "cd .."` --> When we type in cdul, "cd .." command would be executed.

**Note**
In order to add `alias` to terminal, we have to add these alias to Bash config file `~/.bashrc` <br />
Type `sudo open ~/.bashrc`, edit this file and add alias here and save it. Restart your Terminal for alias to take effect. <br />

**Command : `unalias`** <br />
Removes existing alias

`unalias cdul` --> Removes alias from the terminal.

## Directories
**Command : `pwd`** <br />
Print Working Directory

**Command : `ls`** <br />
List files in a directory

`ls -l` --> files displayed as list
`ls -lr` --> r stands for human readable file size 

**Command : `cd`** <br />
Change Directory

`cd` --> Change Directory <br />
`cd ~` --> Goes to Home directory <br />
`cd ..` --> Up a level from current directory <br />
`cd ...` --> Up two level from current directory <br />
`cd Pictures` --> Goes to pictures directory <br />
`cd Users/Jvalaiyapathy` --> Takes us to User directory <br />

**Command : `mkdir`** <br />
Creates a new directory in the current folder

`mkdir sampleFolder` --> Creates a new folder called "SampleFolder" <br />
`mkdir folder1 folder2 folder3` --> Creates multiple folder at the same time <br />
`mkdir -p /home/misc/salesforce` --> Creates all parent folder such as misc, salesforce on the fly <br />

**Flags** <br />
`-v` --> Get confirmation where the directory was created <br />
`-p` --> Allows to create all parent folder on the fly. When we are using this flag, mkdir won't error out if the folder already exist. If it does not exist, then it creates the given folder.<br />

**Command : `rmdir`** <br />
Removes the directory in the current folder

`rmdir sampleFolder` --> Removes "SampleFolder" directory 

## File Operations

**Command : `cp`** <br />
Copy files to specific location <br />

`cp *.txt ~` --> Copy all files of type txt to Home directory <br />
`cp text1.txt ~\HomeTab` --> copy specific file to HomeTab folder <br />

**Command : `mv`** <br />
mv is short for move <br />
Rename folder or file <br />
It is also used to move files to different location <br />

`mv text1.txt text2.txt` --> Moving file to a different location. 
                             text1.txt is the old name of the file, text2.txt is the new name<br />
`rm -f text1.txt` --> You may want to consider removing old file 'text.txt' from current directory<br />

`mv test1.text ~/SampleDirectory` --> Move test1.text file to Sample Directory. <br />
`mv *.txt ~/SampleDirectory` --> Move all files of type txt to Sample Directory <br />
`mv * .` --> Move all files to current directory [This does nothing] <br />
`mv * ..` --> Move all files to 1 level up directory <br />
`mv * ...` --> Move all files to 2 level up directory <br />

**Command : `rm`** <br />
Remove a folder or a file

`rm Jag.txt` --> Removes file <br />
`rm yetAnotherFolder` --> Removes folder "yetAnotherFolder" <br />
`rm -rfv yetAnotherFolder` --> Remove with force. Perform Hard delete. <br />

**Flags** <br />
`-f` --> to ignore non-existent files, never prompt <br />
`-r` --> to remove directories and their contents recursively <br />
`-v` --> to explain whats being done <br />

**Command : `touch`** <br />
create new files or changes file stamp. It is only used to create empty files

`touch index.html` --> creates a new file called "Index.html" <br />

## Create / Open Files
**Command : `open`** <br />
open current location or file

`open index.html` --> open a file <br />
`open index.html -a "Sublime Text` --> open a file in Sublime Text editor <br />
`open . -a "Sublime Text"` --> Open the current folder in Sublime Text editor <br />
`open /custom/path/ -a "Sublime Text"` --> Open specific folder in Sublime Text editor <br />

**Flags** <br />
`-a` --> Specify the name of the application which can be used to open the file. Please note that the name of the application is case sensitive <br />

## Misc
**Command : `screencapture`** <br />
Takes screenshot of the screen

`screencapture -x -t jpg screenshot.jpg` --> creates JPG screenshot and stores in current directory<br />

**Flags** <br />
`-P` --> Take screenshot and preview immediatly <br />
`-x` --> Take screenshot silently <br />
`-t` --> Specify the filetype <br />

## File Examination
**Command : `cat`** <br />
Outputs the contents of the file <br />

`cat index.html` --> Prints the contents of Index.html in the terminal (In this case CAT opens the file) <br />
`cat < index.html` --> In this case the shell opens the file passing it as CAT's standard Input <br />
`cat > newFile.txt` --> This helps to CREATE A NEW FILE called "newFile.txt". We will be prompted to enter text in terminal. <br />
To save the contents of this file press `Ctrl + D` to save and exit. <br />
`cat file1.txt file2.txt > mergedfile.txt` --> Here CAT is used to merge 2 files to a single file. <br />

**Command : `ln`** <br />
Used to Link a file. There are 2 types of links (Soft Link, Hard link)

`ln old.txt new.txt` --> Now the old.txt file is linked to new.txt. new.txt is similar to a replica of old.txt. <br />
                         Any changes made to old.txt will be reflected in new.txt. This is hard link <br />
                         If old.txt is deleted, new.txt will still be accessible <br />
`ln -s old.txt new.txt` --> This creates a soft link between old.txt and new.txt. If old.txt file is deleted, new.txt will not be accessible <br />

## File Permission
 
When we create a file in Shell, there are 4 options which set by default: <br />
A. `User (User who owns the file)` --> Read and Write Permission (Default) <br />
B. `Group (User belonging to file defined ownership group)` --> Read Only Permission (Default) <br />
C. `Other (Everyone else)` --> Read Only Permission (Default) <br />
D. `Execute (Allow executing file as Program)` --> False (Default) <br />

Numeric Values of Pemissions: <br />
`Read (r)` - 4 <br />
`Write (w)` - 2 <br />
`Execute (x)` - 1 <br />

A file at best can have a total numeric value of (4+2+1) = 7 <br /F> 

**Command : `umask`** <br />
Returns the value of system file mode creation mask. Default value is 022 <br />
When we create a file, the system as default subtracts 666 - 022 = 644 (For File), 777 - 022 = 755 (For Folder) <br />
So the default permissions for a file is 644. <br />
`6` --> Owner of the file can Read and Write ( 6 = 4 + 2) <br />
`4` --> Group can only Read file <br />
`4` --> Other can only Read file <br />


## Searching and Sorting
coming soon! <br />

## System Information
coming soon! <br />

## Regular Expressions
coming soon! <br />

Reference: https://courses.cs.washington.edu/courses/cse390a/14au/bash.html <br />
