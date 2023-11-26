# Variables

### Concepts

1. Variables are containers for store data
2. you can specify data type using casting 
```
x = str(mStrign)
y = int(3)
```
3. Here is a way to get data type
```
m = type(dta)
```
4. String variables can declare in single or double quotes
5. Variables are case sensitive
6. A variable name must start with a letter or the underscore character
7. A variable name cannot start with a number
8. A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
9. A variable name cannot be any of the Python keywords.

### Many Values to multiple variables

```
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```
### One value to multiple variable
```
x = y = z = "Orange"
print(x)
print(y)
print(z)
```
### Unpack Collection
```
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```
### 2 ways to create global variable

```
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```

```
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```
change global variable like this
```
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```