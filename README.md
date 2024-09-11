# Number_Exploration_Tool

![Python Image](https://i.pinimg.com/originals/2f/9c/11/2f9c11f9e55efbf1791f12c06d60729b.jpg)

## Objective

Create a Python program that allows the user to explore their favorite numbers interactively. The program will gather the user's name and three favorite numbers, perform logical checks, and display the results in an engaging manner.

## Steps to Implement the Program

**1. Greeting the User**

- Prompt the User for Their Name:

  Start by asking the user to enter their name.

```python
name: str = input("Enter your name: ")
print(f"Enter your name: {name}")
```

**2. Gathering User's Favorite Numbers**

- Prompt the User for Three Numbers:

  Ask the user to provide three of their favorite numbers. These numbers should be stored in a list.

```python
favorite_numbers: list = []

for i in range(1, 4):
    num: int = int(input(f"Enter your favorite number {i}: "))
    print(f"Enter your favorite number {i}: {num}")
    favorite_numbers.append(num)
```

**3. Greeting the User with a Personalized Message**

- Display a Welcome Message:

  After gathering the numbers, greet the user using their name.

```python
print(f"Hello, {name}! Let's explore your favorite numbers:")
```

**4. Checking if Numbers are Even or Odd**

- Create a List of Tuples Indicating Even or Odd:

  Iterate through the list of numbers to determine if each number is even or odd, storing the result in a list of tuples.

```python
even_odd_list: list = []

for num in favorite_numbers:
    if num % 2 == 0:
        even_odd_list.append((num, "even"))
    else:
        even_odd_list.append((num, "odd"))
print(f"{even_odd_list}")
```

- Display the Even/Odd Status:

  Print the even or odd status for each number.

```python
for num, even_odd in even_odd_list:
    print(f"The number {num} is {even_odd}.")
```

**5. Creating and Displaying Tuples of Numbers and Their Squares**

- Generate Tuples of Numbers and Their Squares:

  Use a `for` loop to create tuples containing each number and its square.

```python
squares_list: list = []

for num in favorite_numbers:
    square_tuple: tuple = (num, num ** 2)
    squares_list.append(square_tuple)
print(f"{squares_list}")

for num, square in squares_list:
    print(f"The number {num} and its square: ({num}, {square})")
```

**6. Calculating and Displaying the Sum of the Numbers**

- Calculate the Sum:

  Find the sum of the three numbers.

```python
sum_of_numbers: int = sum(favorite_numbers)
```

- Display the Sum with an Encouraging Message:

  Print the sum along with an encouraging message.

```python
print(f"Amazing! The sum of your favorite numbers is: {sum_of_numbers}")
```

**7. Checking if the Sum is a Prime Number**

- Determine if the Sum is Prime:

  Implement a function to check if the sum is a prime number and display the appropriate message.

```python
def is_prime(n):
    if n <= 1:
        return False
    if n <= 3:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True

if is_prime(sum_of_numbers):
    print(f"Wow, {sum_of_numbers} is a prime number!")
else:
    print(f"{sum_of_numbers} is not a prime number.")
```

```python
Enter your name: Memoona

Enter your first favorite number: 4
Enter your second favorite number: 6
Enter your third favorite number: 9

Hello, Memoona! Let's explore your favorite numbers:

The number 4 is even.
The number 6 is even.
The number 9 is odd.

The number 4 and its square: (4, 16)
The number 6 and its square: (6, 36)
The number 9 and its square: (9, 81)

Amazing! The sum of your favorite numbers is: 19

Wow, 19 is a prime number!
```

## Conclusion

This Python program is designed to be both informative and fun, providing users with the opportunity to explore their favorite numbers interactively. The logical checks, creative formatting, and engaging messages aim to make the experience enjoyable while introducing basic concepts like loops, conditionals, and mathematical operations.

[Click here to open the Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
