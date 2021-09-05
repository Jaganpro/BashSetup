
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

### COMMAND 1: (CURL Help)
* `curl --help` 
  * Provides a list of all commands and parameters supported. 
   ![image](https://user-images.githubusercontent.com/2145211/132132229-49625964-7dd7-4f53-ab67-83fb91493a0f.png)

### COMMAND 2: (Basics)
* `curl https://jsonplaceholder.typicode.com/posts` 
  * Syntax = curl (website)
  ![image](https://user-images.githubusercontent.com/2145211/132132259-5b031b9a-55ac-447e-b49d-ce061584f2a6.png)

### COMMAND 3: (Include Header Response)
* `curl https://jsonplaceholder.typicode.com/posts/1 --include`
  * --include -> Includes Header Information / Includes protocol response 
  ![image](https://user-images.githubusercontent.com/2145211/132132382-bd768a2a-0a86-4ce9-a6bd-39dbb01fd935.png)

### COMMAND 4: (Output Files with CURL)
* `curl https://jsonplaceholder.typicode.com/posts/1 --output sample.txt`

### COMMAND 5: (Creating a POST Request with CURL)
* `curl https://jsonplaceholder.typicode.com/posts --data "title=Hello&Body=HelloWorld"
  * --date --> Pass Data
![image](https://user-images.githubusercontent.com/2145211/132134485-e3fac820-183f-425a-a267-4f2174fec699.png)
