# Introduction

Repository of "dummy" python code snippets that should help the newcomers in Python to learn it the easy way


# Code Snippets
## Level: Easy
### `print`

* Write `Hello World!` to the console output:

```
print "Hello World!"
```

### Single-line comment

* Add single-line comments inside the code:

```
# The following command writes "Hello World!" to the console output
print "Hello World!"  # This is that line
```

### `open()/write()`

* Write `Hello World!` to a file `test.txt` inside current directory:

```
with open("test.txt", "w") as f:
    f.write("Hello World!")
```

Note: String value `"w"` represents an open file "mode". Use `w` when writing, `r` when reading, etc. More can be found [here](https://docs.python.org/2/tutorial/inputoutput.html#reading-and-writing-files)

### `open()/read()`

* Read content of file `test.txt` inside current directory and store it to a variable `value`:

```
with open("test.txt", "r") as f:
    value = f.read()
```

### `raw_input()`

* Read user provided string from keyboard and store it to a variable `value`:

```
value = raw_input()
```

### User function

* Create a function which will take two (string) parameters and return result of concatenation:

```
def concat(a, b):
    return a + b

c = concat("foo", "bar")
```

### Import module

* Import standard module [`math`](https://docs.python.org/2/library/math.html) and print result of `math.cos(math.pi)`:

```
import math
print math.cos(math.pi)
```

### For loop

* Print out all numbers from 0 to 9:

```
for i in xrange(0, 10):
    print i
```

Note: You should prefer usage of `xrange()` over `range()` because of lower memory consumption. More can be found [here](http://pythoncentral.io/how-to-use-pythons-xrange-and-range/).

## Level: Medium

### `sys.stdout`

* Write `Hello World!` to the standard console output:

```
import sys
sys.stdout.write("Hello World!")
```

### Multi-line comment

* Add multi-line comments inside the code:

```
"""
This is a multi-line comment:

The following command writes "Hello World!" to the console output
"""

print "Hello World!"
```
