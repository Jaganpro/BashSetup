## What is Tmux?
Tmux is a terminal Multiplexer . There are multiple advantages in using tmux

* Terminal Split Screen
* Multiple Terminal Sessions with simple commands
* Run Processes that are not tied to your current sessions. (For Example, Long Running sessions can be invoked using Tmux)
* Ability to SSH using Tmux


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
