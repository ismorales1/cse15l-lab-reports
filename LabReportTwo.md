# Lab Report Two: Servers and Bugs

The screenshot below reveals the code to ```StringServer```:
<img width="808" alt="Screen Shot 2023-02-12 at 4 17 58 PM" src="https://user-images.githubusercontent.com/122497830/218345971-3ac200ff-c485-44ef-930a-84d6b134af80.png">



<img width="1161" alt="Screen Shot 2023-02-12 at 4 19 35 PM" src="https://user-images.githubusercontent.com/122497830/218346090-76fe45c3-64e9-443f-8144-98fe4c027d0a.png">

Initially, the `handleRequest()` method gets invoked with the provided URL input. In this example the input was ```localhost:45992/add-message?s=hello``` and the later input was `localhost:45992/add-message?s=It is cloudy today`. Further, the path of the provided input is checked and verifies if the ```add-message``` path was provided. This was computed through the use of the ```getPath()``` and the ```contains()``` methods. After, the query is divided into two elements and stored into a string array using the ```split()``` method. If the 0th index element is ```"s"```, then a proper string was provided, which will be printed onto the webpage. Next, the 1st index element of the string array, which is the deisred string to be printed onto the webpage, is assigned to a local variable, which is then concatenated with a global variable that will hold the entire sequence of strings. 

<img width="661" alt="Screen Shot 2023-02-12 at 4 21 18 PM" src="https://user-images.githubusercontent.com/122497830/218346198-8e5ab9db-912f-4e0e-a697-db896b6532e0.png">

