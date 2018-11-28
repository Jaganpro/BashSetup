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

* `Insert Mode` -- In this mode we are able to write text in the Editor
* `Normal Mode` -- In this mode we are able to navigate inside the Editor
* `Visual Mode` -- Mainly used to Select Text. There are variations in the text.  

NOTE:
To move between different modes, press `ESC` followed by the command.
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

Once the vim editor is open, we can go to the insert mode (Edit Mode) and provide the file name to edit in VIM.

```
:e vimtutordemo.txt
```

NOTE: Here `:e` short form for EDIT.

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

### Creating a New Tab in VIM

```
:tabnew
```
### Moving around in VIM Editor (Cursor Movements) [IN NORMAL MODE]

* (hjkl combo) (Basic Arrow keys replacements)
  * `h` - move cursor left
  * `j` - move cursor down
  * `k` - move cursor up
  * `l` - move cursor right

* (wWeEbB Combo) (Tip to remember -- WEB) (Jumping between words)
  * `w` - Jump forward to the start of the word
  * `W` - Jump forward to the start of the word (Words can contain puntuation)
  * `e` - Jump forward to the end of the word
  * `E` - Jump forward to the end of the word (Words can contain puntuation)
  * `b` - Jump backwards to the start of the word
  * `B` - Jump forward to the end of the word (Words can contain puntuation)
  
* (0$) (Line Navigation)
  * `0` - Jump to the start of the line
  * `$` - Jump to the end of the line
  
* (){} (Sentence and Paragraph Navigation)
  * `}` - Jump to next Paragraph ( or function/block when editing code)
  * `{` - Jump to previous Paragraph
  * `)` - Jump to next Sentence
  * `(` - Jump to Previous Sentence

* (HML Combo) (Lives closer to hjkl arrow keys) (Jumping within current Screen)
  * `H` - move to the top of the screen
  * `M` - move to the middle of the screen
  * `L` - move to the bottom of the screen
  
* (ctrl-b and f) (Screen Navigation)
  * `ctrl+b` - move back one full screen
  * `ctrl+f` - move forward one full screen

* (ggG) (Document Navigation)
  * `gg` - Jump to first line of the document
  * `G` - Jump to last line of the document

### Advanced movements around VIM

Get familier with usage of Arguments in VIM. For example,
If we want to skip and go down 10 lines, we can use the following: (Ie, it is executing 'j' command 10 times)

```
10j
```

Backus Normal Form is also supported in VIM:

In short

* `fx` - Jump to next occurance of character x
* `tx` - Jump to before next occurance of character x

```
[(n)um] <verb> <n(o)un>

Anything in [] --> Optional
Anything in <> --> Required
```

* `[n]f<o>` - Forward until the (nth) (o) (Inclusive)
* `[n]F<o>` - Backward until the (nth) (o) (Inclusive)
* `[n]t<o>` - Forward until the (nth) (o) (Exclusive)
* `[n]T<o>` - Backward until the (nth) (o) (Exclusive)




### Editing Text in VIM Editor (iIxXsSAoOcC)

Once we are in the document, we can start editing the files. There are multiple ways to edit files. But here are the common attributes

	`i` - Enter the Insert mode at Cursor
	`I` - Enter the Insert mode at the first non-blank character
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



### VIM Cheatsheet
	
![image](https://user-images.githubusercontent.com/2145211/48723633-22504180-ebf5-11e8-8aad-c9a7ebf61846.png)

Credits: www.viemu.com



