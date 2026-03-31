# 🧪 01-04: Basic Syntax

Python syntax is the set of rules that define how Python code is written and interpreted.

---

## 🖨️ 1. print() Function

Used to display output on the screen.

### Example:
```python
print("Hello, World!")
Explanation:
print() is a built-in function
Text inside quotes is called a string
Output:
Hello, World!
💬 2. Comments

Comments are used to explain code. They are ignored by Python.

Single-line comment:
# This is a comment
print("Hello")
Inline comment:
print("Hello")  # This prints Hello
📌 3. Indentation (VERY IMPORTANT)

Python uses indentation (spaces) to define blocks of code.

Example:
age = 18

if age >= 18:
    print("Adult")
Explanation:
The indented line belongs to the if block
Without indentation → ❌ Error
❌ Wrong:
if age >= 18:
print("Adult")
🔤 4. Case Sensitivity

Python is case-sensitive.

Example:
name = "Imran"
Name = "Jahid"

print(name)
print(Name)

👉 These are treated as different variables

📦 5. Statements & Lines

Each line is usually one statement.

Example:
x = 10
y = 20
print(x + y)
➕ 6. Multiple Statements in One Line

You can write multiple statements using ; (not recommended).

x = 10; y = 20; print(x + y)

👉 Better to use separate lines for readability

🔗 7. Line Continuation

Used to break long lines into multiple lines.

Using backslash:
total = 10 + 20 + 30 + \
        40 + 50
Using parentheses (recommended):
total = (10 + 20 + 30 +
         40 + 50)
🔠 8. Strings and Quotes

Strings can be written using:

"Hello"
'Hello'
Multi-line string:
text = """This is
a multi-line
string"""
🎯 9. Basic Output Formatting
Example:
name = "Imran"
age = 25

print("Name:", name)
print(f"My age is {age}")