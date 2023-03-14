# Lab Report Five 
--------------------
For lab 3 and part 2 of Lab Report 2, we were introduced to JUnit and its testing capabilities. We attempted to write some tests with the provided files in the lab3 repository. However, apart from writing insightful tests for some of the files, it was difficult to directly identify the symptoms/failure-inducing input for some of the bugs. Therefore, I believe that using the Java command line debugger that we just learned, would be useful in order to troublelshoot and identify bugs quicker. 

----------------------------------------------------
One of the bugs in the LinkedList implementation was that the ```append()``` method enters an infinite loop:

<img width="1038" alt="Screen Shot 2023-03-13 at 7 46 42 PM" src="https://user-images.githubusercontent.com/122497830/224879981-bef2029e-2626-4c63-905f-300e3e251a39.png">

However, to gain more insight about the inifite loop, we can utilize the command line Java debugger. As you can see from the screenshot below, after
utilizing the command line debugger, we see that the linked list instance is initialized and the first two elements actually get appended. However,
when we run the 11th line, that is where we encounter the infinite loop. Now, we have more insight on when the bug occurs, which can lead to identifying
the bug.

<img width="771" alt="Screen Shot 2023-03-13 at 8 03 13 PM" src="https://user-images.githubusercontent.com/122497830/224882303-c7d687bb-e9ea-473e-acab-3e2afec90f3f.png">

<img width="604" alt="Screen Shot 2023-03-13 at 8 36 34 PM" src="https://user-images.githubusercontent.com/122497830/224886832-5529cc53-a17f-4f66-9d5c-f9cfd99840a1.png">

-----------------------------------------------------------------------

In the method ```sumEvenIndices()```, there was a bug that was only invoked through certain input. Apart from the information that JUnit provided, the
Java debugger also provided further context about the bug. As you can see from the code below, unusual behavior occurs when an index position is out
of bounds. The ```input1 ``` variable is supposed to be assigned to an integer that summed all of the numbers at even indices. However, after running the 
8th line, there is weird behavior occuring, which may allow the user to imply that an index related bug is occurring. 

<img width="938" alt="Screen Shot 2023-03-13 at 8 35 24 PM" src="https://user-images.githubusercontent.com/122497830/224886671-901b16a4-bf99-4d03-93b4-319e9ad4999d.png">

<img width="640" alt="Screen Shot 2023-03-13 at 8 35 45 PM" src="https://user-images.githubusercontent.com/122497830/224886730-72ee0a92-76ea-4d9e-9ab7-8c6f4b076ff1.png">

-----------------------------------------------------------------------
From the image below, you can see that the ```averageWithoutLowest()``` method is tested, but gives the wrong output. When using the command line debugger, information is provided, however, it may be confusing and it differs from the JUnit output. In the second image below, you can see that after running lines 39-41, the output does not provide insightful information about ```doubList``` variable. Eventually, it claims that the doubList varibale Therefore, 

<img width="469" alt="Screen Shot 2023-03-13 at 8 49 34 PM" src="https://user-images.githubusercontent.com/122497830/224888556-59105855-ebbd-4bd3-b45b-ce31c7b8dc93.png">


<img width="867" alt="Screen Shot 2023-03-13 at 8 44 49 PM" src="https://user-images.githubusercontent.com/122497830/224887959-34e20860-b892-4104-90a9-1e7fd0a9bffd.png">
