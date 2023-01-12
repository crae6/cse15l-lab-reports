# CSE15L Remote Access
### **1. CSE15L Account**

* First, goto this [link](https://sdacs.ucsd.edu/~icc/index.php) and look up your course-specific account name.

* Then, reset your course-specific password and press enter instead of pressing "Check Password". (Checking password will provide and error)

### **2. Install VSCode**

* Go to [Visual Studio Code's website](https://code.visualstudio.com/) and install the version compatible with your computer.

* If you have taken a CSE course at UCSD you will probably already have this program installed and be able to skip this step. 

* Here is an image of what VS code may look like when it is opened up. ![Photo of VS code](https://user-images.githubusercontent.com/122562172/212160695-7deb3f93-e485-492e-b75d-5819ce9b4045.png)

### **3. Remotely Connecting**

If you are on Windows you will first need to install [Git for Windows](https://gitforwindows.org/)

Then, in VS code you will open a new terminal by using the taskbar at the top of the screen. 

Next, we will enter the following commands into the terminal. 
> $ ssh cs15lwi23zzz@ieng6.ucsd.edu 

The "zzz" will be replaced by the letters in your cse15l username and the $ is just how we write commands, it will not be included in our command. 

because this is your first time connecting to this server you will get a message that looks like this 

<img width="511" alt="Screen Shot 2023-01-12 at 11 27 21 AM" src="https://user-images.githubusercontent.com/122562172/212162519-492a5aa7-7ed7-47ad-987b-2e75312a10da.png">
This message is normal for a first time login and you should just type "yes". 

Next, you will be prompted to enter the password that you reset at the beginning of this tutorial. Once you have logged in, the following message should appear.<img width="530" alt="Screen Shot 2023-01-12 at 10 32 51 AM" src="https://user-images.githubusercontent.com/122562172/212163216-906dd4db-4f18-4a07-a99e-28328bab80ee.png">

Now you should be connected!!

### **4. Testing Commands**

* Finally, we can test our connection by running some commands in our terminal that we've learnt in our lecture. 

* Here are some useful commands: 

  * cd ~
  * cd
  * ls -lat
  * ls -a
  * cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
  * cat /home/linux/ieng6/cs15lwi23/public/hello.txt

* Here is an example of one command in use! <img width="407" alt="Screen Shot 2023-01-12 at 11 37 05 AM" src="https://user-images.githubusercontent.com/122562172/212164232-74a54989-6331-47e7-b1f1-81f2a89fd0d0.png">

### **5. Exiting Remote Access**

* Finally, we can log out of the remote server by typing "exit" or pressing Ctrl-D.
