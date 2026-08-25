# 🎯 Word Guessing Game

A simple word guessing game made using Python and Object-Oriented Programming (OOP).

In this game, the player chooses a difficulty level and tries to guess a randomly selected word using the given hints. The player gets 5 chances to guess the correct word.

---

## 🎮 Features

* Three difficulty levels: Easy, Medium, and Hard
* Random word selection
* 3 hints for each word
* 5 chances to guess the word
* Different scores for different difficulty levels
* Score depends on how quickly the word is guessed
* Option to play the game again
* Input validation for difficulty selection

---

## 🕹️ How the Game Works

1. The player selects a difficulty level.
2. The game randomly selects a word from that level.
3. A hint is shown to the player.
4. The player enters a guess.
5. If the guess is wrong, another chance is given.
6. The player gets a maximum of 5 chances.
7. If the guess is correct, the score is calculated.
8. If all attempts are used, the correct word is displayed.
9. After the game ends, the player can choose to play again.

---

## 📚 Word Bank

The words and their hints are stored in a nested dictionary.

### Easy

* cat
* bat
* apple
* ball

### Medium

* kitchen
* cutlery
* rainbow
* spices

### Hard

* architecture
* algorithm
* psychology
* astronomy

Each word has 3 hints.

---

## 💯 Scoring System

The score depends on the difficulty level and the chance on which the player guesses the word.

### Easy

| Guess      | Score |
| ---------- | ----: |
| 1st chance |    30 |
| 2nd chance |    24 |
| 3rd chance |    18 |
| 4th chance |    12 |
| 5th chance |     6 |

### Medium

| Guess      | Score |
| ---------- | ----: |
| 1st chance |    50 |
| 2nd chance |    40 |
| 3rd chance |    30 |
| 4th chance |    20 |
| 5th chance |    10 |

### Hard

| Guess      | Score |
| ---------- | ----: |
| 1st chance |    70 |
| 2nd chance |    56 |
| 3rd chance |    42 |
| 4th chance |    28 |
| 5th chance |    14 |

The earlier the player guesses the correct word, the higher the score.

---

## 🧠 OOP Concepts Used

I used a class called `WordGuessingGame` to manage the game.

### Class

```python
class WordGuessingGame:
```

### Constructor

The `__init__()` method is used to initialize the game variables.

```python
def __init__(self):
    self.difficulty = None
    self.word = None
    self.chances = 5
    self.score = 0
```

### Methods

Different parts of the game are handled using different methods:

* `choose_difficulty()` → selects the difficulty level
* `select_word()` → randomly selects a word
* `calculate_score()` → calculates the score
* `guess_word()` → handles the guessing process

This helped me keep the game logic organized inside the class.

---

## 🔄 Hint System

Each word has 3 hints.

I used the modulo operator `%` to select hints:

```python
hint = self.words[self.difficulty][self.word][chance % 3]
```

This makes the hint index repeat safely when the number of chances becomes greater than the number of hints.

For example:

```text
Chance 0 → Hint 1
Chance 1 → Hint 2
Chance 2 → Hint 3
Chance 3 → Hint 1
Chance 4 → Hint 2
```

---

## 🛠️ Technologies Used

* Python 3
* `random` module
* Jupyter Notebook / Python

No external libraries are required.

---

## ▶️ How to Run

Clone the repository:

```bash
git clone <your-repository-link>
```

Go to the project folder:

```bash
cd Word-Guessing-Game
```

Run the Python file:

```bash
python word_guessing_game.py
```

---

## 🖥️ Sample Output

```text
Choose your Difficulty Level:
1. Easy
2. Medium
3. Hard

Enter your difficulty level: medium

Hint: You can see it after rain.

Guess the word: rainbow

Correct! 🎉
You earned 50 points!

Selected difficulty: Medium
Your final score: 50

Do you want to play again? (yes/no): no

Thanks for playing! 🎮
```

---

## 🔮 Future Work

I want to improve this project further by adding:

* More words and hints
* A timer for each round
* A high-score system
* Saving scores using file handling
* Player name and leaderboard
* More difficulty levels
* Different types of hints
* A GUI version of the game

---

## 📖 What I Learned

While making this project, I practiced:

* Classes and objects
* `__init__()` constructor
* Instance variables
* Methods
* Nested dictionaries
* Lists
* Loops
* Conditional statements
* User input
* `random.choice()`
* String methods
* Modulo operator
* Basic game logic

---

## 👩‍💻 About the Project

This is one of my Python OOP practice projects. I made this project to understand how different Python concepts can be combined to create a small interactive game.
