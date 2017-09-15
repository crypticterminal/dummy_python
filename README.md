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
with open("test.txt") as f:
    f.write("Hello World!")
```

## Level: Medium

### `sys.stdout`

* Write `Hello World!` to the standard console output:

```
import sys
sys.stdout.write("Hello World!")
```
