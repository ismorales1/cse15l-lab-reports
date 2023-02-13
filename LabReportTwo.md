# Lab Report Two: Servers and Bugs

The screenshot below reveals the code to ```StringServer```:
<img width="808" alt="Screen Shot 2023-02-12 at 4 17 58 PM" src="https://user-images.githubusercontent.com/122497830/218345971-3ac200ff-c485-44ef-930a-84d6b134af80.png">



<img width="1161" alt="Screen Shot 2023-02-12 at 4 19 35 PM" src="https://user-images.githubusercontent.com/122497830/218346090-76fe45c3-64e9-443f-8144-98fe4c027d0a.png">

Initially, the `handleRequest()` method gets invoked with the provided URL input. In this example the input was ```localhost:45992/add-message?s=hello``` and the later input was `localhost:45992/add-message?s=It is cloudy today`. Further, the path of the provided input is checked and verifies if the ```add-message``` path was provided. This was computed through the use of the ```getPath()``` and the ```contains()``` methods. After, the query is divided into two elements and stored into a string array using the ```split()``` method. If the 0th index element is ```"s"```, then a proper string was provided, which will be printed onto the webpage. Next, the 1st index element of the string array, which is the deisred string to be printed onto the webpage, is assigned to a local variable, which is then concatenated with a global variable that will hold the entire sequence of strings. Therefore, when the second url input,`localhost:45992/add-message?s=It is cloudy today` is provided, the local variable `strTemp` will hold and later concatenate `"It is cloudy today"` with any previous strings that were provided earlier to be printed onto the webpage.

<img width="661" alt="Screen Shot 2023-02-12 at 4 21 18 PM" src="https://user-images.githubusercontent.com/122497830/218346198-8e5ab9db-912f-4e0e-a697-db896b6532e0.png">

The `handleRequest()` method is invoked again with the url, ```localhost:45992/add-message?s=hi```. This method also gets invoked another four times after with inputs where the query is: ```s=Today is very sunny```, ```s=There is also no traffic today```, ```s=It is a good day today```, and ```s=San Diego is cool```. This means that after the provided url is handled, the global variable ```entireSequ``` gets updated five times total where each new string gets concatenated to the existing sequence of strings. 
