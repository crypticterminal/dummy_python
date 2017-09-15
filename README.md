# Introduction

Repository of "dummy" python code snippets that should help the newcomers in Python to learn it the easy way


# Code Snippets
## Level: Easy
### `print`

* Write `Hello World!` to the console output:

```
print "Hello World!"
```

### `open()/write()`

* Write `Hello World!` to a file `test.txt` inside current directory:

```
with open("test.txt", "w+") as f:
    f.write("Hello World!")
```

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

## Level: Medium

### `sys.stdout`

* Write `Hello World!` to the standard console output:

```
import sys
sys.stdout.write("Hello World!")
```
