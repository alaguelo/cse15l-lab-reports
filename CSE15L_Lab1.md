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
  - When trying to finally login to connect remotely, input `ssh ACCOUNT_NAME@ieng6.ucsd.edu` into the terminal and type in your new password to check if you can log in successfully (type carefully since the inputs do not show up)
  - *View tutorial for further instruction and more specific help*
## Step 2: Visual Studio Code Setup
- If you already have VSCode installed on your own computer or you want to use the lab's computers, you can skip this step
- Visit the [*Visual Studio Code website,*](https://code.visualstudio.com/) which should look like this: ![vscode1](https://user-images.githubusercontent.com/122497078/212786380-a258f6b2-94cd-4d28-bbb8-9d99076e95ce.png)
  - Follow the instructions for your specified operating system (Mac or Windows). The download page should look like this: ![Screen Shot 2023-01-15 at 5 57 17 PM](https://user-images.githubusercontent.com/122497078/212786504-380b2fb1-8d8a-4de9-9aa2-723b34df0eb8.png)
- Once downloaded, open Visual Studio Code and it should look something like this: ![Screen Shot 2023-01-15 at 6 01 19 PM](https://user-images.githubusercontent.com/122497078/212786545-75185f50-b62e-4ffe-8543-0e888df9aa16.png)
## Step 3: Connecting Remotely to CSE15L
- **If on Windows:**
  - Install [*Git for Windows*](https://gitforwindows.org/) ***(Allows terminal to look similar to in class examples + other useful tools)***
  - The page should look like this: ![Screen Shot 2023-01-15 at 7 45 07 PM](https://user-images.githubusercontent.com/122497078/212786682-14043fbd-b11b-4f2d-bba9-e4bc5252aa25.png)
  - Follow [***these***](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) instructions to set up the correct terminal for VS Code use
- Now finally logging in remotely, open a terminal in VS Code ***(Ctrl or Command + `, or click Terminal then New Terminal by menu options)***
- Use the ***"ssh"*** command to log in using your username. It should look like this: `$ ssh cs15lwi23xx@ieng6.ucsd.edu` (The "$" sign is not part of the input, it is a denotation for a command. **The "x" part of the username should be replaced with your specified account name** )
- If it works correctly, your screen should look something like this:
![Screen Shot 2023-01-15 at 7 33 29 PM](https://user-images.githubusercontent.com/122497078/212786804-7af2b6f4-1399-4bf0-af16-38ca19ffd829.png)
- Input yes to continue logging in. You should be prompted to enter your password that you created earlier
- If you log in correctly, your screen should look like this: 
![Screen Shot 2023-01-15 at 7 43 23 PM](https://user-images.githubusercontent.com/122497078/212786856-633ba9c2-2962-47ac-af04-16f73d1b4214.png)
- After all this, you should now be successfully remotely connected to some computer in the CSE basement
## Step 4: Running Commands
- Test out some commands and just play around with them, try to understand what is happening
- Here is a list of some commands you can try:
  - `cd`
  - `ls`
  - `pwd`
  - `mkdir`
  - `cp`
  - `cd ~`
  - `ls -lat`
  - `ls -a`
  - `ls <directory<directory>>` (directories such as /home/linux/ieng6/cs15lwi23/cs15lwi23xxx *xxx replaced by another username's specified letters*)
- Running some of these commands may look like this: 
![Screen Shot 2023-01-15 at 8 09 28 PM](https://user-images.githubusercontent.com/122497078/212786895-63482d60-5f3d-427f-8dc9-b797fe30e0a0.png)
  - As you can see from this code, running the command `cd` allows you to change directories from within the terminal
  - `ls` lists the files of the directory you are currently in
  - `cd ~` changes the directory to the home directory
- Command to log out: 
  - Press Ctrl + D, then input exit
