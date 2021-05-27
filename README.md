# Units Kattis (Problem C)
### [Link](https://open.kattis.com/problems/units)

## All

(__Input__) 4
km m mm cm
km = 1000 m
m = 100 cm
cm = 10 mm
4
m mm cm km
km = 100000 cm
km = 1000000 mm
m = 1000 mm
6
MiB Mib KiB Kib B b
B = 8 b
MiB = 1024 KiB
KiB = 1024 B
Mib = 1048576 b
Mib = 1024 Kib
6
Kib B MiB Mib KiB b
B = 8 b
MiB = 1048576 B
MiB = 1024 KiB
MiB = 8192 Kib
MiB = 8 Mib
0
![eCommerce](https://s3.gifyu.com/images/Units2.gif)


## Individual
(__Input 1__)   4
km m mm cm
km = 1000 m
m = 100 cm
cm = 10 mm

(__Input 2__)
4
m mm cm km
km = 100000 cm
km = 1000000 mm
m = 1000 mm

(__Input 3__)
6
MiB Mib KiB Kib B b
B = 8 b
MiB = 1024 KiB
KiB = 1024 B
Mib = 1048576 b
Mib = 1024 Kib

(__Input 4__)
6
Kib B MiB Mib KiB b
B = 8 b
MiB = 1048576 B
MiB = 1024 KiB
MiB = 8192 Kib
MiB = 8 Mib

(__Input 5__)
0

![eCommerce](https://s3.gifyu.com/images/Units.gif)

## Problem
The use of units is ubiquitous in science. Physics uses units to distinguish distance (e.g., meters, kilometers, etc.), weight (e.g., kilograms, grams), and many other quantities. Computer scientists have specialized units to describe storage capacity (e.g., kilobytes, megabytes, etc.). You are to write a program to display the conversion factors for a set of units.

Specifying the relationship between various units can be done in many different, but equivalent, ways. For example, the units for metric distance can be specified as the group of relationships between pairs for units: __1__ km = __1000__ m, __1__ m = __100__ cm, and __1__ cm = __10__ mm. An alternative set of pairs consists of: __1__ km = __100000__ cm, __1__ km = __1000000__ mm, and __1__ m = __1000__ mm. In either presentation, the same relationship can be inferred: __1__ km = __1000__ m = __100000__ cm = __1000000__ mm.

For this problem, the units are to be sorted according to their descending size. For example, among the length units cm, km, m, mm, km is considered the biggest unit since __1__ km corresponds to a length greater than __1__ cm, __1__ m, and __1__ mm. The remaining units can be sorted similarly. For this set, the sorted order would be: km, m, cm, mm.

This problem is limited to unit-systems whose conversion factors are integer multiples. Thus, factors such as __1__ inch = __2.54__ cm are not considered. Further, the set of units and the provided conversions are given such that all units can be expressed in terms of all other units.

## Input
The input consists of several problems. Each problem begins with the number of units, *__N__*. *__N__* is an integer in the interval __[2, 10]__. The following line contains *__N__* unique case-sensitive units, each of which consists of at most __5__ characters (using only a–z and A–Z). Following the set of units are *__N-1__* unique lines, each specifying a relationship between two different units, with the format containing the following four space-separated pieces: name of the unit; an “=”; a positive integer multiplier larger than __1__; and the name of a second unit that is smaller than the one to the left of the equal sign. Each of these lines establishes how many units are equivalent to the larger unit on the left. Each unit appears in the set of *__N-1__* lines and is given in such a way to ensure the entire system is defined. The set of multiples yields conversion factors that do not exceed __2<sup>31</sup>−1__.

The sentinel value of __*N*__ __= 0__ indicates the end of the input.

## Output
For each set of units, produce one line of output that contains the equivalent conversions. The conversions should be sorted left to right, with the largest unit appearing on the left. The conversion factors should be defined with respect to the leftmost unit (i.e., the largest unit) and should be separated by “ = ”.

![Units](https://i.ibb.co/93hgTpy/units.png)
