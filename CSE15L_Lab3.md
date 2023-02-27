# CSE15L Lab Report 3
## grep -i
```
grep -i abernathy results.txt
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt

```
grep -i allows the user of the terminal to search for a specific word with case insensitivity. This is useful because it makes it easier to find all instances of the word,
regardless of its upper or lower cases. In the example above, in a results text file that has all of the path directories that includes a text file, it was easy to find which
of these paths included the word "Abernathy," even though I used lowercase. 
```
grep -r abernathy results.txt
```
As you can see from this example, if you try to find the word "Abernathy" with another grep command, and do not use -i, the search is case sensitive, and does not find the
file that you were looking for.
## grep -H
grep -H allows the user of the terminal to search for a specific word, and return an output that shows which files that word can be found in, the name of those files,
and each of their outputs. This is useful for if you want to both search for a word, the file and its name that it is in, and the contents of each file.
### Example 1:
```
grep -H Abernathy results.txt
results.txt:written_2/non-fiction/OUP/Abernathy
results.txt:written_2/non-fiction/OUP/Abernathy/ch1.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch14.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch15.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch2.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch3.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch6.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch7.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch8.txt
results.txt:written_2/non-fiction/OUP/Abernathy/ch9.txt
```
In this example, when looking for the term "Abernathy," it finds that the keyword is located in the results.txt file and displays all the instances in which it comes up, which is helpful for viewing. 

### Example 2:
```
grep -H Berk results.txt
results.txt:written_2/non-fiction/OUP/Berk
results.txt:written_2/non-fiction/OUP/Berk/ch1.txt
results.txt:written_2/non-fiction/OUP/Berk/ch2.txt
results.txt:written_2/non-fiction/OUP/Berk/CH4.txt
results.txt:written_2/non-fiction/OUP/Berk/ch7.txt
```
In this example, when looking for the term "Berk," it finds that the keyword is located in the results.txt file and displays all the instances in which it comes up, which is helpful for viewing. In this case, the viewer can see that "Berk" is less prevalent than "Abernathy"
## grep -c
grep -c allows the user to check how many times a word or input comes up within the file that you search. This is useful to check for how many times an input or a word
is mentioned. In each example below, check how it matches how many lines there are above.
### Example 1:
```
grep -c Abernathy results.txt
10
```
Matching the example above, "Abernathy" is accounted for 10 times within the file. 

### Example 2: 
```
grep -c Berk results.txt
5
```
Matching the second example above, "Berk" is accounted for 5 times within the file.

## grep --color
grep --color allows the user of the terminal to search for an instance of the input or word, and highlight the input with a color within its context. This is useful as
the highlight makes it easy to view and check where the input is within your search. 
### Example 1:
```javascript
grep --color Abernathy results.txt 
written_2/non-fiction/OUP/==Abernathy==
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
```
![image](https://user-images.githubusercontent.com/122497078/218635079-556008c0-06c5-4db3-8830-18b7c33cd9c5.png)

As seen above, the term "Abernathy" is highlighted, showing that grep --color makes it easier to see you desired search term.

### Example 2: 
```javascript
grep --color Berk results.txt
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
```
![image](https://user-images.githubusercontent.com/122497078/218635196-b18ad135-cd4a-4338-a1fd-ccb3b58a2e06.png)

As seen above, the term "Berk" is highlighted, also showing that grep --color makes it easier to see you desired search term.

## Sources:
```
https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/
https://stackoverflow.com/questions/35465557/how-to-apply-color-on-text-in-markdown#:~:text=Markdown%20doesn't%20support%20color,*%20text.&text=As%20the%20original%2Fofficial%20syntax,for%20writing%20for%20the%20web.
```
