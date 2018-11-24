# MacOS Terminal Setup
All Setup Configurations for Mac or Linux Systems

### Top Packages to Install

1. Xcode
2. Brew (Package Manager)

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

Homebrew is the most popular Package Manager for Mac OS X. It is a tool used to easily install open source applications and manage versions easily.

Installing Brew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

This script installs Homebrew at `/usr/local` 




### Environment Variables (Setup in MAC OS)

1. What are Environment Variables ?
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






