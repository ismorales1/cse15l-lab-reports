# Lab Report Three


All options used alongside ```grep```:
- ```grep -v``` 
- ```grep -c```
- ```grep -r```
- ```grep -h```


**Example #1 using ```grep``` with ```-v``` option:**

As you can see from the command below, the ```-v``` option for ```grep``` prints all the lines in the provided file that do not match the provided pattern. Therefore, this command can be useful for identifying files that do not contain a certain patter.

Command:``` grep -v "i" written_2/travel_guides/berlitz1/HandRHongKong.txt```

Output:
```
Recommended Hotels
$$$$above HK$2,500
$$$HK$l,600 to HK$2,500
$$HK$950 to HK$1,600
$below HK$950
```
**Example #2 using ```grep``` with ```-v``` option:**
In this example ```hotel``` is the provided pattern, therefore, any line in ```HandRHongKong.txt``` that does not match the pattern is printed into the terminal.

Command:```grep -v "hotels" written_2/travel_guides/berlitz1/HandRHongKong.txt```

Output:
```
Recommended Hotels
world, with representatives from all the major international chains.
Hotels listed below have full air-conditioning, offer 24-hour or
have excellent business services and conference facilities; many have
shopping malls.
Reservations are strongly recommended, particularly in
summer and at Christmas. If you do arrive without making advance
arrangements, the Hong Kong Hotel Reservation Center at the
International Airport will be happy to arrange accommodations for you
on your arrival.
As a basic guide, the symbols below have been used to
indicate high-season rates in Hong Kong dollars, based on double
major credit cards. A 10% service charge and 5% government tax will be
added to the bill.
$$$$above HK$2,500
$$$HK$l,600 to HK$2,500
$$HK$950 to HK$1,600
$below HK$950
```
**Example #3 using ```grep``` with ```-c``` option:**

The ```-c``` option for ```grep``` prints the number of occurrences that the pattern appears in the provided file or files. In the example below, one file was passed in, therefore, the number of occurrences of the pattern within that file is printed. 

Command:```grep -c "weather" written_2/non-fiction/OUP/Abernathy/ch2.txt```

Output: 
```
1
```
**Example #4 using ```grep``` with ```-c``` option:**

In the example below, multiple files were passed in, therefore, the pathway of the file along with the number of occurrences of the pattern within that file is printed. 

Command:```grep -c "weather" written_2/non-fiction/OUP/Abernathy/*.txt```

Output:
```
written_2/non-fiction/OUP/Abernathy/ch1.txt:0
written_2/non-fiction/OUP/Abernathy/ch14.txt:0
written_2/non-fiction/OUP/Abernathy/ch15.txt:0
written_2/non-fiction/OUP/Abernathy/ch2.txt:1
written_2/non-fiction/OUP/Abernathy/ch3.txt:1
written_2/non-fiction/OUP/Abernathy/ch6.txt:1
written_2/non-fiction/OUP/Abernathy/ch7.txt:0
written_2/non-fiction/OUP/Abernathy/ch8.txt:0
written_2/non-fiction/OUP/Abernathy/ch9.txt:0
```


**Example #5 using ```grep``` with ```-r``` option:**

In this example, ```-r``` allows the user to provide a directory. The files and the files within any subdirectories of the provided directory are then recursively searched to find any file withing the matches the provided pattern.

Command: ```grep -r "cold" written_2/non-fiction/OUP/Berk```

Output:
```
written_2/non-fiction/OUP/Berk/ch1.txt:This does not mean that a shy child should be forced into new situations with coldness, harshness, and impatience—tactics that magnify their dread of new and unpredictable events. Instead, parents who warmly, but consistently and assertively, require their inhibited child to try new experiences and guide and support them in doing so actually reduce the child’s physiological stress reactions, fostering a more adaptive style in the child. Indeed, adult eorts of this kind are believed to be largely responsible for the fact that about 70 percent of extremely inhibited babies cope with novelty more eectively as they get older (although practically none become highly sociable).
written_2/non-fiction/OUP/Berk/ch7.txt:Besides modeling destructive forms of interaction, parents who behave hurtfully toward each other generally interact hostilely with their children.35 They also tend to use inconsistent discipline—alternately strict and lax.36 When parents scold children on some occasions but permit them to act inappropriately on others, children are confused about how to behave and engage in especially high rates of disobedience.
written_2/non-fiction/OUP/Berk/ch7.txt:If parents experience intensifying sibling conﬂict, they may want to reevaluate their communication with each child. Warmth and frequent expressions of affection are associated with positive sibling interaction, whereas harshness and coldness are associated with sibling antagonism.41 Once established, this link between parent–child and sibling relationships is self-perpetuating. Warm parenting fosters considerate sibling interaction, which prompts positive parental communication in the future. When parents are hostile and coercive, children act similarly toward their siblings, and parental anger escalates.
```
**Example #6 using ```grep``` with ```-r``` option:**


# SOURCES!!!!!!!!
