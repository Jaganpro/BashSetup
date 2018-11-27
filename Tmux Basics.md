## What is Tmux?
Tmux is a terminal Multiplexer . There are multiple advantages in using tmux

* Terminal Split Screen
* Multiple Terminal Sessions with simple commands
* Run Processes that are not tied to your current sessions. (For Example, Long Running commands can be invoked using Tmux)
* Ability to SSH using Tmux
  * Ie, Ability to connect and disconnect sessions at will. Tmux will keep the session alive even if we exit the session.
* Share sessions with another person (Peer Programming) 

### 1. Install tmux

```
brew install tmux
```

### 2. Create a new Session/ detach and attach Session

If we just want to create a new session with default name, just type the following

```
tmux
```

In order to get detached from a session

```
tmux detach
```

To attach to a session

```
tmux attach
```

### 3. Exit tmux session

Just like any other terminal sessions, we can use `exit` command to exit tmux sessions
```
exit
```

### 4. Tmux Config

In order to manage configuration of Tmux, we can use the following file

```
vim ~/.tmux.conf
```

### 5. Commands using ctr-b

`ctrl-b` --> Prefix used in Tmux to invoke Tmux commands.
NOTE: This only works within Tmux terminals.
  
Examples:

* `ctrl-b + c` -- Create a new tmux Window
* `ctrl-b + ,` -- Rename current tmux Window

* `ctrl-b + p` -- Tab to previous tmux Window (p - Previous)
* `ctrl-b + n` -- Tab to next tmux Window (n - Next)
* `ctrl-b + w` -- List all Tmux window

Splitting Windows:

* `ctrl-b + %` -- Split Windows Vertically
* `ctrl-b + :` -- It helps us to provide named commands to Tmux. When we use `:split-window` we would be abke to split Window Horizontally (As there is no key-binding for vertical split)

Session Management:

* `tmux list-sessions` -- List all tmux sessions
* `tmux attach -t newshell` -- Attaching to existing tmux sessions

* `ctrl-b + d` -- Detach from the current session

### 6. Creating a new Tmux Session

```
tmux new -s newshell
```






### Things to learn
1. Installing tmuxp







