
# Lab 7: Removing  all the duplicate elements in a list

[TOC]

## Problem statement 

Write a python program that removes all the duplicate elements in a list. 

	Sample Input0: [1, 2, 3, 4]
	Sample Output0: [1, 2, 3, 4]

	Sample Input1: [1, 2, 3, 4, 4]
	Sample Output1: [1, 2, 3]

	Sample Input2: [5, 5, 5, 5]
	Sample Output2: []

	Sample Input3: [11, 22, 33, 44, 22]
	Sample Output3: [11, 33, 44]


## Solution Key

```python 

#!/usr/bin/python
# -*- coding: utf-8 -*-


def remove_duplicates(mlist):
	tokens = {}
	for elem in mlist: 
		tokens[elem] = 1 
		
	return list(tokens.keys())


def get_list_of_elements():
    """returns a list containing elements entered by user
....The sequence of steps in the algorithm is:
....#1 - initialize the list
....#2 - Start loop for maximum of 10 entries
........#3 - Get input from user. If null, break
........#4 - Append the element to the list
....#5 - Return the list containing elements
...."""

    ilist = []  # 1
    for x in range(0, 10):  # 2
        element = input('Enter element ' + str(x) + ': ')
        if element:
            ilist.append(element)  # 4
        else:
            break  # 3
    return ilist  # 5


# Program starts here

elist = get_list_of_elements()
print ('List of elements: ', elist)
nlist = remove_duplicates(elist)
print ('The list after removing duplicates ', nlist)


```


## CloudCoder Exercise 

TBD 

## Pre-Lab Questions 

0. If a list contains `[1, 2, 3, 'python', 3, 4, 'python1', 'python', 5]`, what would the list look like after all the duplicates are removed? 
1. If a list contains `[5, 5, 5, 5, 5, 6, [1, 2, 6], [1, 2, 6]]`, what would the list contain after all the duplicates are removed? 
2. What is the method available to remove an element from a list? 
3. How will you get a list of all the `keys` that are present in a dictionary (which basically contains a key:value pair)? 
4. How will get a list of all the `values` that are present in a dictionary? 
5. What is the python code for building a dictionary out of 3 tuples? For e.g. 
	> ("jan", 31)  
	> ("feb", 28) and  
	> ("mar", 31) `  

6. A list contains `n` elements (where `n` is a positive integer and  `0 > n > 10`. Write the necessary python code to produce a list that contains only the last `n-1` elements. Is there a version of the code that does not use any `list` methods whatsoever to achieve the same result? 

7. What is the value of `L` after you run the code below?

> ![Imgur](http://i.imgur.com/3WRTL5N.png)



## Post-Lab Questions 

0. Rewrite the code to use only `lists` and not a `dictionary`. Or vice versa. 

## Bonus 1 

1. You are asked to remove all the duplicate occurrences of only one specific element in the list. Write a function for this. 

## Bonus 2 

1. There is probably a one-line Pythonic solution for almost every complicated problem out there. That is also the case for this lab exercise. Can you figure it out? 
2. There is even a shorter one liner if you use another powerful Python data type. Can you figure it out? 
3. Between 1 and 2, which solution is more preferable? And why? 


## Interview grade

Calculate the `gcd` for a list of integers using the prime factorization method. The method is well described in the video at http://j.mp/gcdPrime - use lists as part of the solution. 

## Related Links 

https://goo.gl/v7ephq