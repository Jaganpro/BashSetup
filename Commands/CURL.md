
## CURL
* CURL is a tool to transfer data in and out of the server.
* It is a good tool for testing REST API, Downloading Files etc. 
* Various developers would prefer UI tools like PostMan, but CURL is another option.
* It supports 'n' number of protocols (FTP, HTTP, IMAP, POP3 etc.)

## INSTALLATION:
* Most modern Linux distribution have `curl` installed OOTB.
* If you are using Windows - Use Git Bash
* For the puposes of this tutorial - we are going to use `https://jsonplaceholder.typicode.com/` as an example website. 
  * For a sample GET Post : `https://jsonplaceholder.typicode.com/posts`
  * For a single GET Post: `https://jsonplaceholder.typicode.com/posts/1`

## COMMANDS:

* `curl --help` 
  * Provides a list of all commands and parameters supported. 
  
* `curl https://jsonplaceholder.typicode.com/posts` 
  * Syntax = curl (website)

* `curl https://jsonplaceholder.typicode.com/posts -i`
  * -i -> Includes Header Information 