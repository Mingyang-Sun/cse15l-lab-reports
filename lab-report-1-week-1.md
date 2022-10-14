# Lab Report 1 - Remote Access and Filesystem

## Part 1 Installing VScode
1. First, I went to the [Visual Studio Code](https://code.visualstudio.com) website, then downloaded the appropriate version of the Visual Studio Code installer for my macOS operating system.
![Image](images/lab%20report%201%201.1.png)

2. When the installer has been downloaded, double click to unzip the file “VSCode-darwin-universal.zip” and then you will get the Visual Studio Code application to be installed.
![Image](images/lab%20report%201%201.2.png)

3. After the Visual Studio Code is installed, you can open the application and get a window that looks like this to be shown.
![Image](images/lab%20report%201%201.3.png)

## Part 2 Remotely Connecting
1. In order to use Visual Studio Code and a terminal to connect to a remote computer, the first step is that you need to open up a terminal in Visual Studio Code. You can achieve it by moving your cursor to the upper left corner and stopping right the terminal menu, and then clicking the new terminal option to open.
![Image](images/lab%20report%201%202.1.png)

2. After a terminal has been opened, you should type this command “ssh cs15lfa22??@ieng6.ucsd.edu” and replace ?? with your unique letters in your course-specific account. Then it will prompt you to enter your login password. Once you successfully logged into your remote server, you should see something similar to the following image.
![Image](images/lab%20report%201%202.2.png)

3. If you are wondering how to find your course-specific account username and password, you may follow this great [tutorial](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit) that covers every step that you needed.

## Part 3 Trying Some Commands
1. In line 62, you can see that I used a command of “ls”, which lists all the files and folders in the current directory. In line 63, the command “ls -a” is used to list all the files and folders including hidden files in the current directory. In line 64, “ls -lat” is a command that lists all the files and folders including hidden files in the current directory with more information like dates.
![Image](images/lab%20report%201%203.1.png)

2. In line 71, a “cd &lt;path&gt;” command is used to switch from the current working directory to where the destination could be placed in the &lt;path&gt;. In line 72, the “cd ~” command is used to navigate back to my home directory. In line 74, the command “cd ..” is used to navigate back to the previous working directory. In line 75, the command “pwd” stands for print working directory. In line 76, the command “cp &lt;path&gt;” is used to make a copy of the file in &lt;path&gt; to your current working directory.
![Image](images/lab%20report%201%203.2.png)

## Part 4 Moving Files with scp
1. In order to copy files back and forth between your local and remote computers, you could utilize the command “scp” to transfer your files. As you can see, I created a file called WhereAmI.java on my computer’s desktop using a terminal, put in some java code, and compiled and ran it on my terminal with some displays of my system information.

Some Java code:
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
![Image](images/lab%20report%201%204.1.png)

2. Then in the directory where I created that java file, I used the command “scp &lt;file&gt; &lt;destination&gt;” to transfer the file of “WhereAmI.java” to the destination “cs15lfa22cv@ieng6.ucsd.edu:~/” which is my remote computer. After utilizing the scp command, I logged back to my remote server, and with the command ls, you can see that the file WhereAmI.java is shown in my remote server’s directory.  
![Image](images/lab%20report%201%204.2.png)

## Part 5 Setting an SSH Key
1. Setting up an SSH key can replace the use of your password, which would save the time used for entering your password when you login into your remote server. To set up an SSH key, first, you will have to log out of your remote server. And then type the command “ssh-keygen” to begin. This “ssh-keygen” command will create a pair of files called the public key and private key. When users have been prompted to “Enter file in which to save the key (/User/username/.ssh/id_rsa)”, just press “enter” for this part to save the files in the default path. And then when users have been prompted to “Enter passphrase”, just press “enter” as well which would leave empty for no passphrase.
![Image](images/lab%20report%201%205.1.png)

2. After going through the entire ssh-keygen command processing, you should log in back to your remote server, create a “.ssh” directory using the command “mkdir .ssh”, and then go back to your client, and scp your ssh key to your remote server by the command “scp /Users/username/.ssh/id_rsa.pub cs15lfa22??@ieng6.ucsd.edu:~/.ssh/authorized_keys”. If you set everything up successfully, you can log in to your remote server without entering your password like the below image.
![Image](images/lab%20report%201%205.2.png)

## Part 6 Optimizing Remote Running
1. First I made a local edit to WhereAmI.java in my desktop directory using the command “vi WhereAmI.java”, and compiled and ran it again with new outputs displayed. Then I used the scp command to copy the WhereAmI.java files to the remote server.
![Image](images/lab%20report%201%206.1.png)

2. After the WhereAmI.java file has been scp to the remote server, I compiled and ran the WhereAmI.java file that is on the remote server without logging into my remote server by using the commands “ssh cs15lfa22cv@ieng6.ucsd.edu “javac WhereAmI.java” ” and  “ssh cs15lfa22cv@ieng6.ucsd.edu “java WhereAmI” ”. The reason why I compiled and ran the files without logging into the remote server is that wrote the commands in quotes at the end of an ssh command, which allows me to directly run the commands on the remote server.
![Image](images/lab%20report%201%206.2.png)

3. If you want to run multiple commands in the same line, you can use semicolons to separate them. For example, by running the commands “cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI” in the same line, you will copy the contents in WhereAmI.java to a new file called OtherMain.java, and then compile the OtherMain.java file, since these two .java files contain the exactly same contents, they will have the same .class file after compile.
![Image](images/lab%20report%201%206.3.png)