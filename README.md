# Number Guessing Game


Welcome to my **Number Guessing Game**
This is a simple **number guessing game** made using Python.
In this game, the computer chooses a random number and you have to guess it.
The game tells you whether your guess is **above or below** the random number.
This project is made for beginners who are learning Python and want to practice:

* Variables
* `input()`
* `print()`
* `if`, `elif`, and `else`
* `while` loop
* `break`
* `continue`
* `int()`
* `.isdigit()`
* `random` module
* `random.randint()`
* Comparison operators
* Basic game logic

----------------------------------------------------------------------------------------

## How the Game Works

The game starts by asking you to enter a number.
```python
top_of_range = input("Type a number: ")
```
For example:
```text
Type a number: 100
```
The computer will then choose a random number between `0` and the number you entered.
For example:
```text
Random number = 57
```
You don't know the random number.
Now you have to guess the number.
```text
Make a guess: 30
You were below the number!
Make a guess: 80
You were above the number!
Make a guess: 57
You got it!
```
At the end, the game tells you how many guesses you needed.
```text
You got it in 3 guesses
```
--------------------------------------------------------------------------------------

# Game Story
You are playing a number guessing game.
First, the game asks you for the highest number.
```text
Type a number:
```
The computer randomly chooses a number between:
```text
0
```
and:
```text
Your number
```
Now you have to find the secret number.
You can keep guessing until you find the correct number.
-----------------------------------------------------------------------------------------------

# Entering the Maximum Number
The game asks:
```python
top_of_range = input("Type a number: ")
```
For example:
```text
Type a number: 100
```
The number `100` becomes the maximum number for the game.
The computer can now choose any number between:
```text
0 to 100
```
------------------------------------------------------------------------------------------------

# Checking the Input
The game checks whether the user entered a number.
```python
if top_of_range.isdigit():
```
If the user enters a number:
```text
100
```
the program continues.
If the user enters something like:
```text
hello
```
the game displays:
```text
Please type a number next time.
```
Then the game stops.
---------------------------------------------------------------------------------------------

# Creating the Random Number
The game uses:
```python
random_number = random.randint(0, top_of_range)
```
`random.randint()` generates a random number.
For example, if:
```text
top_of_range = 100
```
the computer can randomly choose:
```text
25
57
89
3
100
```
The player does not know which number was selected.
--------------------------------------------------------------------------------------------

# Making a Guess
The game asks:
```python
user_guess = input("Make a guess: ")
```
For example:
```text
Make a guess: 50
```
The program then checks the guess.
There are three possible situations:
```text
Guess = Random Number
Guess > Random Number
Guess < Random Number
```
-------------------------------------------------------------------------------------------------------------

# If You Guess Correctly
If your guess is equal to the random number:
```python
if user_guess == random_number:
```
The game prints:
```text
You got it!
```
You win the game! 
Then the game uses:
```python
break
```
to stop the loop.
----------------------------------------------------------------------------

# If Your Guess is Too High
If your guess is greater than the random number:
```python
elif user_guess > random_number:
```
The game prints:
```text
You were above the number!
```
For example:
```text
Random number = 50
Your guess = 80
```
Because:
```text
80 > 50
```
your guess is too high.


# If Your Guess is Too Low
If your guess is smaller than the random number:
```python
else:
    print("You were below the number!")
```
For example:
```text
Random number = 50
Your guess = 20
```
Because:
```text
20 < 50
```
your guess is too low.
----------------------------------------------------------------------------------------------------

# Guess Counter
The game also counts how many guesses you make.
At the beginning:
```python
guesses = 0
```
Every time you make a guess:
```python
guesses += 1
```
This means:
```python
guesses = guesses + 1
```
For example:
```text
First guess  → 1
Second guess → 2
Third guess  → 3
Fourth guess → 4
```
When you find the correct number, the game displays:
```text
You got it in 4 guesses
```
------------------------------------------------------------------------------------------------

# while Loop
The game uses
```python
while True:
```
This creates a loop that keeps asking the player for guesses.
The loop continues until the player finds the correct number.
When the correct number is found:
```python
break
```
stops the loop.
-------------------------------------------------------------------------------------------------

# Using continue
The game uses
```python
continue
```
when the player enters something that is not a number.
For example:
```text
Make a guess: hello
Please type a number next time.
```
Instead of ending the game, `continue` goes back to the beginning of the loop.
Then the game asks:
```text
Make a guess:
```
again.
---------------------------------------------------------------------------------------------

# Python Concepts Used

## 1. Variables
The game uses variables such as:
```python
top_of_range = 100
random_number = 57
guesses = 0
```
Variables are used to store information.
For example:
```python
guesses = 0
```
stores the number of guesses.

## 2. input()
`input()` is used to take information from the player.
Example
```python
user_guess = input("Make a guess: ")
```
The player can type:
```text
50
```
The program stores the answer in:
```text
user_guess
```

## 3. print()
`print()` displays information on the screen.
Example:
```python
print("You got it!")
```
Output:
```text
You got it!
```

## 4. if Statement
The `if` statement checks a condition.
Example:
```python
if user_guess == random_number:
    print("You got it!")
```
This means:
> If the user's guess is equal to the random number, print "You got it!"

## 5. elif
`elif` means **else if**.
Example:
```python
if user_guess == random_number:
    print("You got it!")
elif user_guess > random_number:
    print("You were above the number!")
```
If the first condition is false, Python checks the `elif` condition.

## 6. else
`else` runs when the previous conditions are false.
Example:
```python
else:
    print("You were below the number!")
```
If the guess is not equal to the random number and is not greater than it, it must be smaller.

## 7. .isdigit()
`.isdigit()` checks whether the input contains digits.
Example:
```python
"100".isdigit()
```
returns:
```text
True
```
But:
```python
"hello".isdigit()
```
returns:
```text
False
```
This helps the game check whether the player entered a number.

## 8. int()
`input()` gives us a string.
So the game converts the input into an integer:
```python
top_of_range = int(top_of_range)
```
For example:
```text
"100"
```
becomes:
```text
100
```
This allows Python to compare and work with the number.

## 9. random.randint()
The game uses:
```python
random.randint(0, top_of_range)
```
This generates a random integer between the starting and ending numbers.
For example:
```python
random.randint(0, 100)
```
could give:
```text
37
```
or:
```text
84
```
or:
```text
100
```
-----------------------------------------------------------------------------------------------------------

# Game Flow
The game can be understood like this:
```text
                 START
                   |
          Enter Maximum Number
                   |
            Check the Input
              /         \
            NO           YES
            |             |
           EXIT      Generate Random
                         Number
                           |
                     Make a Guess
                           |
                   Is it a Number?
                    /          \
                  NO            YES
                  |              |
             Try Again       Compare Guess
                                |
                    ┌───────────┼───────────┐
                    ↓           ↓           ↓
                  Equal       Greater      Lower
                    |           |            |
                   WIN       Too High      Too Low
                    |
                  BREAK
                    |
              Show Guesses
                    |
                   END
```
----------------------------------------------------------------------------------------------------

# Project Structure
The project is very simple:
```text
Number-Guessing-Game/
│
├── guessing_game.py
│
└── README.md
```

### `guessing_game.py`
Contains the complete Python number guessing game.

### `README.md`
Contains information about the project, gameplay, installation, and Python concepts.

------------------------------------------------------------------------------------------------------

#  Technologies Used

* **Python**
* **VS Code / Jupyter Notebook** (recommended)
* **GitHub**

The game uses Python's built-in `random` module.
No external Python libraries are required.

# Features
* Random number generation
* User-defined number range
* Interactive guessing
* High and low hints
* Guess counter
* Invalid input handling
* Unlimited guesses
* Winning condition
* `while` loop practice
* `break` and `continue` practice

# Future Improvements
I can improve this game in the future by adding:
* Difficulty levels
* Limited number of attempts
* Score system
* High-score system
* Easy / Medium / Hard mode
* Timer
* Hint system
* Play again option
* Multiplayer mode
* Graphical interface
* Sound effects

# What I Learned
While making this project, I practiced how to:
```text
Take user input
      ↓
Check whether the input is valid
      ↓
Convert string into integer
      ↓
Generate a random number
      ↓
Use if / elif / else
      ↓
Use while loop
      ↓
Compare two numbers
      ↓
Use break and continue
      ↓
Count the number of guesses
```
This project helped me understand how basic Python programming can be used to create an interactive game.

-----------------------------------------------------------------------------------------

# Author
**Dinesh Chahar**
Beginner Python Developer!!
Currently learning:
* Python
* C#
* DSA
* OOP
* Game Development

## If You Like This Project
If you found this project interesting, you can:------>>> Star the repository 

### Thanks for Playing!
**Can you guess the secret number? **
**Keep guessing until you get it! **
