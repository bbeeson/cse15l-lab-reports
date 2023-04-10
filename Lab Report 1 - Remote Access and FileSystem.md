# Lab Report 1

This will act as a guide and cheat sheet for remembering how to log into a course-specific account on ieng6.

The main steps in order are:
*** 
- [Lab Report 1](#lab-report-1)
  - [Installing VSCODE](#installing-vscode)
  - [Remote Connection](#remote-connection)
  - [Commands](#commands)


## Installing VSCODE
First we have to download Vscode, here is the link to the download page
[VScode_Download](https://code.visualstudio.com/)

After installing Vscode and opening the application, it should look like this:

![Image](screenshots/installed_vscode.png)

## Remote Connection
Since a majority of the courses at UCSD uses a course specfic account it is good to be able to login into the remote server associated with that account. It can be helpful when collaborating with other students and uploading files. 

First make sure git is installed. Go onto VScode and open a new terminal. Use the ssh command alongside the account specific username, which for me is cs15lsp23ab therefore the command will be:
ssh cs15lsp23zz@ieng6.ucsd.edu
Then enter your username and password when prompted.

After connection it should look like this.

![Image](screenshots/successful_remote.png)

## Commands

Finally we can try to perform some commands into the terminal. Commands that will work are ones such as cd, ls, pwd, and mkdir.
Where cd will change what directory you are assessing, ls will list the contents of the directory you are in, pwd will print 
what the current working directory you are working in is, and finally mkdir will make a new directory for you to work inside of. 


![Image](screenshots/some_commands.png)

