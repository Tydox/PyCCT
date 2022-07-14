# PyCCT
Python Cheat Sheet Templates - Personal Memory Refresher

___
Dictionary:
1. Explicit - describes something that is very clear and without vagueness or ambiguity. 
2. Implicit - often functions as the opposite, referring to something that is understood, but not described clearly or directly, and often using implication or assumption.
3. 

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

#### Slicing  a List
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
