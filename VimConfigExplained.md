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
