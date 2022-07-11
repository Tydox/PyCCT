# PyCCT
Python Cheat Sheet Templates
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


>[!TIP]
>```python
You can also combine tabs and newlines in a single string. The string "\n\t" tells Python to move to a new line, and start the next line with a tab```

3. rstrip()
Python can look for extra whitespace on the right and left sides of a string. To ensure that no whitespace exists at the right end of a string, use the rstrip() method
```python
fav_language = 'cpp '  
print(f"With Extra WhiteSapce: {fav_language} \nWithout Extra WhiteSpace: {fav_language.rstrip()}")
```

