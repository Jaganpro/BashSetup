# MacOS Terminal Setup
All Setup Configurations for Mac or Linux Systems

### Top Packages to Install

* Xcode
* Brew (Package Manager)
* Git
* Vim
* Z Shell
  * Oh my Zsh
* Utils
  * Tree
* JAVA



### 1. Install XCode Command Line Tools

Usage: XCode is a command line tool package which includes everything that the developer needs to get started with development in Mac OS. It installs commonly used tools such as GCC, clang, perl, svn, git, strings, cpp and other default commands usually found in linux distribution.

```
xcode-select --install
```

If we print the path of the Xcode, we will be able to see the list of packages installed in our system

```
xcode-select --print-path
```
We would get something like this `/Library/Developer/CommandLineTools`

In order to see the list of tools installed in our system, we can go to the following location

```
cd /Library/Developer/CommandLineTools/usr/bin
```

![image](https://user-images.githubusercontent.com/2145211/48972258-c6baf500-eff4-11e8-8b81-ad7cf2ecf93b.png)


### 2. Homebrew

Homebrew is the most popular Package Manager for Mac OS X. It is a tool used to easily install open source applications and manage versions of different applications easily.

Installing Brew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

This script installs Homebrew at `/usr/local` 


Important Commands to remember:

* `brew list` - List all installed Formulae in local system.
* `brew install <formulae` - Install specific Formulae using brew
* `brew uninstall <formulae>` - Uninstall a specific Formulae.
* `brew update` - Fetches newest version of Homebrew and all formulae from Github.
* `brew upgrade [formulae]` - Upgrade outdated Formulae. 
* `brew cleanup` - Removes any older versions of Packages that you have installed.
* `brew doctor` - It will check the system for any potential problems

Top Packages to install with Brew:

* https://gist.github.com/indiesquidge/ec010eca3ffa254788c2
* https://www.quora.com/What-are-the-first-or-must-have-homebrew-packages-that-you-install-on-your-Mac
* http://osxdaily.com/2018/03/26/best-homebrew-packages-mac/

### 3. Install Git

Git is free and open source distributed version control designed to handle small and large scale development projects. 
If you already have git, update git to its latest version

```
brew install git
```

![image](https://user-images.githubusercontent.com/2145211/48984655-8038c980-f0cc-11e8-8cc3-9f858e7ee342.png)


### 4. Install Vim

Vim is a highly configurable text editor

```
brew install vim
```

Once you installed vim, you should be able to check the version

```
vim --version|head -n 1
```

![image](https://user-images.githubusercontent.com/2145211/48984900-b4fa5000-f0cf-11e8-8d82-fc1102ffd272.png)


Refer to this tutorial, if you want to get started with VIM  https://github.com/Jaganpro/Vim-Tutorial


### 5. The Z Shell 

Z Shell or also called as `zsh`, is built on top of Shell. Its primarily installed to configure plugins and themes.

```
brew install zsh
```

Once you install `zsh`, please install the framework `oh my zsh` which helps to manage `zsh` configuration.
The configuration of `zsh` is under `~/.zshrc` file.
Please see here for more information : https://github.com/robbyrussell/oh-my-zsh


We can use `curl` to install `oh my zsh`
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

After installing `zsh`, if the default terminal has not changed to `zsh`, use the following command to change the default terminal
```
chsh --shell $(which zsh)
```

`chsh` - Change Shell
`--shell` - Name the user's login shell.


### 6. Tree

Tree is a command line utility which represents directory structure in a more presentable manner.
This can be used as a replacement for `ls -l` command.

```
brew install tree
```

![image](https://user-images.githubusercontent.com/2145211/48985158-ea546d00-f0d2-11e8-8443-2bb8192e9e84.png)

Usage:

```
tree -L 1
```

`-L` - Represents Level of Depth to be rendered

![image](https://user-images.githubusercontent.com/2145211/48985232-6fd81d00-f0d3-11e8-9f9d-221c720015a9.png)


### 7. JAVA

If you want to install JAVA, we have the following options

A. Install it using the Oracle Website : https://www.oracle.com/technetwork/java/javase/downloads/index.html

B. Install it using Brew

```
brew update
brew tap caskroom/versions
brew cask install java
```
This would install `JAVA 9`. If we want `JAVA 8`, then use `brew cask install java8`

If we have installed the JAVA correctly, then we should be able to verify the version.

![image](https://user-images.githubusercontent.com/2145211/48985404-1ffa5580-f0d5-11e8-9bc2-ce1216596353.png)

The next step is to set the JAVA path correctly. Please see the `Setup Environment Variables` topic to understand more about environment variables. 

```
export JAVA_HOME="`/usr/libexec/java_home -v 1.8`"
```


### 8. Setup Environment Variables (Setup in MAC OS)

1. What are Environment Variables?
Environment Variables are global system variables accessible by process running under the Operating System (OS). They are useful to store system-wide values such as Directories to search the executable programs (PATH)

2. How to Print all the Environment Variables in Mac OS?

```
printenv
```
We should be getting something like this:

![image](https://user-images.githubusercontent.com/2145211/48972713-ccb5d380-effe-11e8-8240-a3d4b5074abc.png)

NOTE: This environment variables also include the "PATH" variable, which we commonly use to launch applications in terminal.

3. How to print the current value of the $PATH variable?

```
echo $PATH
```

![image](https://user-images.githubusercontent.com/2145211/48972757-bbb99200-efff-11e8-96ac-12705a58b0a5.png)

Please note that in MAC OS, the values are seperated by `:` 


4. How do you add directory to the $PATH variable? 

```
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
```

This command takes everything in the single quotes and adds it to `~/.bash_profile` file.
Everytime you open a new terminal, `.bash_profile` is called.
The `export $PATH` line tells your system to look in `/usr/local/bin` first, since that's where homebrew installs tools.

NOTE: If you are using `zsh`, use the `~/.zshrc` file to update the PATH.


### Troubleshooting

NOTE: Whenever we get the error where we cannot write to a certain path (say `/usr/local`), we can give the following command

```
sudo chown -R `whoami` /usr/local
```
* `sudo` allows to run commands using higher access rights
* `chown` means Change Owner
* `-R` flag applies this to all nested files and directories
* `whoami` Variable that represents OSX username


### Other Installations

* NPM
* Node JS

