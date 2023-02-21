# Lab Report Three


All options used for the command ```grep```:
- ```grep -v``` 
- ```grep -c```
- ```grep -r```
- ```grep -h```


**Example #1 using ```grep``` with ```-v``` option:**

As you can see from the command below, the ```-v``` option for ```grep``` prints all the lines in the provided file that do not match the provided pattern. Therefore, this command can be useful for identifying files that do not contain a certain pattern.

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
-----------------------------------------------------
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

In this example, the ```-r``` option allows the user to provide a directory. The files within the directory and any subdirectories are then recursively searched to find any file that matches the pattern. 

Command: ```grep -r "cold" written_2/non-fiction/OUP/Berk```

Output:
```
written_2/non-fiction/OUP/Berk/ch1.txt:This does not mean that a shy child should be forced into new situations with coldness, harshness, and impatience—tactics that magnify their dread of new and unpredictable events. Instead, parents who warmly, but consistently and assertively, require their inhibited child to try new experiences and guide and support them in doing so actually reduce the child’s physiological stress reactions, fostering a more adaptive style in the child. Indeed, adult eorts of this kind are believed to be largely responsible for the fact that about 70 percent of extremely inhibited babies cope with novelty more eectively as they get older (although practically none become highly sociable).
written_2/non-fiction/OUP/Berk/ch7.txt:Besides modeling destructive forms of interaction, parents who behave hurtfully toward each other generally interact hostilely with their children.35 They also tend to use inconsistent discipline—alternately strict and lax.36 When parents scold children on some occasions but permit them to act inappropriately on others, children are confused about how to behave and engage in especially high rates of disobedience.
written_2/non-fiction/OUP/Berk/ch7.txt:If parents experience intensifying sibling conﬂict, they may want to reevaluate their communication with each child. Warmth and frequent expressions of affection are associated with positive sibling interaction, whereas harshness and coldness are associated with sibling antagonism.41 Once established, this link between parent–child and sibling relationships is self-perpetuating. Warm parenting fosters considerate sibling interaction, which prompts positive parental communication in the future. When parents are hostile and coercive, children act similarly toward their siblings, and parental anger escalates.
```
**Example #6 using ```grep``` with ```-r``` option:**

In this example, the subdirectory ```/OUP``` is provided, therefore, it is recursively searched and any file within that matches the pattern is displayed. This means that any file and any subdirectory files in ```/OUP```are printed onto the terminal if they match the pattern.

Command: ```grep -r "spawned" written_2/non-fiction/OUP```

Output: 
```
written_2/non-fiction/OUP/Abernathy/ch2.txt:For the United States this brings us back to Samuel Slater, “father of American manufactures.” By 1810, the Pawtucket, Rhode Island, enterprise begun with Slater’s cunning had spawned a vibrant cotton-spinning industry throughout New England. The next step in developing a U.S.-based industry was to bring the machine that took yarn and transformed it into finished cloth—the power loom—across the Atlantic. This feat was accomplished in much the same way that Slater brought cotton spinning to the United States, through the agency of a crafty Boston merchant, Francis Cabot Lowell. As business historian Robert Dalzell notes,
written_2/non-fiction/OUP/Kauffman/ch3.txt:Some wellspring of creation, lithe in the scattered sunlight of an early planet, whispered something to the gods, who whispered back, and the mystery came alive. Agency was spawned. With it, the nature of the universe changed, for some new union of matter, energy, information, and something more could reach out and manipulate the world on its own behalf. Selfish? Yes. But how does matter, energy, information, and something else miraculous become selfish? From that miracle grew a biosphere = and, we must surmise, from that grow other biospheres, scattered seeds and gardens across the cosmos.
```

**Example #7 using ```grep``` with ```-h``` option:**

In this example, the ```-h``` option is utilized, which displays the line in the provided file that matches the pattern. However, it does this without displaying the file name, meaning, only the line from the file is displayed. This can be utilized for output or input redirection.

Command: ```grep -h "encryption" written_2/non-fiction/OUP/Abernathy/*.txt```

Output:
```
A number of developments, many linked to issues we have discussed, indicate both the potential and limitations of electronic retailing. In one sense, the Internet offers opportunities akin to mail-order retailing for playing a very lean game. For example, Lands’ Ends became an early leader in adopting certain lean retailing elements into its catalog operations and has aggressively entered Internet retailing. This retailer launched its Web site in 1995, the first major apparel retailer to do so. Its site incorporates an encryption system to protect customers against credit-card thefts.46
```

**Example #8 using ```grep``` with ```-h``` option:**

In this example, the lines that contain the pattern are displayed, but not the multiple file names.

Command:```grep -h "skylights" written_2/non-fiction/OUP/*/*.txt```

Output: 
```
One might assume that just as the highest-rated cars—Mercedes-Benz, BMW, Lexus—represent the highest standards of automobile technology, the most admired architecture would be the best built. This was generally true in the past, but in the twentieth century, when new materials and new aesthetic theories often have driven architects to cavalier experimentation, even celebrated architects have fallen short in that department. Le Corbusier’s white suburban villas, for example, were crudely finished in cement plaster on top of brick, and since the architect usually ignored (for aesthetic reasons) intrusive metal flashing and coping strips, the crude “machines for living” often aged poorly. Some Frank Lloyd Wright buildings have leaky skylights, sagging overhangs, and defective heating systems. This does not make them any less delightful to visit, but it must make them considerably less delightful to inhabit. Perhaps the most dramatic example of failed experimentation in recent years is the Centre Georges Pompidou in Paris, which opened in 1977. The building was widely praised for its architectural innovation—the British periodical Architectural Design called it “a seminal building of the Modern Movement.” The architects Renzo Piano and Richard Rogers turned the building literally inside-out. They dramatically hung pipes, ducts, fire stairs, elevators, and escalators from the exterior structure. These previously hidden elements were now exposed in plain sight—and exposed to the elements. The result might have been foreseen: after only twenty years, the French government was obliged to close the building for a two-year renovation. Although the authorities maintained that the renovation was required because of the unexpectedly large number of visitors, according to Le Monde almost half of the $90 million budget was spent on refurbishing the façade.
A number of years ago I accompanied the architect Jack Diamond on a visit to a building that he had just completed at York University in Toronto. It was a student center, containing a food court and lounges on the main level and student organization offices on the second floor. The exterior of the building was decidedly traditional. Facing a landscaped common, the well-proportioned façade consisted of a colonnaded brick base supporting a row of double columns capped by a deep copper-lined cornice. Behind the colonnade, which was fitted with retractable glass panels that could be opened during warm weather, was a two-story-high hall lit by three large skylights. The exterior had a simplicity that reminded me of McKim, Mead & White, albeit without Classical ornament.
```

----
## Sources:
[ChatGpt Link](https://openai.com/blog/chatgpt/) : 
This is where I discovered the options ```-v``` and ```-c```

[geeksforgeeks Link](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) :
This is the source I used for ```-r``` and ```-h```.
