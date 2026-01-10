# Function

## Function

```
// Some code
def greet():
    print("Hello")

```

## Parameters & arguments

```
// Some code
def add(a, b):
    return a + b

add(2, 3)

```

`return` vs `print`

def f():\
return 10

def g():\
print(10)

## Scope

### Local variables

### global variables

* `global` keyword

```python
// Some code
# 1. Global variable
count = 10

def modify_global():
    global count  # Declare that we are using the global variable 'count'
    count = 20    # Modify the global variable
    print(f"Inside function (after modification): {count}")  # Output: 20

def create_local():
    # No 'global' keyword here, so this creates a new local variable
    count = 5
    print(f"Inside function (local variable): {count}")  # Output: 5

# Function calls
print(f"Before function call: {count}")  # Output: 10
modify_global()
print(f"After function call (global): {count}")  # Output: 20 (global variable changed)

create_local()
print(f"After function call (local): {count}")  # Output: 20 (global variable unchanged)

```



`nonlocal`

`fgsdf`

```
// Some codedef outer():
    x = 10

    def inner():
        nonlocal x
        x = 20

    inner()
    print(x)

outer()
```

* Nested functions

def outer():\
def inner():\
print("Hello from inner")\
inner()

outer()



* LEGB rule (name it later)

| Letter | Scope     | Meaning                 |
| ------ | --------- | ----------------------- |
| L      | Local     | Inside current function |
| E      | Enclosing | Outer (nested) function |
| G      | Global    | Module level            |
| B      | Built-in  | Python built-ins        |

#### Example

```python
x = "global"

def outer():
    x = "enclosing"
    def inner():
        print(x)
    inner()

outer()
```

* Closures

A function that **remembers variables from its outer scope**, even after the outer function finishes.

```
// Some code
def make_multiplier(n):
    def multiply(x):
        return x * n
    return multiply

double = make_multiplier(2)
print(double(5))
```

* Lambdas

```
// Some code
add = lambda a, b: a + b
print(add(2, 3))

same thing:

def add(a, b):
    return a + b


```

*
* ## Parameter \*arg and \*\*keyarg
