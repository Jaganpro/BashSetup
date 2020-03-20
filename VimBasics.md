## Vim Editor

![image](https://user-images.githubusercontent.com/2145211/77179809-5ebcd780-6a9f-11ea-8d80-c31fd02e6315.png)

* We are also going to learn how to use various screen multiplexers
* How we can use this to deliniate various projects we are working on.
* We can potentially use Hotkeys to make our whole computer work with Vim Editor.
* Getting rid of the mouse - how to shift to keyboard centric programming model

![image](https://user-images.githubusercontent.com/2145211/77178676-cbcf6d80-6a9d-11ea-8fb3-f5ccf5b67c3d.png)

* It is shipped on any unix like platform
* It is highly customizable - Example: Writing specific macro, 
* Super low CPU Usage
* Super efficient - If you speak the VIM Language


* What distinguishes VIM from other editors?
* Most programmers edit code more than they write code.
* There are usually 7 modes, but 4 are the most important

![image](https://user-images.githubusercontent.com/2145211/77178720-dd187a00-6a9d-11ea-93ec-2ff1917d2b2e.png)

* Normal Mode - 
  * This is where we do most of textual and visual interactions.
  * Here you interact with text and tell it what to do.
  
* Insert Mode - 
  * i - insert
  * a - append
  * c - change

* Visual Mode
  * Similar to Normal Mode, except it works with highlighted blocks of text.
  * You have different types
    * Visual Character Mode
    * Visual Line Mode
    * Visual Block Mode
    
* Command Line Mode
  * This is how you will be able to utilize unix commands which have been shipped from the 90's (Example: Search and Replace)
  
![image](https://user-images.githubusercontent.com/2145211/77179025-4bf5d300-6a9e-11ea-81c9-c831af17ab2c.png)

* Vim is not a character editor.
* It is a language by itself. 
* We want to think in terms of operators, text objects and motions
  * Operators act upon text objects or motions.

![image](https://user-images.githubusercontent.com/2145211/77179781-506ebb80-6a9f-11ea-87eb-adbc3add66c1.png)

* Operators are the verb of the vim language
* It specifies actions to be performed on text objects or motions.
  * c - change
  * d - delete
  * y - yank (Copy to your register)
  * gU - Make it uppercase (go Uppercase - if you want to remember)
