# MacSetup
All Setup Configurations for Mac or Linux Systems

### Top Packages to Install

1. Xcode
2. 

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





