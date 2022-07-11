# PyCCT
Python Cheat Sheet Templates - Personal Memory Refresher
--- 
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
#### Accessing Elements in a List
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

