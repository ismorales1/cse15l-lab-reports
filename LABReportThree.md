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
Example #2 using ```grep``` with ```-v``` option:

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
