# Remote Access Tutorial
## Step 1 (Account Lookup)-
### To look up your course-specific account, you must go to: [this link ](https://sdacs.ucsd.edu/~icc/index.php)and enter your information under account lookup: ![ahhhhh](https://github.com/jraynovi/cse15l-lab-reports/blob/main/IMG_0411.jpg?raw=true)

### Once you receive your account information; under additional accounts, there will be an 11 character account beggining with "csl15fa22". Click on this account as highlighted in the image below:![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/lookupresults.jpg?raw=true)

### Proceed to reset your password and fill out your account information again, which will bring you to the "Global Passwod Change Request" page. Fill this page out and be sure to select "No" to reset your TritonLink password: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/dontchangetritonlink.jpg?raw=true)
## Step 2 (Download Visual Studio Code)-
### To download Visual Studio Code, first open this [link](https://code.visualstudio.com/) and follow the instructions (there are different versions so be sure to select the correct one for your operating system). Once you have it installed, the first window you see when you open the application should look similar to this: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/Part%201.png?raw=true)
## Step 3 (Connect Remotely)-
### To connect to the server remotely, we will be using the 11 character username and our newly created password. If you are on mac, ssh will be built in; however, on windows you must go to this [link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) and install OpenSSH. 
### Once we have SSH up and running, we will reopen Visual Studio Code and open terminal (Click on Terminal in top menu and select New Terminal). 
### In this terminal, you will type "ssh" followed by your accountname @ieng6.ucsd.edu. Your terminal should look like this: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.50.57%20PM.png?raw=true) You are now able to enter your password as follows (It will not write it out as you type, then press enter).
### You are now connected to the remote server if your screen looks similar to this: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.54.32%20PM.png?raw=true)
### To test out if our remote server is working correctly, we can test out some commands. Common commands include:
### cd
### ls
### cat
### pwd
### To learn more about what these commands do, you can head to this [link](https://kb.iu.edu/d/afsk), but your terminal will display the directories used, and be correctly switching directories: ![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/command%20test.png?raw=true)