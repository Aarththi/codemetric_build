# codemetric_build
Task Title: Build Calculator
Description :
This task helps you learn how to build a basic calculator using Python that performs arithmetic operations like:
Addition (+)
Subtraction (-)
Multiplication (*)
Division (/)

Python Concepts Used;
Functions---A function is a block of reusable code.
You define functions like add(a, b) to organize your logic clearly.
Input/Output (I/O)
input() is used to take user input.
print() displays the result to the user.
Loops (while)
The loop allows the user to perform calculations multiple times until they choose to exit.
Conditionals (if-elif-else)
These are used to check which operation the user wants to do.
Exception Handling (try-except)
Prevents the program from crashing if the user types something wrong (like a letter instead of a number or dividing by zero).
f-strings
These are used for clean and formatted output like:
python
Copy
Edit
print(f"{num1} + {num2} = {result}")
Calculator Code Explanation:---
python
Copy
Edit
def add(a, b):
    return a + b
 This function takes two numbers and returns their sum.

python
Copy
Edit
def subtract(a, b):
    return a - b
This returns the difference of the two numbers.

python
Copy
Edit
def multiply(a, b):
    return a * b
This returns the product (multiplication result) of the numbers.

python
Copy
Edit
def divide(a, b):
    return a / b
This returns the quotient (result of division).

python
Copy
Edit
print("Welcome to the Python Calculator!")
print("Type 'exit' at any time to quit.\n")
This prints a welcome message and tells the user how to exit the calculator.

Main Loop Starts
python
Copy
Edit
while True:
This starts a loop that keeps repeating until the user types 'exit'.
Getting First Number
python
Copy
Edit
    try:
        num1 = input("Enter first number: ")
        if num1.lower() == 'exit':
            break
        num1 = float(num1)
input() asks the user to type a number.

.lower() turns any capital letters into lowercase.

If the user types "exit", the loop stops using break.

float(num1) converts the input into a decimal number.

Get the Operation
python
Copy
Edit
        op = input("Enter operation (+, -, *, /): ")
        if op.lower() == 'exit':
            break
        if op not in ['+', '-', '*', '/']:
            print("Invalid operator. Try again.\n")
            continue
Asks the user to enter an operator.

If it's not one of the valid symbols, it gives an error and goes to the next loop.

Getting Second Number
python
Copy
Edit
        num2 = input("Enter second number: ")
        if num2.lower() == 'exit':
            break
        num2 = float(num2)
Works just like num1. Takes the second number.

Perform Operation
python
Copy
Edit
        if op == '+':
            result = add(num1, num2)
        elif op == '-':
            result = subtract(num1, num2)
        elif op == '*':
            result = multiply(num1, num2)
        elif op == '/':
            if num2 == 0:
                raise ZeroDivisionError("Cannot divide by zero.")
            result = divide(num1, num2)
This block checks which operator the user chose.

It then calls the correct function (add, subtract, etc.).

Before dividing, it checks if num2 is 0 (to prevent division by zero).

Show the Result
python
Copy
Edit
        print(f"Result: {num1} {op} {num2} = {result}\n")
Uses an f-string to display the calculation clearly.

How to Run the Script:
Save the Python code as calculator.py.

Open terminal or command prompt.

Navigate to the folder where it’s saved.

Type and run:
nginx
Copy
Edit
python calculator.py

Output examples:
Welcome to the Python Calculator!
Enter first number: 10  
Enter operation (+, -, *, /): /  
Enter second number: 2  
Result: 10.0 / 2.0 = 5.0

Enter first number: abc
Invalid input. Please enter numeric values only.

 So I Learned:---
How to use functions to break your code into parts.

How to use loops to keep a program running.

How to handle errors using try-except.

Why input validation is important.

How to format and display output using f-strings.

