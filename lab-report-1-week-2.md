# Remote Access
*By Annika O'Rourke*

This blog post will teach you about remote access! 

## Step 1: Instaling Visual Studio Code

The first step will be to download Visual Studio Code to your device. Click the link and follow the instructions on the website. 

[Link](https://code.visualstudio.com/)

<img width="1537" alt="Screen Shot 2022-04-10 at 8 44 17 PM" src="https://user-images.githubusercontent.com/103288525/162662952-6cfa880c-f3c1-4d91-9024-f8a3092561bb.png">

^This is what you should see after you have installed Visual Studio Code. (Depending on your settings, it may look slightly different).

## Step 2: Finding Your Course-Specific Account for Remotely Connecting

In order to remotely connect, you need to know your account. It will be in the form: cs15lsp22zz, except the "zz" will be replaced by your own specific letters. To find this, go to this [link](https://sdacs.ucsd.edu/~icc/index.php). You will see something like this: <img width="1339" alt="Screen Shot 2022-04-10 at 9 12 31 PM" src="https://user-images.githubusercontent.com/103288525/162663974-3efefe5d-66b2-40ef-a943-2c4af69059b2.png">

Click "Submit", then you should see your course under "Additional Accounts". There, click your course, and find your specific course number. Congrats! You have found your course-specific account and can move on to the next step. 

## Step 3: Connecting Using the Terminal

Open Visual Studio Code, press Terminal, and click new Terminal. Next, type $ ssh cs15lsp22zz@ieng6.ucsd.edu except instead of zz, it should be your course specific account letters. It will prompt you to continue connecting, answer "yes". Then, it will prompt you to use a password. At this point, you should see: 

<img width="671" alt="Screen Shot 2022-04-10 at 9 50 38 PM" src="https://user-images.githubusercontent.com/103288525/162667039-bec3b466-3e58-4694-95e7-4179113542d1.png">


Use your password that you normally use when signing into ucsd related sites, the one you type when signing on using Active Directory. If you see something similar to:
```
Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
quota: No filesystem specified.
Hello cs15lsp22zz, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   23:25:01   0  0.08,  0.17,  0.11
ieng6-202   23:25:01   1  0.09,  0.15,  0.11
ieng6-203   23:25:01   1  0.08,  0.15,  0.11

Sun Jan 02, 2022 11:28pm - Prepping cs15lsp22
```

Congrats! You have successfully remotely connected. 

## Step 4: Trying Commands

Commands will look different on your own computer and after remotely connecting. Try some out! Here is a list of commands: 
* cd ~
* cd
* ls -lat
* ls -a
* ls <directory> where <directory> is /home/linux/ieng6/cs15lsp22/cs15lsp22abc, where the abc is one of the other group members’ username
* cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lsp22/public/hello.txt
  
  
Here is an example of what it might look like when you try them on your computer: 
  
  <img width="831" alt="Screen Shot 2022-04-10 at 10 09 13 PM" src="https://user-images.githubusercontent.com/103288525/162668833-79ad29e9-6374-438a-a3a5-9e32f45b9748.png">

 ## Step 5: Moving Files
  
  This is going to teach you how to move files between your computer and other computers. The first step is to create a file, named "WhereAmI.java". In the file, copy the following text:
  
  ```
  class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
  ```

  Open the terminal. You should see something like this: 
  
  <img width="722" alt="Screen Shot 2022-04-10 at 10 22 15 PM" src="https://user-images.githubusercontent.com/103288525/162670172-f1222305-ebec-46b5-aeed-4cca8bb533ef.png">

  
  Next, in the terminal, run the following command using your own specific letters: 
  ```
  scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/
  ```
  When it prompts you to input your password, do so. 
Log into ieng6 with ssh again, and use ls. You should see the file there in your home directory! Now you can run it on the ieng6 computer using javac and java.
  
## Step 6: How to set an SSH Key
  
  Sometimes it is annoying to input the password multiple times. Instead, let's use a command to skip this step. We will input commands to do this, as shown (the exact commands will be shown following:
  
  <img width="805" alt="Screen Shot 2022-04-10 at 11 06 53 PM" src="https://user-images.githubusercontent.com/103288525/162674893-fa5d4fa5-9949-437a-a47d-aff281abf1ae.png">

  
  Here is how to run it:
  
```
# on client (your computer)
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
```
  
**Do not add a passphrase for this step.**

```
Enter same passphrase again: 
Your identification has been saved in /Users/<user-name>/.ssh/id_rsa.
Your public key has been saved in /Users/<user-name>/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 <user-name>@<system>.local
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|       . . + .   |
|      . . B o .  |
|     . . B * +.. |
|      o S = *.B. |
|       = = O.*.*+|
|        + * *.BE+|
|           +.+.o |
|             ..  |
+----[SHA256]-----+
```
  
  Next, follow the steps to copy the public key to the .ssh directory of your user account on the server.
```
$ ssh cs15lsp22zz@ieng6.ucsd.edu
<Enter Password>
# now on server
$ mkdir .ssh
$ <logout>
# back on client
$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
# You use your username and the path you saw in the command above
```
  
 Congrats! Now you can ssh or scp from this client to the server without entering your password.

  
 ## Step 7: Optimizing Remote Running
  
  There are many ways to make remote running easier. For example, to run multiple commands at the same time, seperate them by semicolons. Shown here: 
  
  ```
  $ cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI
  ```
  
  Also, you can use the up arrow to recall the last command that you entered.
  For example, seen here, the second command line wasn't typed but recalled from the last command. It was much easier to do this than re-type the command.
  
  <img width="903" alt="Screen Shot 2022-04-10 at 11 12 50 PM" src="https://user-images.githubusercontent.com/103288525/162675654-addcbe92-6616-4dac-91fc-9b1afbd9b5a8.png">
  
**Thank you for reading! I hope you learned about remote access.**
  
  
