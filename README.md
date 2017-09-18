# Introduction

Repository of "dummy" Python (v2) code snippets that should help the newcomers to learn it the easy way


# Code Snippets
## Level: Easy

### Variable

* Put string `Hello World!` to the variable `value`:

```
value = "Hello World!"
```

or

```
value = 'Hello World!'
```

Note: Some people prefer usage of `'` for delimiting single character values, while `"` for all other multi character values

---

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

* Write `Hello World!` to a file `dummy.txt` inside current directory:

```
with open("dummy.txt", "w") as f:
    f.write("Hello World!")
```

Note: String value `"w"` represents an open file "mode". Use `w` when writing, `r` when reading, etc. More can be found [here](https://docs.python.org/2/tutorial/inputoutput.html#reading-and-writing-files).

### `open()/read()`

* Read content of file `dummy.txt` inside current directory and store it to a variable `value`:

```
with open("dummy.txt", "r") as f:
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

### For-loop

* Print out all numbers from 0 to 9:

```
for i in xrange(0, 10):
    print i
```

Note: You should prefer usage of `xrange()` over `range()` because of lower memory consumption. More can be found [here](http://pythoncentral.io/how-to-use-pythons-xrange-and-range/).

### While-loop

* Print out all numbers from 0 to 9:

```
i = 0
while i < 10:
    print i
```

### `list()/[]`

* Store all numbers from 0 to 9 to a list `numbers`:

```
numbers = []  # shorter for list()

for i in xrange(10):
    numbers.append(i)
```

or:

```
numbers = range(10)
```

or (by using one-liner "iterator"):

```
numbers = [i for i in xrange(10)]
```

### `dict()/{}`

* Store all numbers from 0 to 9, along with english related cardinal, to a dictionary `numbers`:

```
numbers = {}  # shorter for dict()

numbers[0] = "zero"
numbers[1] = "one"
numbers[2] = "two"
numbers[3] = "three"
numbers[4] = "four"
numbers[5] = "five"
numbers[6] = "six"
numbers[7] = "seven"
numbers[8] = "eight"
numbers[9] = "nine"
```

or just:

```
numbers = {0: "zero", 1: "one", 2: "two", 3: "three", 4: "four", 5: "five", 6: "six", 7: "seven", 8: "eight", 9: "nine"}
```

### `set()`

* Store all numbers from 0 to 9 to a set `numbers`:

```
numbers = set()

for i in xrange(10):
    numbers.add(i)
```

Note: Difference between a list and a set is that list has (all) elements stored in order of appending new elements, while set stores unique values in no particular order

### `tuple()`

* Store all numbers from 0 to 9 to a tuple `numbers`:

```
numbers = tuple(xrange(10))
```

or:

```
numbers = (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)
```

Note: Difference between a list and a tuple is that list can be changed, while tuple can't (immutable). In theory, tuple should consume less memory

## Level: Medium

### `sys.stdout`

* Write `Hello World!` to the standard console output:

```
import sys
sys.stdout.write("Hello World!")
```

### Write binary content to a file

* Write `Hello World!` to a binary file `dummy.raw` inside current directory:

```
with open("dummy.raw", "wb") as f:
    f.write("Hello World!")
```

Note: Use binary file mode appendix `b` when dealing with raw non-textual content as Python accross different operating systems tends to use different newline representations. More can be found [here](https://docs.python.org/2/tutorial/inputoutput.html#reading-and-writing-files).

### Multi-line comment

* Add multi-line comments inside the code:

```
"""
This is a multi-line comment:

The following command writes "Hello World!" to the console output
"""

print "Hello World!"
```

### Catching exceptions

* Running some code while expecting that something could go wrong:

```
try:
    a = 1 / 0
except Exception, msg:
    print "[x] something went wrong ('%s')" % msg
```

### `any()`

* Enter two numbers `a` and `b` and check if any of conditions `a > 17`, `a == b`, `a == b * 3` is satisfied:

```
a = int(raw_input("a = "))
b = int(raw_input("b = "))
print "Any condition is satisfied: %s" % any((a > 17, a == b, a == b * 3))
```

### `all()`

* Enter two numbers `a` and `b` and check if all conditions `a > 17`, `a == b`, `a == b * 3` are satisfied:

```
a = int(raw_input("a = "))
b = int(raw_input("b = "))
print "All conditions are satisfied: %s" % all((a > 17, a == b, a == b * 3))
```

### `filter()`

* Remova all `None` values from a list `[1, 2, 3, None, 4, None, 5]`:

```
values = [1, 2, 3, None, 4, None, 5]
filtered = filter(lambda _: _ is not None, values)
```

or:

```
values = [1, 2, 3, None, 4, None, 5]
filtered = filter(None, values)
```

or just:

```
values = [1, 2, 3, None, 4, None, 5]
filtered = [_ for _ in values if _ is not None]
```
