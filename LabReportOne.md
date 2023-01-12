# CSE 15L Tutorial
## Step 1: Installing VScode

First, go to the Visual Studio Code website and download the application: [Visual studio code link](https://code.visualstudio.com/).
Confirm that you downloaded the proper version of the application, which is dependent on the operating system.

Initial Interface of VScode:
<img width="1512" alt="Screen Shot 2023-01-11 at 10 21 21 PM" src="https://user-images.githubusercontent.com/122497830/211992664-4e7a4c5a-934a-4dc8-a68d-6d610c3e16f0.png">

## Step 2: Remotely Connecting
The second step of the tutorial is to remotely connect to another computer. Open a terminal in VScode and type ssh cs15lwi23??@ieng6.ucsd.edu (Replace ?? with the appropriate letters in your account name). Once you successfully login by also typing in your password, you should encounter an interface like below.

<img width="504" alt="Screen Shot 2023-01-11 at 3 46 43 PM" src="https://user-images.githubusercontent.com/122497830/211998602-5b4a637c-16ee-4f40-8918-b5e470238759.png">

## Step 3: Trying Commands 
Try some of the following commands in the terminal. Note, if you want to utilize these commands in the remote computer, you must type in ssh first prior to the command. Note: some commands may lead to errors. 

Commands:
- cd
- pwd
- cd~
- ls -lat
- ls -a
- cat /home/linux/ieng6/cs15lwi23/public/hello.txt
- cat /home/linux/ieng6/cs15lwi23/public/hello.txt ~/

What the ls -a command does:
<img width="1240" alt="Screen Shot 2023-01-11 at 4 15 57 PM" src="https://user-images.githubusercontent.com/122497830/212000789-2604cfa4-b2b9-447f-bef8-09d6941f9d19.png">
