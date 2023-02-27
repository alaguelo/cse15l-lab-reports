# CSE15L Lab Report 4
## Step 4: Log Into ieng6
![image](https://user-images.githubusercontent.com/122497078/221502520-d06b00be-0a51-47b6-965e-fe2165abe0be.png)

First, I typed in ```ctrl + r``` to open up the reverse search within the terminal. Then, I typed in ```cs``` to bring up possible commands that should have my username
in them. This brought up the command ```ssh cs15lwi23ane@ieng6.ucsd.edu```. After that, I clicked ```<enter>``` to input the command. Then, I inputted my password and clicked
```<enter>``` again to successfully log me in.

## Step 5: Clone fork of repository to my GitHub account
![image](https://user-images.githubusercontent.com/122497078/221506345-153a3dfb-744c-4cde-bdc3-9e30310439f4.png)

To clone the fork of the repository of lab7 that I made, I inputted ```git clone git@github.com:alaguelo/lab7.git``` and ```<enter>```. I used the SSH key I created in class to make this
process easier.

## Step 6: Running Tests
![image](https://user-images.githubusercontent.com/122497078/221508238-9c155904-6ff7-4f9c-bcc0-05d37d463b86.png)

To run the tests, first I changed directories into the newly cloned lab 7 using ```cd lab7``` and ```<enter>```. To compile the testers I clicked the ```<up>``` arrow 22 times to 
find this command: ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```, then clicked ```<enter>``` to compile. I then clicked the ```<up>``` arrow 21 times to
find this command: ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```, then clicked ```<enter>``` to run the 
tests.

## Step 7: Editing the Code
![image](https://user-images.githubusercontent.com/122497078/221513217-a6d2e0ee-55d5-46b0-9ffc-5725e60ae070.png)
![image](https://user-images.githubusercontent.com/122497078/221513071-daf949a0-291a-45c0-8323-971d6ed69f48.png)


To fix my error, I inputted the command ```nano L<tab>.j<tab>```. It looks like ```nano ListExamples.java```. 
To scroll down to fix the error, I clicked ```<down>``` 42 times. Then I clicked ```<right>``` 12 times to go to the part I needed to fix. I used ```<delete>``` to delete the error
then typed ```<2>``` to fix it. I then typed ```ctrl + o``` and ```<enter>``` to save my changes, then ```ctrl + x``` to exit back into the terminal.

## Step 8: Rerunning Tests
![image](https://user-images.githubusercontent.com/122497078/221514819-e9d97c06-a689-42e5-b268-653cf32d223a.png)


To rerun the tests, I first recompiled by pressing ```<up>``` 4 times then ```<enter>``` since I had just compiled. To run the test again, I pressed ```<up>``` 3 times, then ```<enter>```.

## Step 9: Committing and Pushing Changes
![image](https://user-images.githubusercontent.com/122497078/221515278-c764a9f3-3492-4bcf-9efa-24113ced3278.png)

To commit and push the changes, I first inputted ```git add L<tab>.j<tab>```. I then used the command ```git commit -m "Update"```. I inputted the "Update" part so I could
see if the update happened correctly. Since I already have an SSH key, it committed and pushed all at once easier. 

