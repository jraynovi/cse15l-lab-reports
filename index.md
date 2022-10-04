# Remote Access Tutorial
## Step 1 (Account Lookup)-
### To look up your course-specific account, you must go to: [this link ](https://sdacs.ucsd.edu/~icc/index.php)and enter your information under account lookup: ![insert image](https://github.com/jraynovi/cse15l-lab-reports/blob/main/IMG_0411.jpg?raw=true)

### Once you receive your account information; under additional accounts, there will be an 11 character account beggining with "csl15fa22". Click on this account as highlighted in the image below:![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/lookupresults.jpg?raw=true)

### Proceed to reset your password and fill out your account information again, which will bring you to the "Global Passwod Change Request" page. Fill this page out and be sure to select "No" to reset your TritonLink password: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/dontchangetritonlink.jpg?raw=true)
## Step 2 (Download Visual Studio Code)-
### To download Visual Studio Code, first open this [link](https://code.visualstudio.com/) and follow the instructions (there are different versions so be sure to select the correct one for your operating system). Once you have it installed, the first window you see when you open the application should look similar to this: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/Part%201.png?raw=true)
## Step 3 (Connect Remotely)-
### To connect to the server remotely, we will be using the 11 character username and our newly created password. If you are on mac, ssh will be built in; however, on windows you must go to this [link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) and install OpenSSH. 
### Once we have SSH up and running, we will reopen Visual Studio Code and open terminal (Click on Terminal in top menu and select New Terminal). 
### In this terminal, you will type "ssh" followed by your accountname @ieng6.ucsd.edu. Your terminal should look like this: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.50.57%20PM.png?raw=true) You are now able to enter your password as follows (It will not write it out as you type, then press enter).
### You are now connected to the remote server if your screen looks similar to this: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.54.32%20PM.png?raw=true)
## Part 5- Test Commands
### To test out if our remote server is working correctly, we can test out some commands. Common commands include:
### cd
### ls
### cat
### pwd
### To learn more about what these commands do, you can head to this [link](https://kb.iu.edu/d/afsk), but your terminal will display the directories used, and be correctly switching directories: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/command%20test.png?raw=true)
## Part 6- Copy your computer to the remote computer
### First, we need to log out of our remote computer to work on our own. This is a simple step, where we use the command exit or Ctrl + D to get out of the system.
### We will now create a create a new java project file named WhereAmI.java in our local computer to test when we run our files. Once you have created the file copy and paste these contents:
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
### This will allow us to determine whether or not the file compiles when we run it in our terminal using java WhereAmI or javac WhereAmI.java.
