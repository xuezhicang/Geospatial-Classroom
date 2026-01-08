# Control Flow & Algorithmic

## Sequence

```python
# Some Python code
num_1 = 1
num_2 = 2
sum_num = num_1 + num_2

print(f"the sum of two numbers is {sum_num }")
```

## Selection

### if-else

**Important:** Python uses **four spaces for indentation**, and this indentation is mandatory to define code blocks.

| **Category** | **Symbol** | **Meaning**                    | **Example**            |
| ------------ | ---------- | ------------------------------ | ---------------------- |
| Comparison   | `==`       | Equal to                       | `if a == b:`           |
| Comparison   | `!=`       | Not equal to                   | `if a != b:`           |
| Comparison   | `>`        | Greater than                   | `if a > b:`            |
| Comparison   | `<`        | Less than                      | `if a < b:`            |
| Comparison   | `>=`       | Greater than or equal to       | `if a >= b:`           |
| Comparison   | `<=`       | Less than or equal to          | `if a <= b:`           |
| Assignment   | `=`        | Assigns a value                | `x = 10`               |
| Logical      | `and`      | Both conditions must be true   | `if a > 5 and b < 10:` |
| Logical      | `or`       | At least one condition is true | `if a > 5 or b < 10:`  |
| Logical      | `not`      | Reverses the condition         | `if not a == 0:`       |
| Membership   | `in`       | Value exists in sequence       | `if x in my_list:`     |
| Membership   | `not in`   | Value does not exist           | `if x not in my_list:` |
| Identity     | `is`       | Same object                    | `if a is b:`           |
| Identity     | `is not`   | Different object               | `if a is not b:`       |

```python
// Some code
if condition_1:
    pass
else:
    pass

```

```python
// Some code

if condition_1:
    pass
elif contidion_2:
    pass
else:
    pass
```

### switch

Python got a **switch-like statement in version 3.10!!**

```python
def day_name(day):
    match day:
        case 1:
            return "Monday"
        case 2:
            return "Tuesday"
        case 3:
            return "Wednesday"
        case 4:
            return "Thursday"
        case 5:
            return "Friday"
        case 6 | 7:
            return "Weekend"
        case _:
            return "Invalid day"

print(day_name(1))
print(day_name(6))
print(day_name(10))
```

```python
//an interesting example

```

## Iteration

```python
// Some code
for i in range(10):
    print(i)
```

```python
// Some code
i = 0
while i<10:
    print(i)
```
