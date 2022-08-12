# PyCCT
Python Cheat Sheet Templates - Personal Memory Refresher

___
Dictionary:
1. Explicit - describes something that is very clear and without vagueness or ambiguity. 
2. Implicit - often functions as the opposite, referring to something that is understood, but not described clearly or directly, and often using implication or assumption.
3. Mutable - value can be changed
4. Immutable - value cannot be changed

___

## Data Types
### Boolean
True == 1
False == 0

```python
print(f"True==0?: {True==0}")  
print(f"True==1?: {True==1}")  
print(f"False==0?: {False==0}")  
print(f"False==1?: {False==1}")
```





## F - Strings
"f" stands for "format"

```python
   firstName = "lena"  
   lastName = "tsibirii"  
   name = f"{firstName} {lastName}"
```

```python 
   firstName = "Lolipop"  
   lastName = "Fluffy"  
   print(f"{firstName} {lastName}")
```

# White Spaces
1. Tabs `\t`
To add a tab to your text, use the character combination `\t` :
```python
print("\t <something>")
```
2. New Line `\n`
To add a newline in a string, use the character combination `\n` :
```python
print("Languages:\nPython\nC++\n <something>")
```


#### TIP
```python
You can also combine tabs and newlines in a single string. The string "\n\t" tells Python to move to a new line, and start the next line with a tab
```

3. Stripping Whitespace - `rstrip()`
Python can look for extra whitespace on the right and left sides of a string. To ensure that no whitespace exists at the right end of a string, use the rstrip() method
```python
fav_language = 'cpp '  
print(f"With Extra WhiteSapce: {fav_language} \nWithout Extra WhiteSpace: {fav_language.rstrip()}")
```

# Numbers
### Int Operators:
1. Add `a + b`
2. Substract `a - b`
3. Multiply `a * b`
4. Divide `a / b` ->$\ A\ /\ B = \frac{A}{B}$
5. Exponent `a ** b` ->$\ A**\ B = A ^ B$
6. Modulo `a % b`
### Float
A number with a decimal point is a *float*.

### Integers & Floats
When you divide any two numbers A,B. Even if they are integers that result in a whole number, you'll always get a float!
```python
4/2 = 2.0
```
That is because python defaults to a float in any operation that uses a float, even if the output is a whole number.

### Underscores in Numbers (int,float)
When writing long numbers, you can group digits using underscores to make the number more readable whilst still keeping the correct value!
```python 
num = 14_00_01234_32
#is the same as
num = 14000123432
```

### Multiple Assignment
You can assign values to more than one variable using just a single line, this can help shorten your program and make it easier to read. 

`Tip:`
This is most common technique when initializing a set of numbers.
```python
x=4  
y=7  
z=3  
print(x,y,z)

#----vs----

a,b,c = 4,7,3  
print(a,b,c)
```

### Constant
Unlike C, in order to have a constant variable aka immutable, you use all capital letters ONLY AS AN INDICATION that the variable should be treated as a constant and never be changed, but it can still be changed if you are not careful!
```python
MAX_AMMO = 132
```
This is just a visual indication to "Hey don't change me".

# Comments
Comments are initiated as `#`
```python
def func():
	print(5) #this will print number 5
	#print fluffy
	print(fluffy)
```

# Data Structures
## Lists
Lists allow you to sore a set of information in one place, whether you have just a few or many items.

A list is a collection of items in a particular order. Like an ordered set.

A list can have whatever variable type you fancy dancy.

* It's a good idea to make the name of your list - plural, such as letters,digits,names and cars

```python
#Example of a list
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
```

### List Operations

---

##### Accessing Elements in a List
Lists are ordred collections, you access any position using the index like in C.
```python
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles[0])
print(bicycles[2])

#will print
> trek
> redline
```

* Note that the Index positions start at 0 and not 1

##### Accessing the Element from the end in a List
Using negative indices will allow to access the list from its end.
index = -1 , will access the last element in a list.
index = -2, will access the second from last in a list.

```python
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles[-1])
print(bicycles[-2])

#will print
> specialized
> redline
```

---

#### Changing, Adding, and Removing Elements
##### Creating an Empty List
```python
myList = []
```
##### Modifiying Elements in a List
To change an element, use the name of the list followed by the index of the element you want to change, and then provide the new value you want that item to have.
```python
myList[<index>] = <Some Data>
```
Example:
```python
motorcycles = ['honda', 'yamaha', 'suzuki']  
motorcycles[2] = 'ducati'
```

##### Duplicating/Copying a List
```python
old_list = [5,4,3,2,1]  
new_list = old_list[:]  
print(new_list)  
new_list.append(123123)  
print(old_list)  
print(new_list)
```


#### Adding Elements to a List
##### 1. Append
When you append an item to a list, the new element is added to the end of the list,without affecting any of the other elements in the list.

```python
myList.append(<Some Data>)
```
Example:
```python
motorcycles.append('ducati')
```

The append() method makes it easy to build lists dynamically. For example, you can start with an empty list and then add items to the list using a series of append() calls.
```python 
motorcycles = [] #empty list
motorcycles.append('honda') 
motorcycles.append('yamaha') 
motorcycles.append('suzuki')
```

##### 2. Insert
You can add a new element at any position in your list by using the insert() method. You do this by specifying the index of the new element and the value of the new item.

* It will PUSH the element into the list, not overwrite existing data!*
```python
myList.insert(<index>,<Some Data>)
```
Example:
```python
motorcycles = ['honda', 'yamaha', 'suzuki']  
motorcycles.insert(0, 'ducati')
```

#### Removing Elements from List
here’s a simple way to decide: 
when you want to delete an item from a list and not use that item in any way, use the del statement; 
if you want to use an item as you remove it, use the pop() method.


##### 1. Del
You can remove an item according to its position in the list or according to its value.
If you know the position of the item you want to remove from a list, you can use the del statement.
```python
del myList[<index>]
```

##### 2.Pop
The pop() method removes the last item in a list, but it lets you work with that item after removing it. 
The term pop comes from thinking of a list as a stack of items and popping one item off the top of the stack. In this analogy, the top of a stack corresponds to the end of a list.
```python
poppedVal = myList.pop()
```
You can use pop() to remove an item from any position in a list by including the index of the item you want to remove in parentheses
```python
poppedVal = myList.pop(<index>)
```

#### 3. Remove by Value
If you only know the value of the item you want to remove, you can use the `remove()`
```python
myList.remove(<some data>)
```
Example:
```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']   
motorcycles.remove('ducati')
```

* The `remove()` method deletes only the first occurrence of the value you specify. If there’s a possibility the value appears more than once in the list, you’ll need to use a loop to make sure all occurrences of the value are removed.
---
#### Orginizing a List
##### Sort vs Sorted
Sort - changes your list 
```python 
myList.sort()
```

Sorted - created a copy of your list and sorts that one, keeps the origiral list unchanged
```python 
sorted(myList)
```

Example:
```python 
cars = ['bmw', 'audi', 'toyota', 'subaru']  
print("Here is the original list:")  
print(cars)  
print("\nHere is the sorted list:")  
print(sorted(cars))  
print("\nHere is the original list again:")  
print(cars)  
print("\nHere is the permanent sorted list:")  
cars.sort()  
print(cars)  
print("\nHere is the reversed permanent sorted list:")  
cars.sort(reverse=True)  
print(cars)
```

*Sorting a list alphabetically is a bit more complicated when all the values are not in lowercase.*

##### Reverse Order
To reverse the original order of a list, you can use the `reverse()`.
```python 
myList.reverse()
```
Notice that reverse() doesn’t sort backward alphabetically; it simply reverses the order of the list indices!


##### Find Length of a List
You can quickly find the length of a list by using the `len()` .

```python
len(myList)
```

Python counts the items in a list starting with one, so you shouldn’t run into any off by one errors when determining the length of a list.

---

### Working With Lists
#### For Loops

```python
for <item> in <item_list> :
	print(<item>)


for dog in dogs:
	do_something
```

#### Numerical List
Lists are ideal for storing sets of numbers, and Python provides a variety of tools to help you work efficiently with lists of numbers.

```python
for <index> in range( <start_index> , <end_index> ):
	print(<index>)


for value in range(1,5):
	print(value)
	
	# >1,2,3,4
	
for value in range(3):
	print(value)
	
	# >0,1,2
```

The range is from `<start_index>` until  `<end_index> -1`
Example:
range(0,5) -> 0,1,2,3,4
range(7,9) -> 7,8
range(7,10) -> 7,8,9

```python
for num in range(start_index, end_index, step_size)

for i in range(0,20,5):  
    print(i)  
  
for i in range(20,0,-5):  
    print(i)
```

#### Creating  A Numerical List
```python
myList = list(range(end_index) #defaults start to 0
myList = list(range(start_index, end_index))
myList = list(range(start_index, end_index, step_size))
			  
			  
			  
squares = []  
for value in range(1,11):  
    square = value ** 2  
    squares.append(square)  
print(squares)  
  
squares = []  
for value in range(1,11):  
    squares.append(value**2)  
print(squares)  
  
squares= []  
for value in range(1,11):  
    squares.insert(value-1,value**2)  
print(squares)
```

#### Simple Numerical List Functions
```python
digits = list(range(0,20,3))
min(digits)
max(digits)
sum(digits)
```

#### List Comprehensions
List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.
A list comprehension combines the for loop and the creation of new elements into one line, and automatically appends each new element.

```python

newlist = [<new_value_in_List> for <index> in range(<end index>) if condition == True]


newList = [value/2 for value in range(1,15)]  
print(newList)  
  
newList = [value for value in range(1,15) if(value % 2 == 0)]  
print(newList)

newList = [value*100 for value in range(1,15) if(value % 2 == 0) if(value/2 > 3)]  
print(newList)

```

#### Iterating over a List
```python
# Iterating over a list!  
# more efficient way!  
# value only  
numbers = [num for num in range(0, 10, 2)]  
print(f"Numbers:{numbers}")  
for value in numbers:  
    print(f"\t\t\t\tValue={value}")  
  
# value and index  
numbers = [num for num in range(0, 10, 2)]  
print(f"Numbers:{numbers}")  
for index, value in enumerate(numbers):  
    print(f"\t\tIndex={index}\tValue={value}")  
  
# less efficient way!  
numbers = [num for num in range(0, 10, 2)]  
print(f"Numbers:{numbers}")  
for index in range(len(numbers)):  
    print(f"\t\tIndex={index}\tValue={numbers[index]}")

```

#### Slicing  a List - Creating a subset of list
```python
myList[start_Index : end_Index : step_Size]
-------------------------------------------
newList = [value for value in range(1,15)]  
print(newList)  
> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]

print(newList[5:]) #start from index 6 til end 
> [6, 7, 8, 9, 10, 11, 12, 13, 14]

print(newList[-5:])  #start from index 5 from last aka 10 til end
> [10, 11, 12, 13, 14]

print(newList[:5]) #start from index 0 til 4
> [1, 2, 3, 4, 5]

print(newList[:-5]) #start from index 0 til 5 from last aka 10
> [1, 2, 3, 4, 5, 6, 7, 8, 9]

print(newList[0:10:2])  #start from index 0 til 10 with a step of 2 betwen indices
> [1, 3, 5, 7, 9]
```

#### Looping Through a Slice
You can use a slice in a for loop if you want to loop through a subset of the elements in a list. In the next example we loop through the first three players and print their names as part of a simple roster, Instead of looping through the entire list of players, we loop through only the first three names:

```python
players = ['charles', 'martina', 'michael', 'florence', 'eli']  
print("Here are the first three players on my team:")  
for player in players[:3]:  
    print(player.title())
	
>	Here are the first three players on my team:
	Charles
	Martina
	Michael
```

When you’re working with data, you can use slices to process your data in chunks of a specific size.

#### Copying a List
INCORRRECT! 
Python will reference the pointer to the same address, it won't copy the variable like in C
```python
lena = ['blue','purple','red']  
daniel = lena  
daniel.append('black')  
print("daniel=lena")  
print(f"Lena:{lena}")  
print(f"Daniel:{daniel}")  

>	daniel=lena
	Lena:['blue', 'purple', 'red', 'black']
	Daniel:['blue', 'purple', 'red', 'black']
```

CORRECT!
You use `newList = oldList[:]` in-order to successfully copy a list!
This is how to create 2 seperate lists! 
```python
lena = ['blue','purple','red']  
daniel = lena[:]  
daniel.append('black')  
print("\ndaniel=lena[:]")  
print(f"Lena:{lena}")  
print(f"Daniel:{daniel}")

>	daniel=lena[:]
	Lena:['blue', 'purple', 'red']
	Daniel:['blue', 'purple', 'red', 'black']
```


---


## Tuples - Immutable list
Lists work well for storing collections of items that can change throughout the life of a program, sometimes you’ll want to create a list of items that cannot change.

### Creating a Tuple
```python
myTup = (<values>)
```

Once you define a tuple, you can access individual elements by using each item’s index, just as you would for a list.


* Tuples are technically defined by the presence of a comma; the parentheses make them look neater and more readable. If you want to define a tuple with one element, you need to include a trailing comma: `myTup = (21,)`




## Logical Comp
### Check if a Value is in a List
```python
flag = <value> in <list>
#flag will be a bool - True\False
```

Example:
```python
requested_toppings = ['mushrooms', 'onions', 'pineapple']
flag = 'mushrooms' in requested_toppings #check if value is in a list  
print(flag)

> True
```

### Check if a Value isn't in a List
```python
flag = <value> not in <list>

if <value> not in <list>
	do something
```
Example:
```python
users = ["dan","shrek","gulnuma","lexi"]  
user1 = "fluffy"  
user2 = "dan"  
  
flag = user1 not in users  
print(flag)  
flag2 = user2 not in users  
print(flag2)
```

## If Statements
```python
if <conditional_test>:
	do something
```
## If Else Statements
```python
if <conditional_test>:
	do something
else: 
	do something_else
```
## If-elif-else Statements
```python
if <conditional_test>:
	do something
elif <conditional_test>:
	do something
elif <conditional_test>:
	do something
else:
	do something
	
```


## Dictionaries
Dictionaries is like a hash table, for every key you store whatever value you want, it can be an int, list, tuple, a dict within a dict, etc.

The key is the identifier, and the value is the content you want stored related to that id.
```python
#Init an Empty Dictionary
newDict = {}  
#Add a new Key:Value pair
newDict[ <key> ] = <value>
```

Typically, you’ll use empty dictionaries when storing user-supplied data in a dictionary or when you write code that generates a large number of key-value pairs automatically.

```python
alien_0 = {'color': 'green', 'points': 5}  
print(alien_0)  
alien_0['x_position'] = 0  
alien_0['y_position'] = 25  
print(alien_0)
```

### Modifying Values in a Dictionary
```python
newDict[ <existing_key> ] = <new_value>
```

### Removing Key:Values in a Dictionary
This will remove the entire key and all associated values -> this is not a pop function.
```python
del newDict[ <existing_key> ]
```

### Finding/Accessing Values

Using get you can search and retrieve a value, and also have a default value (custom error message).
```python
value = mydict.get(<key> , <custom error message if key isnt found>)
```


If you leave out the second argument in the call to get() and the key doesn’t exist, Python will return the value None. The special value None means “no value exists.” This is not an error: it’s a special value meant to indicate the absence of a value.

```python
alien_0 = {'color': 'green', 'points': 5}
point_value = alien_0.get('colors',"Some Default Value because key wasnt found")  
print(point_value)  
point_value = alien_0.get('color',"Some Default Value because key wasnt found")  
print(point_value)
```

### Looping through Dictionary

#### Key + Value loop
```python
for key, value in users.items():  
    print(f"\nKey: {key}\tValue: {value}")
```

#### Key loop - python default behaviour
```python
for key in users.keys():  
    print(f"\nKey: {key}")

#IS THE SAME AS BECAUSE ITS PYTHON DEFAULT BEHAVIOUR
for key in users:  
    print(f"\nKey: {key}")

```

#### Value loop
```python
for val in users.values():  
    print(f"\nValue: {val}")
```


## Sets
Set is an unordered list of unique values, it will store nonrepetitive list of values.
```python
myset ={ value1, value2, value3 }
```

sets do not retain items in any specific order.

```python
mySet = {'c','p','c','d'}  
print(mySet)

> c,p,d
```

### Nesting  - Math Set -> Subset -> Subset
Dict in a List
List in a Dict
List in a List
Dict in a Dict
You shoudn't next too far, 1 subset or 2 subsets is already complex enough, look for a simpler solution.


## While
```python
end_condition = 5  
iterator = 0  
while iterator < end_condition:  
    print("fluffy dog\t")  
    iterator +=1  
  
msg = "exit"  
while msg != "exit":  
    msg = input(f"{msg}:")  
    if msg != "exit":  
        print(msg)  
  
active = True  
while active: #while active == true  
    msg = input(f"{msg}:")  
  
    if msg == "exit":  
        active = False  #stop while loop  
    else:  
        print(msg)
```

#### Special Keywords!
##### Break
Will stop the loop entirely!

##### Continue
Will skip all the remaining code and skip to the next iteration.

### Removing All Instances of spcific values from a List
```python
numbers = [1,2,3,1,1,5]  
rem_num = 1  

while rem_num in numbers:  #this is a dynamic condition->refreshes numbers - for loop does not refresh the condition variable!!!
    numbers.remove(rem_num)  
  
print(numbers)

numbers = [1,2,3,1,1,5]  
rem_num = 1  
i=0  
while rem_num in numbers:  
    numbers.remove(rem_num)  
    i+=1  
    if i == 2:  
        numbers.append(1)  
    print(numbers)  

>	[2, 3, 1, 1, 5]
	 [2, 3, 1, 5, 1]
	 [2, 3, 5, 1]
	 [2, 3, 5]
```

## Functions
Template:
```python
def myFunc(args):
	<do something>
```

### Function Default value - like in C
```python
def func(arg1,arg2=default_value)

def mypet(name,age=7):  
    print(f"Name: {name}\nAge: {age}")

mypet("Lucky")
```

### Calling function with un-ordered arguments
you can specify what argument you want to associate with your value, that why you don't need to worry about positional arguments / the order of the function paramaters.

```python
myFunc(arg3=something, arg1=something, arg2=something)


def mypet(name,age):  
    print(f"Name: {name}\nAge: {age}")  
  
  
#Main  
if __name__ == '__main__':  
    mypet(age=5,name="Lucky")



```

### Making Argument optional
Better to use `None`  than `''`

We can set the argument to `''` which will make it empty default value and ignore the argument unless the user provides a value.
```python
def myFunc(arg1, arg2='')
	if arg2:
		do something
	else:
		do something

def myFunc(arg1, arg2=None)
	if arg2:
		do something
	else:
		do something

```

```python
def pets(name,age=None):  
    if age:  
        print(f"Name: {name}\nAge: {age}")  
    else:  
        print(f"Name: {name}")
```


### Preventing a Function from Modifiying a List/Dict/etc
In order to pass a copy of the list (not the original), basically by Value and not Reference, we use `[:]`

```python
def myFunc(aList):
	do something

#Main
myFunc(myList[:])
```

```python
def checkPointers(ogList,cpyList):  
    print(f"Objects are the same in memory:\t{ogList is cpyList}")  
  
#Main  
if __name__ == '__main__':  
    mylist = [1,2,3]  
    checkPointers(ogList=mylist,cpyList=mylist[:])  
    checkPointers(ogList=mylist,cpyList=mylist)

> Objects are the same in memory:	False
> Objects are the same in memory:	True

```


## Import function from other files
### Import all functions from Module
```python
import <file>
```

### Import a Specific Function
```python
from module_name import func_name

from module_name import func_name1,func_name2,fun_nameK
```

### Import Function with an alias
```python
from module_name import func_name as newFuncName
```

### Import Module with an alias
```python
import module_name as newModuleName
```

### Import All Function directly
Then you dont need to write module_name.func2, and just func2.
```python
from module_name import *
```



# Testing Your Code
