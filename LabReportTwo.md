# Lab Report Two: Servers and Bugs

Part 1:
-------
The screenshot below reveals the code to ```StringServer```:
<img width="808" alt="Screen Shot 2023-02-12 at 4 17 58 PM" src="https://user-images.githubusercontent.com/122497830/218345971-3ac200ff-c485-44ef-930a-84d6b134af80.png">



<img width="1161" alt="Screen Shot 2023-02-12 at 4 19 35 PM" src="https://user-images.githubusercontent.com/122497830/218346090-76fe45c3-64e9-443f-8144-98fe4c027d0a.png">

Initially, the `handleRequest()` method gets invoked with the provided URL input. In this example the input was ```localhost:45992/add-message?s=hello``` and the later input was `localhost:45992/add-message?s=It is cloudy today`. Further, the path of the provided input is checked and verifies if the ```add-message``` path was provided. This was computed through the use of the ```getPath()``` and the ```contains()``` methods. After, the query is divided into two elements and stored into a string array using the ```split()``` method. If the 0th index element is ```"s"```, then a proper string was provided, which will be printed onto the webpage. Next, the 1st index element of the string array, which is the deisred string to be printed onto the webpage, is assigned to a local variable, which is then concatenated with a global variable that will hold the entire sequence of strings. Therefore, when the second url input,`localhost:45992/add-message?s=It is cloudy today` is provided, the local variable `strTemp` will hold and later concatenate `"It is cloudy today"` with any previous strings that were provided earlier to be printed onto the webpage.

<img width="661" alt="Screen Shot 2023-02-12 at 4 21 18 PM" src="https://user-images.githubusercontent.com/122497830/218346198-8e5ab9db-912f-4e0e-a697-db896b6532e0.png">

The `handleRequest()` method is invoked again with the url, ```localhost:45992/add-message?s=hi```. This method also gets invoked another four times where the inputs and query is: ```s=Today is very sunny```, ```s=There is also no traffic today```, ```s=It is a good day today```, and ```s=San Diego is cool```. This means that after the provided url is handled, the global variable ```entireSequ``` gets updated five times and each new string gets concatenated to the existing sequence of strings. Each time that a new query is provided in the url, the ```entireSequ``` global variable gets updated and the corresponding sequence of strings gets printed onto the webpage. Also, a new line is provided after each new input, allowing each new subset of strings to appear below the previous strings provided in the query.
 
Part 2:
-------

Failure inducing input for the ```append()``` method in the LinkedListExample.java program (as a JUnit test):
```
@Test
public void linkedListAppendTester(){
 LinkedList pracList = new LinkedList();
 pracList.append(4);
 pracList.append(8);
 pracList.append(7);

 assertEquals("4 8 7 ", pracList.toString());
}
```
Input for the ```append()``` method in the LinkedListExample.java program that does not induce a failure (as a JUnit test):
```
@Test
public void linkedListAppendTesterTwo(){
 LinkedList secondList = new LinkedList();
 secondList.append(9);
 secondList.append(2);

 assertEquals("9 2 ", secondList.toString());
}
```
Screenshot of symptom and output of running program with Failure inducing input/test:
<img width="985" alt="Screen Shot 2023-02-12 at 7 28 14 PM" src="https://user-images.githubusercontent.com/122497830/218363835-63d15388-a974-47ab-be3a-b4368249777c.png">

Screenshot of symptom and output of running program with non-failing inducing input/test:
<img width="988" alt="Screen Shot 2023-02-12 at 7 29 35 PM" src="https://user-images.githubusercontent.com/122497830/218363994-6b3be0ec-ef62-47ad-b908-e8f60ee9f417.png">

Fixing code:

Before fixing ```append()``` method:
```
public void append(int value) {
 if(this.root == null) {
  this.root = new Node(value, null);
  return;
 }
 // If it's just one element, add if after that one
 Node n = this.root;
 if(n.next == null) {
  n.next = new Node(value, null);
  return;
 }
 // Otherwise, loop until the end and add at the end with a null
 while(n.next != null) {
  n = n.next;
  n.next = new Node(value, null);
 }
}

```

After fixing ```append()``` method:
```
public void append(int value) {
 if(this.root == null) {
  this.root = new Node(value, null);
  return;
 }
 // If it's just one element, add if after that one
 Node n = this.root;
 if(n.next == null) {
  n.next = new Node(value, null);
  return;
 }
 // Otherwise, loop until the end and add at the end with a null
 while(n.next != null) {
  n = n.next;
 }
 n.next = new Node(value, null);
}

```
Fix Explanation: Before fixing the ```append()``` method, the program would enter an infinite loop each time one wanted to append a new node with a linked list of size 3 or greater. This was caused by the line ```n.next = new Node(value, null);``` being in the wrong block of code. A new node would be created during each iteration of the while loop, resulting in never finding the last node whose next refernce variable is pointing to null. To fix this, I put the same line of code, ``` n.next = new Node(value, null);``` , outside of the while loop. This allows the while loop to reach the last node, such that a new node can then be appended as expected. 

Part 3:
-------

I learned how to utilize certain git commands and features such as git clone or forking. Further, I learned how to utilize JUnit in order to identify bugs and flaws in my program. Also, I learned how to initiate a server and write code in order to handle certain input from a segment of URLs.




