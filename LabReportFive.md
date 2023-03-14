# Lab Report Five 
--------------------
During the week 3 lab, we were introduced to JUnit and its testing capabilities. We attempted to write some tests with the provided files in the lab3 
repository. However, apart from writing insightful tests for some of the files, it was difficult to directly identify the symptoms of some of the bugs. 
Therefore, I believe that using the Java command line debugger that we just learned, would be useful in order to troublelshoot and identify bugs quicker. 

----------------------------------------------------
One of the bugs in the LinkedList implementation was that the ```append()``` method enters an infinite loop:

<img width="1038" alt="Screen Shot 2023-03-13 at 7 46 42 PM" src="https://user-images.githubusercontent.com/122497830/224879981-bef2029e-2626-4c63-905f-300e3e251a39.png">

However, to gain more insight about the inifite loop, we can utilize the command line Java debugger. As you can see from the screenshot below, after
utilizing the command line debugger, we see that the linked list instance is initialized and the first two elements actually get appended. However,
when we run the 11th line, that is where we encounter the infinite loop. Now, we have more insight on when the bug occurs, which can lead to identifying
the bug.

<img width="771" alt="Screen Shot 2023-03-13 at 8 03 13 PM" src="https://user-images.githubusercontent.com/122497830/224882303-c7d687bb-e9ea-473e-acab-3e2afec90f3f.png">
