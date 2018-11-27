## What is Tmux?
Tmux is a terminal Multiplexer . There are multiple advantages in using tmux

* Terminal Split Screen
* Multiple Terminal Sessions with simple commands
* Run Processes that are not tied to your current sessions. (For Example, Long Running commands can be invoked using Tmux)
* Ability to SSH using Tmux
  * Ie, Ability to connect and disconnect sessions at will. Tmux will keep the session alive even if we exit the session.
* Share sessions with another person (Peer Programming) 

### 1. Create a new Session or Window

If we just want to create a new session with default name.

```
tmux
```

If we want to specify a name, use the following syntax

```
tmux new -s <name> 
```

### 2. Exit tmux session

Just like any other terminal sessions, we can use `exit` command to exit tmux sessions
```
exit
```

### 3. Tmux Config

In order to manage configuration of Tmux, we can use the following file

```
vim ~/.tmux.conf
```

### 4. Commands using ctr-b

`ctrl-b` --> Prefix used in Tmux to invoke Tmux commands.
NOTE: This only works within Tmux terminals.
  
Examples:

* ctrl-b + c -- Create a new tmux Window
* ctrl-b + , -- Rename current tmux Window

* ctrl-b + p -- Tab to previous tmux Window (p - Previous)
* ctrl-b + n -- Tab to next tmux Window (n - Next)
* ctrl-b + w -- List all Tmux window

Splitting Windows:

* ctrl-b + % -- Split Windows Vertically
* ctrl-b + : -- Split Window Horizontally

















