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

## scope

### Local variables

### global variables

* `global` keyword

```
// Some code
# 1. 全局变量
count = 10 

def modify_global():
    global count # 声明 count 是全局变量
    count = 20 # 修改全局变量
    print(f"在函数内部（修改后）: {count}") # 输出 20

def create_local():
    # 这里没有使用 global，所以会创建一个新的局部变量
    count = 5 
    print(f"在函数内部（局部变量）: {count}") # 输出 5

# 调用函数
print(f"函数调用前: {count}") # 输出 10
modify_global()
print(f"函数调用后 (global): {count}") # 输出 20 (被修改了)

create_local()
print(f"函数调用后 (local): {count}") # 输出 20 (全局 count 没变)
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
