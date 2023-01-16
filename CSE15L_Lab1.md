# CSE15L Lab 1 Report
## Step 1: CSE15L Account Setup
- Search for your CSE15L account here: *https://sdacs.ucsd.edu/~icc/index.php*
  - Log in to view your account, then you should be able to see your account name under **"Additional Accounts"**
  - Your account should like **"cse15l,"** followed by your account specific characters
- Reset your password ([*Tutorial*](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit))
  - ***Note: Follow instructions carefully and exactly, the website is glitchy***
  - Click your account name, then click the link highlighted as ***"change your password"***
  - Enter a new password according to the site's parameters, then click enter on your keyboard ***(Don't click check password, it doesn't work and will loop the password creation process.)***
  - You should get a page indicating that your password has successfully reset
  - When trying to finally login to connect remotely, input *"ssh ACCOUNT_NAME@ieng6.ucsd.edu"* into the terminal and type in your new password to check if you can log in successfully (type carefully since the inputs do not show up)
  - *View tutorial for further instruction and more specific help*
## Step 2: Visual Studio Code Setup
- If you already have VSCode installed on your own computer or you want to use the lab's computers, you can skip this step
- Visit the [*Visual Studio Code website,*](https://code.visualstudio.com/) which should look like this: 
![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%205.36.13%20PM.PNG)
  - Follow the instructions for your specified operating system (Mac or Windows). The download page should look like this:
![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%205.57.17%20PM.png)
- Once downloaded, open Visual Studio Code and it should look something like this: 
![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%206.01.19%20PM.png)
## Step 3: Connecting Remotely to CSE15L
- **If on Windows:**
  - Install [*Git for Windows*](https://gitforwindows.org/) ***(Allows terminal to look similar to in class examples + other useful tools)***
  - The page should look like this: ![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%207.45.07%20PM.png)
  - Follow [***these***](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) instructions to set up the correct terminal for VS Code use
- Now finally logging in remotely, open a terminal in VS Code ***(Ctrl or Command + `, or click Terminal then New Terminal by menu options)***
- Use the ***"ssh"*** command to log in using your username. It should look like this: ***"$ ssh cs15lwi23xx@ieng6.ucsd.edu"*** (The "$" sign is not part of the input, it is a denotation for a command. **The "x" part of the username should be replaced with your specified account name** )
- If it works correctly, your screen should look something like this:
![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%207.33.29%20PM.png)
- Input yes to continue logging in. You should be prompted to enter your password that you created earlier
- If you log in correctly, your screen should look like this: 
![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%207.43.23%20PM.png)
- After all this, you should now be successfully remotely connected to some computer in the CSE basement
## Step 4: Running Commands
- Test out some commands and just play around with them, try to understand what is happening
- Here is a list of some commands you can try:
  - cd
  - ls
  - pwd
  - mkdir
  - cp
  - cd ~
  - ls -lat
  - ls -a
  - ls <directory<directory>> (directories such as /home/linux/ieng6/cs15lwi23/cs15lwi23xxx *xxx replaced by another username's specified letters*)
- Running some of these commands may look like this: 
![Image](file:///Users/altairlanceaguelo/Desktop/Screen%20Shot%202023-01-15%20at%208.09.28%20PM.png)
- Command to log out: 
  - Press Ctrl + D, then input exit
