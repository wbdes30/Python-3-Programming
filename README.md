# Python-3-Programming-Project
Course 5 assignments of Python 3 Programming Specialization by University of Michigan on Coursera
## Assignment 1

By using Object-Oriented Programming (OOP), you will create a program called _WordyPy_. In WordyPy, the bot you create must try to guess a five-letter secret word based on feedback given from the game engine. For each word guess your bot makes, the WordyPy game engine will give detailed feedback which your bot can use to increase its chances of winning.

The rules of WordyPy are as follows:

1. Each guess must be a five letter English word. Only the 26 letters of the English alphabet are used, and case does
   not matter.
2. The game engine, which is written for you, generates a hidden 5 letter word called the _target word_.
3. The bot, which you must write, attempts to guess that word. It will get up to six tries.
4. The bot will be given the location of a datafile which has a list of allowable words (one per line). Your bot must
   read in this datafile and only make guesses from this datafile.
5. After each guess the system provides feedback indicating if each character is in the correct position for the target
   word, and if not, if the character is in the target word but in the wrong position.
6. The bot must be "smart" in that once it has identified the correct location of a letter in a word it must only guess
   future words where that letter is in the same position.
7. We have written tests for these requirements; you must pass those tests to pass the assignment.

#### Architecture
![alt text](https://github.com/wbdes30/Python-3-Programming/blob/main/A1/architecture.png?raw=true)

You don't have to write the `GameEngine` – we've done that for you. However, the `GameEngine` will not work until you have correctly defined the `Letter` and `Bot` classess, including their methods. You will work on those!

## Assignment 2

A more complicated version of _WordyPy_ in Assignment 1. The architecture for the software has changed a bit, here's a breakdown:

#### Architecture
![alt text](https://github.com/wbdes30/Python-3-Programming/blob/main/A2/py3_assignment2.drawio.png?raw=true)

**`GameEngine`**

The `GameEngine` class now return a `PIL.Image` object when the `play` method is called. 

**`Bot`**

The biggest change to the `Bot` class is that the `record_guess_results()` method no longer takes a list of letters, but an image. To deal with this image you need to implement two helper methods which are private (remember: if a function or method starts with an underscore in python the intention is for it to be private to the class). 

## Assignment 3: Creating a WordyPy Solver
Your job is to read in a WordyPy partial play and provide a next good guess. A good guess is one which:

- Continues to adhere to the rules of WordPy
- Does not repeat words which have already been played
- Uses the knowledge of previous guesses to pick a new good word
A module called wordy was provided to import.
