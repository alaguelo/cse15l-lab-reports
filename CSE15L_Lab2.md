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
![Screen Shot 2023-01-30 at 12 50 55 PM](https://user-images.githubusercontent.com/122497078/215592139-0bbb73bf-c8d2-4bd5-9cd4-bd7786cd6d80.png)

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
  




