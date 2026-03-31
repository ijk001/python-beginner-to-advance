# 🧪 01-04: Basic Syntax

Python syntax is the set of rules that define how Python code is written and interpreted.

---

## 🖨️ print() Function

Used to display output on the screen.

### Example:

```print("Hello, World!")```

or,

```print('Hello, World!')```

Explanation:

- print() is a built-in function

- Text inside quotes is called a string

- can be used both single or double quote

Output: 
```Hello, World!```

---

## ⌨️ input() Function

The `input()` function is used to take input from the user.

### Example

```
name = input("Enter your name: ") 
print(name)
```

Explanation:

- input() waits for user input

- The text inside " " is a prompt

- The entered value is stored in the variable

⚠️ Important: input() Always Returns String

```
age = input("Enter your age: ")
print(type(age))
```

Output: 
```<class 'str'>```

👉 Even a number is entered, it will be stored as a string

---

## 💬 Comments

Comments are used to explain code. They are ignored by Python.

Single-line comment: # is used for comment

### Example

``` 
# This is a comment
print("Hello")
```

Inline comment:

```print("Hello")  # This prints Hello```

## 📌 Indentation (VERY IMPORTANT)

Python uses indentation (spaces) to define blocks of code.

### Example:
```
age = 18

if age >= 18:
    print("Adult")
```

Explanation:

- The indented line belongs to the if block

- Without indentation → ❌ Error

### ❌ Wrong:
```
if age >= 18:
print("Adult")
```
---

## 🔤 Case Sensitivity

Python is case-sensitive.

### Example:
```
name = "Imran"
Name = "Jahid"

print(name)
print(Name)
```

👉 These are treated as different variables

---

## 📦 Statements & Lines

Each line is usually one statement.

### Example:
```
x = 10
y = 20
print(x + y)
```
---

## Multiple Statements in One Line

Multiple statements in single line can be written ; (but not recommended).

```x = 10; y = 20; print(x + y)```

👉 Better to use separate lines for readability

---

## 🔗 Line Continuation

Used to break long lines into multiple lines.

Using backslash:
```
total = 10 + 20 + 30 + \
        40 + 50
```
Using parentheses (recommended):
```
total = (10 + 20 + 30 +
         40 + 50)
```

---

## 🔠 Strings and Quotes

Strings can be written using both double and single quote:
```
"Hello"
'Hello'
```
Multi-line string is written within tripple quote:
```
text = """This is
a multi-line
string"""
```
or,
```
text = '''This is
a multi-line
string'''
```

---

## 🎯 Basic Output Formatting

### 🔹 1. Comma Formatting (Basic Print)
```
name = "Imran"
print("Name:", name)
```
- "Name:" → string (fixed text)
- name → variable
- , → separates items in print()


### 🔹 2. f-String Formatting (Modern Way)
```
age = 25
print(f"My age is {age}")
```
- f"" → formatted string
- "My age is " → string
- {age} → variable inserted inside string

- 👉 Python replaces {age} with its value

---