# Vim
This repo introduces basics of Vim and its usage.

### Check Vim Installation and Version

Most of the Mac computers should have VIM pre-installed

![image](https://user-images.githubusercontent.com/2145211/48574771-06d7f480-e8de-11e8-8294-f3fda37adeea.png)


### Introduction

Vim in essense a Free and Open Source(FOSS) advanced text editor. It is highly configurable.
It different from other editors because it introduces the concept of Modality (Ie, it has different modes).
We spend more time reading code than writing it. VIM is optimized for what you do most (Reading/Navigating Text)


There are 3 different types of modes in VIM:

* Insert Mode -- In this mode we are able to write text in the Editor
* Normal Mode -- In this mode we are able to navigate inside the Editor
* Visual Mode -- Mainly used to Select Text. There are variations in the text.  

NOTE:
To move between different modes, press "ESC" followed by the command.
Ie, Pressing `ESC` quits from Insert Mode to Normal Mode. Then we can use `:` and type the command.
We can press `i` again to get back into Insert Mode.

### Opening files in VIM Editor

```
vim <filename>
vim test.txt
```

The other way to open VIM Editor is to just type "vim"

```
vim
```

This opens up the Vim Editor. Then we can go to the insert mode (Edit Mode) and provide the file name to edit in VIM.

```
:e vimtutordemo.txt
```

NOTE: Here ":e" short form for EDIT.

![image](https://user-images.githubusercontent.com/2145211/48583941-7a85fb80-e8f6-11e8-8be9-348b5d7b0de8.png)


### Closing the VIM Editor

This will close the editor without saving the file.
```
:q! 
```

### Saving a file in VIM Editor

```
:w <filename>
:w test.txt
```

NOTE: There is a special program called as the "VimTutor". It can be run using the command 'vimtutor'. It is a text file which describes the basics of the VIM Editor.

### Moving around the VIM Editor (hjkl)

Once you are inside of the VIM Editor, you can use the arrow keys or the following keys for the cursor to move 
right, down, up, left (h, j, k, l)


	    k
	    ^
	h <   > l
	    v
	    j

They also introduce us to the concept/Usage of Arguments in VIM. For example,

If we want to skip and go down 10 lines, we can use the following: (Ie, it is executing 'j' command 10 times)

```
10j
```

### Creating a New Tab in VIM

```
:tabnew
```

### Editing Text in VIM Editor (iIxXsSAoOcC)

Once we are in the document, we can start editing the files. There are multiple ways to edit files. But here are the common attributes

	`i` - Enter the Insert mode at Cursor
	`I` - Entet the Insert mode at the first non-blank character
	`x` - Delete the current Character
	`X` - Delete the one on the left
	`s` - Substitute Character under cursor.
	`S` - Substitute the entire line
	`A` - Append text at End of Line
	`o` - Open Above - Enter Insert more on the next line
	`O` - Open Below - Enter Insert more on the line above
	`c` - Change
	`C` - Change to End of Line (Delete the characters from the Cursor Position to EOL)
	
### Editing in VIM : Beyond Basics - 1 (wWbBeE)

	`w` - (Next word) Forward to the beginning of the next word (Seperated by characters)
	`W` - (Next WORD) Forward to the beginning of the next WORD (Seperated by White Space)
	`b` - (Back word) Backward to the next beginning of the word
	`B` - (Back Word) Backward to the next beginning of the WORD
	`e` - (end word) Forward to the next end of the word
	`E` - (end WORD) Forward to the next end of the WORD
	
NOTE: We can also use this as arguments, For example, skips 3 words

```
3w
```

NOTE 2: `hjkl` and `wbe` are introduction to commands which have `numbers` before the command.

### Editing in VIM : Beyond Basics - 2 (fFtT)

NOTE: These commands introduces full syntax of VIM Editor

Backus Normal Form for VIM:

```
[(n)um] <verb> <n(o)un>

Anything in [] --> Optional
Anything in <> --> Required
```

* `[n]f<o>` - Forward until the (nth) (o) (Inclusive)
* `[n]F<o>` - Backward until the (nth) (o) (Inclusive)
* `[n]t<o>` - Forward until the (nth) (o) (Exclusive)
* `[n]T<o>` - Backward until the (nth) (o) (Exclusive)


### VIM Cheatsheet
	
![image](https://user-images.githubusercontent.com/2145211/48723633-22504180-ebf5-11e8-8aad-c9a7ebf61846.png)

Credits: www.viemu.com

### Configuring VIM Editor

In order to configure VIM Editor, we have to edit `~/.vimrc` file.

```
vim ~/.virmc
```

The following are list of options to consider enabling before using VIM Editor.

1. Enabling Current Line Numbers in VIM Editor

```
set number
```

2. Enable Relative Line Number

```
set relativenumber
```

3. Turn on Syntax Highlighting

```
syntax enable
```

4. Set History to retain more commands. (By Default, VIM Saves last 8 commands).

```
set history=100
```

5. AutoIndent (Ie, if my current line is indented 3 spaces, when i press enter, the next line should automatically indent 3 spaces as well

```
set autoindent
```

NOTE: If you want to undo the default indent behavior just use `^d (Ctrl + d)` 

6. Make Search Case Insensitive

```
set ignorecase
```

7. Highlight Matching Search String

```
set hlsearch
```

8. Display mode at the bottom of the screen

```
set showmode
```

9. Remove compatibility of old vi editor
```
set nocompatible
```


### TODO: Other things to learn / Needs more research

1. sudo apt -- Command
2. How to update apt 
3. What are all the packaged installed for "apt" 
4. How to update the JAVA_HOME variable
5. Learn more about the "open ~/.bash_profile" 
6. Learn more about "sudo apt-get update" command
7. "sudo apt-get install vim"
8. Setting up ".vimrc" file
9. http://fisadev.github.io/fisa-vim-config/  -- Fisa Vim Config
10. Popular Plugins to Install for Vim -- For example : File Explorer
11. Remapping CAPS Lock Key to Escape -- https://pqrs.org/osx/karabiner/index.html
12. Vim CheatSheet - https://www.glump.net/_media/howto/desktop/vim-graphical-cheat-sheet-and-tutorial/vi-vim-cheat-sheet-and-tutorial.pdf
13. Configuring VIM - ~/.vimrc  -- This is the file to configure VIM . "Using ~ means Home Directory" - Make sure that we check it in GITHUB - 
14. Use other peoples vimrc dot files - 
15. Dot Files Management in Mac - https://github.com/thoughtbot/dotfiles
16. Plugins for Development:
	A. Ctrl P - Fuzzy file search
	B. NerdTree
	C. AG for Vim - Helps to search through projects
17. :set showcmd
18. https://nvie.com/posts/how-i-boosted-my-vim/
19. https://medium.com/usevim/vim-101-set-hidden-f78800142855
20. VIM Airline : https://github.com/vim-airline/vim-airline
21. VIM Themes : https://github.com/reedes/vim-thematic
22. NerdTree Setup : https://medium.com/@victormours/a-better-nerdtree-setup-3d3921abc0b9
23. Common Configuration setup of VIM: https://github.com/carlhuda/janus
24. Using i3 for Window Management. This is only available in linux. So use https://ianyh.com/amethyst/ for Mac.
25. VIM + Tmux
26. https://medium.freecodecamp.org/learn-linux-vim-basic-features-19134461ab85

