# CSE15L Lab Report 5
## Redoing Lab 3: Researching the command ```find```
The ```find``` command allows a user to search through file heirarchies, helping the user find specific files or directories.
This command is useful for searching for these files and allowing the user to do with them as needed.

## ```find -empty```
The command ```find -empty``` lets the user search for a files or directories that are empty. An empty file or directory would
have no data as a file, or no subdirectories or files as a directory. This command is useful because it shows directories or 
files that are not really in use, which can be deleted or edited as needed.

### Example 1: 
``` 
find non-fiction/ -empty
non-fiction//OUP/Abernathy/ch0.txt
```
For this example, I used the ```find -empty``` command to search for any empty files or subdirectories within the 
```non-fiction/``` directory. Using this command, I found that within the ```non-fiction/``` directory, a pathway is found that
has an empty file. This command shows the pathway of that empty file, showing the user, or me, that within ```non-fiction/```,
the directories ```//OUP/Abernathy/``` holds an empty ```ch-.txt``` file. Seeing this and how this file is not in use, I can
delete it as needed, whether it be for space or simply because it has no use.

### Example 2:
```
find written_2/ -empty
written_2//grep.txt
```
In this example, I wrote in the command ```find written_2/ -empty``` to check for empty files in this directory. This
find command found that in ```written_2/```,  the file ```grep.txt``` is empty. I could delete this as well file since it is 
not really in use.

## ```find -type```
The command ```find -type``` lets the user search for files of a specific type. This command allows the user to search for files
such as regular files with ```find -type f```, directories with ```find -type d```, and links with find -type l```. It is
useful for even further specification when searching.

### Example 1:
```
find written_2/ -type f -name "*.txt"
written_2//non-fiction/OUP/Berk/ch2.txt
written_2//non-fiction/OUP/Berk/ch1.txt
written_2//non-fiction/OUP/Berk/ch4.txt
written_2//non-fiction/OUP/Berk/ch7.txt
written_2//non-fiction/OUP/Abernathy/ch2.txt
written_2//non-fiction/OUP/Abernathy/ch3.txt
written_2//non-fiction/OUP/Abernathy/ch1.txt
written_2//non-fiction/OUP/Abernathy/ch7.txt
written_2//non-fiction/OUP/Abernathy/ch6.txt
written_2//non-fiction/OUP/Abernathy/ch8.txt
written_2//non-fiction/OUP/Abernathy/ch9.txt
written_2//non-fiction/OUP/Abernathy/ch15.txt
written_2//non-fiction/OUP/Abernathy/ch14.txt
```
In the example above, I used the command ```find written_2/ -type f -name "*.txt"``` so that I could find all files that were a
text file within the ```written_2/``` directory. As you can see, it was helpful in displaying all the files that had text.

### Example 2:
```
find written_2/ -type d -name "travel_guides" 
written_2//travel_guides
```
In this example, I used the ```find -type d``` iteration of the ```find -type``` command, using it to search for a specific
directory within the ```written_2/``` directory. It returned to me the only directory under ```written_2/``` which had the
name I specified, which was useful in showing me that there was only one directory of ```travel_guides/```.

## ```find -name```
The command ```find_name``` allows users to search for files under a specific name. It searches through directories
to return if any of the files that match the specified search. This command is useful for when the user knows exactly what file they are looking for. 

### Example 1:
```
find written_2/ -name "ch1.txt"
written_2//non-fiction/OUP/Berk/ch1.txt
written_2//non-fiction/OUP/Abernathy/ch1.txt
written_2//non-fiction/OUP/Rybczynski/ch1.txt
written_2//non-fiction/OUP/Kauffman/ch1.txt
written_2//non-fiction/OUP/Fletcher/ch1.txt
```
Above, I wanted to search for files that had the name ```ch1.txt``` under the ```written_2/``` directory. Using this command
I was able to find that there were 5 files under this directory that shared this name, meaning that there were five
different chapter ones that I could read through. 

### Example 2:
```
find written_2/ -name "*.txt"
written_2//non-fiction/OUP/Berk/ch2.txt
written_2//non-fiction/OUP/Berk/ch1.txt
written_2//non-fiction/OUP/Berk/CH4.txt
written_2//non-fiction/OUP/Berk/ch7.txt
written_2//non-fiction/OUP/Abernathy/ch2.txt
written_2//non-fiction/OUP/Abernathy/ch3.txt
written_2//non-fiction/OUP/Abernathy/ch1.txt
written_2//non-fiction/OUP/Abernathy/ch7.txt
written_2//non-fiction/OUP/Abernathy/ch6.txt
written_2//non-fiction/OUP/Abernathy/ch8.txt
written_2//non-fiction/OUP/Abernathy/ch9.txt
written_2//non-fiction/OUP/Abernathy/ch15.txt
written_2//non-fiction/OUP/Abernathy/ch14.txt
written_2//non-fiction/OUP/Rybczynski/ch2.txt
written_2//non-fiction/OUP/Rybczynski/ch3.txt
written_2//non-fiction/OUP/Rybczynski/ch1.txt
```
If I wanted to find every text file inside ```written_2/``` instead, I could search for the pattern name ```*.txt```, as I did
above. As you can see, it gave me every file matching the ```*.txt``` pathway, which would be useful for if I wanted to 
check which files I could access to read in these circumstances.

## ```find -mtime```
This command lets users search for files or directories that were augmented within a certain amount of time specified by the user. This would
be useful for checking updates to these files or directories, allowing the user to create a timeline of when these files
changed, or seeing if any command they ran actually changed the files they were working with. This command can also be used
alongside the ```find -type``` command to check even more specifically.

### Example 1:
```
find written_2/ -mtime -7 -type f 
written_2//grep.txt
```
If I wanted to find a file that had been modified inside ```written_2/``` within seven days for example, I would use
```find written_2/ -mtime -type f```. As you can see, since I was the one who created the grep.txt file and accessed it 
to view all of the files within these directories, it can be seen that it was modified within the past seven days.

### Example 2:
```
find written_2/ -mtime -7 -type d
written_2/
written_2//non-fiction
written_2//non-fiction/OUP
written_2//non-fiction/OUP/Berk
written_2//non-fiction/OUP/Abernathy
```
If I wanted to view directories inside ```written_2/``` that had been modified in the last week, I could call the same
command above but change the type I search to directory. In this example, since I accessed these directories during the lab, 
the command returns the directories I changed in the past week.

## Sources
```
- ChatGPT
- https://www.diskinternals.com/linux-reader/bash-find-command/
```
