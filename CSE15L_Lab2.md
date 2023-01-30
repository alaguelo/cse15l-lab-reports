# CSE15L Lab Report 2
## Part 1: StringServer
![Screen Shot 2023-01-29 at 10 43 37 PM](https://user-images.githubusercontent.com/122497078/215406513-e1a78b40-17fc-46f0-8a6f-a0f2864004ca.png)
![Screen Shot 2023-01-29 at 10 43 54 PM](https://user-images.githubusercontent.com/122497078/215406681-777c6217-91a4-4a61-a27c-afcc0eb38433.png)
![Screen Shot 2023-01-29 at 10 49 32 PM](https://user-images.githubusercontent.com/122497078/215407512-c06b0aa5-231a-44cf-9d99-0b4d7188f957.png)
![Screen Shot 2023-01-29 at 10 50 14 PM](https://user-images.githubusercontent.com/122497078/215407570-605fdb11-d28e-4de3-9582-5db45c8d6097.png)
- For each of my screenshots using `/add-message`, the `handleRequest` and `main` methods are called.
- For the `handleRequest` method, relevant arguments include the url and the path within the url. The values of these arguments are URI values for the
url, and string values for the path within the url. The main method takes in a string as an argument, of which it is a string value that describes a port
number for hosting the webserver.
- The URI value changes as the url that is passed through the `handleRequest` method changes. It depends on what the user types in as they visit the webserver.
The string value changes for the path within the url as users add different words to the webserver. Once the webserver is created, the string argument for 
the port number does not change, but for every webserver creation, the port number argument can be changed.
## Part 2: Lab 3 Bugged Reverse Array
-**Failure Inducing Input:**
```
@Test
public void testReverseInPlace2(){
  int[] input2 = {1,2,3,4,5};
  ArrayExamples.reverseInPlace(input2);
  assertArrayEquals(new int[]{5,4,3,2,1}, input2);
}
```
-**Non-Failure Inducing Input:**
```
@Test
public void testReverseInPlace(){
  int[] input3 = {3};
  ArrayExamples.reverseInPlace(input3);
   assertArrayEquals(new int[]{3}, input3);
```
-**Symptom:**
- Output of first test above:
![Screen Shot 2023-01-30 at 12 47 48 PM](https://user-images.githubusercontent.com/122497078/215591539-3ed30ee4-8d6d-4fb9-9110-2baff6c5a390.png)
- Output of second test above:
![Screen Shot 2023-01-30 at 12 50 55 PM](https://user-images.githubusercontent.com/122497078/215610908-ce8a9848-2db3-424c-89dd-e1c4ed2edb3d.png)

-**Bug Fix:**
-Before Fix:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
-After Fix:
```
static void reverseInPlace(int[] arr) {
    int temp = 0;
    for(int i = 0; i < arr.length/2; i += 1) {
      temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```
-Fix: The issue with the first code was that, because the code was trying to reverse the array only using one array, when getting to the latter half of the
array, the indices after the midpoint would be assigned to the updated array in the front half of the array. For example, in an array of {1,2,3,4,5}. reversing it with the first code block would return {5,4,3,4,5}. To fix this, as seen in the updated code, a temporary variable is needed to hold the element of the index you are at. Doing this, you could update the array so that it would hold the correct values after each update, assigning each element to the correct index.
## Part 3: What I Learned
One thing I took away from the past two labs is how to debug efficiently. A big part of debugging efficiently is having a good mindset toward the code. I learned that when looking at my code, having a positive attitude will help me debug and create a better working code, helping me attain that "professional" level of "correctness," as I want my code to work and work well. For example, last quarter, I found myself rushing through my PAs, not really trying to understand what was wrong with it, but changing a few things trying to see if it would be correct when I turned it in. Going through this lab, I was taken step by step through debugging, in which I feel I helped me understand what steps I could take, and having it as a guide made me feel better about debugging in general. I know now that looking at the code as a whole and trying to fully understand it while writing tests for it, which I also need to understand, is the way to go, as it forces me to fully know what I am doing. I now know that coding is a process that is better taken slow, for me at least, rather than trying things that when i don't understand what is going on.
