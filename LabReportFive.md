# Lab Report Five 
--------------------
For lab 3 and part 2 of the 2nd Lab Report, we were introduced to JUnit and its testing capabilities. We attempted to write some tests with the provided files in the lab3 repository. However, apart from writing insightful tests for some of the files, it was difficult to directly identify the symptoms/failure-inducing input for some of the bugs. Therefore, I believe that using the Java command line debugger that we just learned, would be useful in order to troublelshoot and identify bugs quicker. 

----------------------------------------------------
One of the bugs in the LinkedList implementation was that the ```append()``` method entered an infinite loop:

<img width="583" alt="Screen Shot 2023-03-13 at 9 10 20 PM" src="https://user-images.githubusercontent.com/122497830/224891001-644440d2-d2c0-4426-878c-7730528e60b4.png">

JUnit testing method:

<img width="604" alt="Screen Shot 2023-03-13 at 8 36 34 PM" src="https://user-images.githubusercontent.com/122497830/224886832-5529cc53-a17f-4f66-9d5c-f9cfd99840a1.png">

Test failing:

<img width="1038" alt="Screen Shot 2023-03-13 at 7 46 42 PM" src="https://user-images.githubusercontent.com/122497830/224879981-bef2029e-2626-4c63-905f-300e3e251a39.png">

----------------------------------------------------
However, to gain more insight about the infinite loop, we can utilize the command line Java debugger. First, I need to compile and run the Java debugger with respect to the LinkedList testing file:

<img width="728" alt="Screen Shot 2023-03-13 at 9 13 29 PM" src="https://user-images.githubusercontent.com/122497830/224891448-1bd7de30-3ed5-44be-9614-54571c565a38.png">


----------------------------------------------------
As you can see from the screenshot below, after utilizing the command line debugger, we see that the linked list instance is initialized and the first two elements actually get appended. We know this because we run the 8th, 9th, and 10th line of the testing method one by one. This is achievable through the deubgger by utilizing the ```next``` command, which runs an individual line of code. Also, the ```stop at``` command was utilized in order to run multiple individual lines, without running the entire program. 

<img width="1077" alt="Screen Shot 2023-03-13 at 9 15 03 PM" src="https://user-images.githubusercontent.com/122497830/224891675-2f2946c6-eae4-4a8c-afbe-4200708ef5f0.png">

----------------------------------------------------
However, when we run the 11th line, this is where we encounter the infinite loop. Now, we have more insight on when the bug occurs, which can lead to identifying the bug quicker. 

<img width="1095" alt="Screen Shot 2023-03-13 at 9 17 23 PM" src="https://user-images.githubusercontent.com/122497830/224891953-2ef39b98-b87d-4f9e-8856-a563bfad6371.png">

Also, we now have a stronger idea of what the failure inducing input is for this particular method, which is, appending more than two elements. Further, we also gained insight as to what is not failure inducing input, and for this case, it's appending 2 or less elements to a linked list. 
