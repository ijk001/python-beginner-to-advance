# 01-07: Operators in Python

Operators are symbols or keywords used to perform operations on values and variables.

Example:
```
a = 10
b = 5

print(a + b)   # 15
```

Here, + is an operator.

---

## Types of Operators in Python

Python has several types of operators:

Arithmetic Operators
Assignment Operators
Comparison Operators
Logical Operators
Bitwise Operators
Membership Operators
Identity Operators

2. Arithmetic Operators

These are used for mathematical calculations.

Operator	Meaning	Example
+	Addition	5 + 2 → 7
-	Subtraction	5 - 2 → 3
*	Multiplication	5 * 2 → 10
/	Division	5 / 2 → 2.5
//	Floor Division	5 // 2 → 2
%	Modulus (remainder)	5 % 2 → 1
**	Exponent (power)	5 ** 2 → 25
Example
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
3. Assignment Operators

These are used to assign values to variables.

Operator	Example	Same as
=	x = 5	assign 5 to x
+=	x += 3	x = x + 3
-=	x -= 3	x = x - 3
*=	x *= 3	x = x * 3
/=	x /= 3	x = x / 3
//=	x //= 3	x = x // 3
%=	x %= 3	x = x % 3
**=	x **= 3	x = x ** 3
Example
x = 10
x += 5
print(x)   # 15

x *= 2
print(x)   # 30

x -= 4
print(x)   # 26
4. Comparison Operators

These compare two values and return True or False.

Operator	Meaning	Example
==	Equal to	5 == 5 → True
!=	Not equal to	5 != 3 → True
>	Greater than	5 > 3 → True
<	Less than	5 < 3 → False
>=	Greater than or equal to	5 >= 5 → True
<=	Less than or equal to	5 <= 2 → False
Example
a = 10
b = 20

print(a == b)   # False
print(a != b)   # True
print(a < b)    # True
print(a > b)    # False
print(a <= 10)  # True
print(b >= 15)  # True
5. Logical Operators

These are used to combine conditions.

Operator	Meaning
and	True if both conditions are True
or	True if at least one condition is True
not	Reverses the result
Example
a = 10
b = 5

print(a > 5 and b < 10)   # True
print(a < 5 or b < 10)    # True
print(not(a > 5))         # False
Explanation
and → both sides must be true
or → at least one side must be true
not → changes True to False, and False to True
6. Bitwise Operators

These work on binary numbers (bits).

Operator	Meaning
&	AND
`	`
^	XOR
~	NOT
<<	Left shift
>>	Right shift
Example
a = 5    # 0101
b = 3    # 0011

print(a & b)   # 1
print(a | b)   # 7
print(a ^ b)   # 6
print(a << 1)  # 10
print(a >> 1)  # 2

For beginner notes, you can mention these briefly and learn them deeply later.

7. Membership Operators

These check whether a value exists in a sequence such as string, list, or tuple.

Operator	Meaning
in	Value exists
not in	Value does not exist
Example
nums = [1, 2, 3, 4]

print(2 in nums)       # True
print(7 in nums)       # False
print(7 not in nums)   # True

With string:

text = "python"

print("py" in text)      # True
print("java" not in text)  # True
8. Identity Operators

These check whether two variables refer to the same object in memory.

Operator	Meaning
is	Same object
is not	Not same object
Example
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)      # True
print(a is c)      # False
print(a == c)      # True
Important
== checks whether the values are equal
is checks whether they are the same object
9. Operator Precedence

Operator precedence means which operator is evaluated first in an expression.

Example:

print(2 + 3 * 4)

Output:

14

Why?

Because * has higher precedence than +.

So Python does:

2 + (3 * 4)
10. Common Operator Precedence Order

From higher precedence to lower precedence:

Precedence	Operators
Highest	()
	**
	+x, -x, ~x
	*, /, //, %
	+, -
	<<, >>
	&
	^
	`
	==, !=, >, <, >=, <=, is, is not, in, not in
	not
	and
Lowest	or
11. Associativity

When two operators have the same precedence, Python decides the order using associativity.

Left to Right Associativity

Most operators are evaluated from left to right.

Examples:

print(10 - 3 - 2)

This means:

(10 - 3) - 2

Output:

5

Another example:

print(20 / 5 * 2)

This means:

(20 / 5) * 2

Output:

8.0

So these are generally left to right:

*, /, //, %
+, -
comparison chaining works specially
and, or
Right to Left Associativity

Some operators are evaluated from right to left.

Exponent Operator **
print(2 ** 3 ** 2)

This means:

2 ** (3 ** 2)

Output:

512

Because:

3 ** 2 = 9
2 ** 9 = 512

So ** is right to left.

12. Examples of Precedence and Associativity
Example 1
print(5 + 2 * 3)

Step:

2 * 3 = 6
5 + 6 = 11

Output:

11
Example 2
print((5 + 2) * 3)

Step:

Parentheses first → 5 + 2 = 7
7 * 3 = 21

Output:

21
Example 3
print(10 - 4 + 2)

- and + have same precedence, so go left to right:

(10 - 4) + 2 = 8

Output:

8
Example 4
print(2 ** 3 ** 2)

Go right to left:

2 ** (3 ** 2) = 2 ** 9 = 512
Example 5
print(True or False and False)

and has higher precedence than or.

So:

True or (False and False)
True or False

Output:

True
13. Comparison Chaining

Python allows chaining comparisons.

x = 5
print(1 < x < 10)   # True

This means:

1 < x and x < 10

Another example:

print(10 > 5 > 2)   # True
print(10 > 5 < 2)   # False
14. Use Parentheses for Clarity

Even if you know precedence, using parentheses makes code easier to read.

Example:

result = (a + b) * c

This is clearer than:

result = a + b * c
15. Very Important Beginner Mistakes
Mistake 1: = vs ==
x = 5      # assignment
x == 5     # comparison
= assigns value
== compares value
Mistake 2: is vs ==
a = [1, 2]
b = [1, 2]

print(a == b)   # True
print(a is b)   # False
== → same value
is → same object
Mistake 3: forgetting precedence
print(2 + 3 * 4)   # 14, not 20

Use parentheses when needed:

print((2 + 3) * 4)   # 20
16. Full Example
a = 10
b = 3
c = 2

print(a + b * c)         # 16
print((a + b) * c)       # 26
print(a > b and b > c)   # True
print(a == 10 or b == 5) # True
print(not(a < b))        # True
print(2 ** 3 ** 2)       # 512
17. Quick Summary
Types of operators
Arithmetic
Assignment
Comparison
Logical
Bitwise
Membership
Identity
Precedence
Decides which operator works first
Associativity
Decides direction of evaluation when operators have same precedence
Direction
Most operators: left to right
**: right to left
18. Practice Examples

Try to predict the output first:

print(8 + 2 * 5)
print((8 + 2) * 5)
print(20 / 5 * 2)
print(2 ** 2 ** 3)
print(True and False or True)
print(not True or False)
print(5 > 3 and 2 < 1)
Answers
18
50
8.0
256
True
False
False
19. Short Note Version
# Operators in Python

# 1. Arithmetic: +, -, *, /, //, %, **
# 2. Assignment: =, +=, -=, *=, /=
# 3. Comparison: ==, !=, >, <, >=, <=
# 4. Logical: and, or, not
# 5. Bitwise: &, |, ^, ~, <<, >>
# 6. Membership: in, not in
# 7. Identity: is, is not

# Precedence: which operator is evaluated first
# Associativity: evaluation direction when precedence is same

# Most operators: left to right
# Exponent (**): right to left