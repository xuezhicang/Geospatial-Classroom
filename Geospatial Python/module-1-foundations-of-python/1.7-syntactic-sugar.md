# Syntactic sugar

### Common examples of Python syntactic sugar

#### 1. List / Set / Dict Comprehensions

Instead of writing loops manually:

```python
squares = []
for i in range(10):
    squares.append(i * i)
```

You can write:

```python
squares = [i * i for i in range(10)]
```

This is one of Python’s most beloved features—compact and expressive.

***

#### 2. Multiple Assignment & Tuple Unpacking

Swap variables without a temp variable:

```python
a, b = b, a
```

Unpack values easily:

```python
x, y, z = (1, 2, 3)
```

Behind the scenes, Python is still creating a tuple.

***

#### 3. `for … else`

This surprises many people:

```python
for n in numbers:
    if n == 5:
        break
else:
    print("5 not found")
```

The `else` runs **only if the loop didn’t break**.

***

#### 4. Default and Keyword Arguments

Instead of forcing argument order:

```python
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}")
```

Usage:

```python
greet("Alice")
greet("Bob", greeting="Hi")
```

This makes APIs much more readable.

***

#### 5. `with` Statement (Context Managers)

Instead of:

```python
f = open("file.txt")
try:
    data = f.read()
finally:
    f.close()
```

You write:

```python
with open("file.txt") as f:
    data = f.read()
```

Cleaner, safer, and harder to mess up.

***

#### 6. Ternary (Conditional) Expressions

One-line `if-else`:

```python
result = "even" if x % 2 == 0 else "odd"
```

Instead of a full `if` block.

***

#### 7. Chained Comparisons

Python lets you write math-like expressions:

```python
if 0 < x < 10:
    print("x is in range")
```

This is syntactic sugar for:

```python
if x > 0 and x < 10:
```

***

#### 8. f-Strings (Formatted String Literals)

Instead of:

```python
"Hello " + name + ", you are " + str(age)
```

You write:

```python
f"Hello {name}, you are {age}"
```

They’re faster and far more readable.

***

#### 9. `*args` and `**kwargs`

Collect variable arguments easily:

```python
def add(*numbers):
    return sum(numbers)
```

And unpack them:

```python
nums = [1, 2, 3]
add(*nums)
```

***

#### 10. `@decorators`

Decorators are _heavy_ syntactic sugar:

```python
@timer
def slow_function():
    ...
```

This is really:

```python
slow_function = timer(slow_function)
```

They’re powerful but can hide complexity.
