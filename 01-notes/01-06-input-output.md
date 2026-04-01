# ⌨️ 01-06 Input & Output

---

## 📌 input() Function

input() is used to take input from the user through the keyboard.

- It pauses the program and waits for user input
- Whatever the user types is returned as a string (str)
- Optional message (prompt) can be shown to guide the user

✅ Syntax

```input("message to user")```

✅ Example
```
name = input("Enter your name: ")
print("Hello", name)
```
💡 Explanation
- The program displays → Enter your name:
- The user types → Imran
- name stores "Imran" (string)
- print() displays the result

⚠️ Important Note

```age = input("Enter age: ")```

- Even if the user enters 25, Python stores it as: "25"   # string, not integer

### 📌 Taking Multiple Inputs
🔹 Simple Way
```
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print("Sum =", a + b)
```

🔹 Multiple Inputs in One Line
```
a, b = map(int, input("Enter two numbers: ").split())

print("Sum =", a + b)
```
👉 Example input:

```10 20```

---

## 📌 Type Conversion (Casting)
### 🔹 Why Type Conversion is Needed?

Since input() returns a string, mathematical operations will fail without conversion.

❌ Example (Error)
```
num = input("Enter a number: ")
print(num + 5)
```

👉 Error because:
- "num" is string
- 5 is integer

✅ Correct Approach
```
num = int(input("Enter a number: "))
print(num + 5)
```
### 🔹 Common Conversion Functions

| Function | Description            | Example                  |
|----------|------------------------|--------------------------|
| `int()`  | Converts to integer    | `int("10") → 10`         |
| `float()`| Converts to decimal    | `float("3.5") → 3.5`     |
| `str()`  | Converts to string     | `str(100) → "100"`       |

🔹 Float Example
```
price = float(input("Enter price: "))
print(price * 2)
```

🔹 String Conversion Example
```
num = 50
text = str(num)
print("Value is " + text)
```

---

## 📌 print() Function

print() is used to display output on the screen

- It can print text, numbers, variables, and expressions
- It automatically converts values to string when displaying

✅ Basic Usage
```
print("Hello World")
print(10)
print("Age:", 25)
```

🔹 Printing Multiple Values
name = "Imran"
age = 25

print("Name:", name, "Age:", age)

👉 Output:

```Name: Imran Age: 25```

### ⚙️ Important Parameters of print()
#### 🔹 1. sep (Separator)

Defines how multiple values are separated

```print("A", "B", "C", sep="-")```

👉 Output:

```A-B-C```

#### 🔹 2. end (Ending Character)

Controls what is printed at the end
```
print("Hello", end=" ")
print("World")
```
👉 Output:
```Hello World```

🔹 Default Behavior
```
print("Hello")
print("World")
```
👉 Output:
```
Hello
World
```
👉 **Because default end = "\n" (new line)**

---

### 📌 Output Formatting

Formatting helps display output in a clear and readable way

#### 🔹 Method 1: Using Comma ,
```
name = "Imran"
age = 25

print("Name:", name, "Age:", age)
```

👉 Simple and beginner-friendly

#### 🔹 Method 2: Using + (Concatenation)
```
name = "Imran"
print("Hello " + name)
```
⚠️ **Only works with strings**

print("Age: " + str(25))   # must convert number to string

#### 🔹 Method 3: format() Method
```
name = "Imran"
age = 25

print("My name is {} and I am {} years old".format(name, age))
```

#### 🔹 Method 4: f-Strings (Best ⭐)

Introduced in Python 3.6

```
name = "Imran"
age = 25

print(f"My name is {name} and I am {age} years old")
```
f-strings are powerful, because:
-Clean and readable
-Can include variables + expressions
```
a = 10
b = 5

print(f"Sum = {a + b}")
```
---

### Formatting Numbers using f-Strings

#### 🔹 Basic Syntax

```f"{value:format_specifier}"```

#### 🔹 1.1 Decimal Precision

Example:
```
pi = 3.1415926535

print(f"{pi:.2f}")
```

👉 Output:

```3.14```

💡 Explanation

.2f → 2 decimal places

f → float

Examples
```
num = 5

print(f"{num:.2f}")
```

👉 Output:

```5.00```

#### 🔹 1.2 Width & Alignment
````
num = 25

print('*****')
print(f"{num:5}")
````
👉 Output:
```
*****
   25
```
##### Alignment Types
```
print('*****')
print(f"{25:<5}")  # Left
print(f"{25:>5}")  # Right
print(f"{25:^5}")  # Center
print('*****')
```
👉 Output:
```
*****
25   
   25
 25  
*****
```

#### 🔹 1.3 Zero Padding
```
num = 7

print(f"{num:05}")
```
👉 Output:

```00007```

### 🔹 1.4 Comma Separator
```
num = 1000000

print(f"{num:,}")
```

👉 Output:

```1,000,000```

### 🔹 1.5 Percentage Formatting
```
value = 0.85

print(f"{value:.2%}")
```
👉 Output:

```85.00%```

### 🔹 1.6 Scientific Notation
```
num = 123456

print(f"{num:.2e}")
```
👉 Output:

```1.23e+05```

### 🔹 1.7 Combining Everything
```
num = 12345.6789

print(f"{num:,.2f}")
```

👉 Output:

```12,345.68```

---

## 📌 Combined Example (Real Use)
```
name = input("Enter your name: ")
age = int(input("Enter your age: "))
height = float(input("Enter your height: "))

print(f"\n--- User Information ---")
print(f"Name   : {name}")
print(f"Age    : {age}")
print(f"Height : {height:.2f}")
print(f"In 5 years, age will be {age + 5}")
```

---

## ⚡ Quick Summary
- input() → takes input (always string)
- print() → displays output
- sep → controls separator
- end → controls line ending
- int(), float(), str() → type conversion
- f-strings → best for formatting

---

## 🎯 Practice Problems
# Problem 1
name = input("Enter name: ")
print(f"Welcome {name}")

# Problem 2
num = int(input("Enter a number: "))
print(f"Square = {num * num}")

# Problem 3
a, b = map(int, input("Enter two numbers: ").split())
print(f"Sum = {a + b}, Difference = {a - b}")

---