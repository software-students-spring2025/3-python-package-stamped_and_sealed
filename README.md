# Python Package Exercise

An exercise to create a Python package, build it, test it, distribute it, and use it. See [instructions](./instructions.md) for details.

## Features
*CodeJester* is a Python package designed to make coding more fun with simple text transformations and feel-good messages. It includes four features: reversing text, converting words into leetspeak, generating random compliments for developers, and generating random fortunes for developers. 

The **Reverse Text** function flips any string backward, giving a fun twist to your input. The **Leetspeak** converter transforms text into a stylized hacker-style format (e.g., "hello" becomes "h3ll0"). The **Developer Compliments** feature provides developers with encouraging messages like "Your code is a masterpiece in the making" or "You're a debugging pro," based on the type of compliment you choose (debugging, coding, or motivational). Inspired by fortune cookies, the **Fortune** function provides developers with fortunes like "Your potential is limited only by your imagination" or "First, solve the problem. Then, write the code," based on a chosen theme (inspirational, funny, or programming).  

Now matter which feature you decide to use, *CodeJester* adds a bit of positivity and entertainment to a developer's workflow.

***
## A badge showing the result of the latest build/test workflow run
![Latest Build Status](https://github.com/software-students-spring2025/3-python-package-stamped_and_sealed/actions/workflows/event-logger.yml/badge.svg)
***
## A link to *CodeJester*'s page on the PyPI website
https://test.pypi.org/project/stamped-and-sealed/
***
## How a developer who wants to import your project into their own code can do so - include documentation and code examples for all functions in your package and a link to an example Python program that uses each of them.

To use the functions from our package in your own code, you'll need to import them as follows:

```python
from stamped_and_sealed import dev_compliment, leetspeak, reverse_text, fortune_py
```

Function Documentation and Examples

### `dev_compliment(category: str) -> None`

Provides positive affirmations for developers in different categories.

**Parameters:**
- `category` (str): The category of compliment. Options include "debugging", "coding", or "motivation".

**Returns:**
- None (prints the compliment to the console)

**Example usage:**
```python
from stamped_and_sealed import dev_compliment

# Get a coding-related compliment
dev_compliment("coding")

# Get a debugging-related compliment
dev_compliment("debugging")

# Get a motivational compliment
dev_compliment("motivation")
```

### `leetspeak(text: str) -> str`

Converts normal text into leetspeak by replacing letters with numbers and symbols.

**Parameters:**
- `text` (str): The normal text to convert.

**Returns:**
- str: The text converted to leetspeak.

**Example usage:**
```python
from stamped_and_sealed import leetspeak

# Convert a simple message
normal_text = "Hello World"
leet_text = leetspeak(normal_text)
print(leet_text)  # Output: "#3||0 \\/\\/0|2|d"

# Use with user input
user_input = input("Enter text to convert: ")
converted = leetspeak(user_input)
print(f"Leetspeak version: {converted}")
```

### `reverse_text(text: str) -> str`

Reverses the characters in the provided text.

**Parameters:**
- `text` (str): The input string to reverse.

**Returns:**
- str: The reversed string.

**Example usage:**
```python
from stamped_and_sealed import reverse_text

# Reverse a simple message
original = "Python is fun"
reversed_message = reverse_text(original)
print(reversed_message)  # Output: "nuf si nohtyP"

# Create a palindrome checker
def is_palindrome(word):
    return word.lower() == reverse_text(word).lower()

print(is_palindrome("radar"))  # Output: True
print(is_palindrome("Python"))  # Output: False
```

### PyFortune Functions

#### `pyfortune.generate_fortune(theme: str = "inspirational") -> str`

Generates a fortune cookie message from the specified theme.

**Parameters:**
- `theme` (str, optional): The theme of fortune to generate. Options include "inspirational", "funny", or "programming". Default is "inspirational".

**Returns:**
- str: A fortune message from the selected theme.

**Example usage:**
```python
from stamped_and_sealed import fortune_py

# Get a default (inspirational) fortune
fortune = fortune_py.generate_fortune()
print(fortune)

# Get a funny fortune
funny_fortune = fortune_py.generate_fortune("funny")
print(funny_fortune)

# Get a programming-related fortune
prog_fortune = fortune_py.generate_fortune("programming")
print(prog_fortune)
```

#### `pyfortune.format_fortune(message: str, format_type: str = "plain") -> str`

Formats a message with the specified formatting style.

**Parameters:**
- `message` (str): The message to format.
- `format_type` (str, optional): The formatting style to apply. Options include "plain" or "ascii_box". Default is "plain".

**Returns:**
- str: The formatted message.

**Example usage:**
```python
from stamped_and_sealed import fortune_py

message = "Success is not final, failure is not fatal."

# Format with plain style (no special formatting)
plain = fortune_py.format_fortune(message, "plain")
print(plain)

# Format with ASCII box
boxed = fortune_py.format_fortune(message, "ascii_box")
print(boxed)
```

#### `pyfortune.get_random_fortune() -> str`

Generates a random fortune from any available theme.

**Parameters:**
- None

**Returns:**
- str: A random fortune message.

**Example usage:**
```python
from stamped_and_sealed import fortune_py

# Get a random fortune
fortune = fortune_py.get_random_fortune()
print(fortune)

# Get and format a random fortune
random_fortune = fortune_py.get_random_fortune()
formatted = fortune_py.format_fortune(random_fortune, "ascii_box")
print(formatted)
```
See [Example_Project](./Example_Project) for a python project that uses all these functions
***
## How a developer who wants to contribute to CodeJester can set up the virtual environment, install dependencies, and build and test your package for themselves

1. Fork and Clone the Repository: Start by forking the repository on GitHub and cloning it locally:
```
git clone https://github.com/software-students-spring2025/3-python-package-stamped_and_sealed.git
cd 3-python-package-stamped_and_sealed
```
2. Set Up the Virtual Environment: Use pipenv to manage dependencies and virtual environments. Install pipenv (if you haven’t already) and set up the environment
```
python3 -m pip install pipenv
pipenv install
pip install -e .
```
3. Build and Test the Package: Before making any changes, run tests to ensure the package is working correctly by running `pytest`
4. Create a New Feature Branch: Before making any changes, create a new branch with `git checkout -b feature-new-function`
5. Make Your Changes and Commit: Once you have implemented your changes, stage and commit them:
```
git add .
git commit -m "Added new feature"
```
5. Push Your Changes and Create a Pull Request: Push your changes to your forked repository with  `git push origin feature-new-function`

***
## *Stamped and Sealed* Teammates
- [Ethan Yu](https://github.com/ethanyuu910) 
- [Isha Gopal](https://github.com/ishy04)
- [Jennifer Huang](https://github.com/jennhng) 
- [Lana Davydov](https://github.com/lanadavydov)
- [Tarini Mathur](https://github.com/tmathur2005)

***
## Instructions for how to configure and run all parts of CodeJester for any developer on any platform
These instructions will help developers set up and run the package on any platform (Windows, macOS, or Linux).

### Installation and Setup

1. **Clone the Repository**:
   - Clone the repository to your local machine:
     ```bash
     git clone https://github.com/your-username/3-python-package-stamped_and_sealed.git
     cd 3-python-package-stamped_and_sealed
     ```
2. **Set Up a Virtual Environment**:
   - Create a virtual environment (recommended):
     ```bash
     python -m venv venv
     ```
   - Activate the virtual environment:
     - On Windows:
       ```bash
       venv\Scripts\activate
       ```
     - On macOS/Linux:
       ```bash
       source venv/bin/activate
       ```
3. **Install Dependencies**:
   - Install the required dependencies using `pip`:
     ```bash
     pip install -r requirements.txt
     ```
4. **Run the Package**:
   - You can now use the `CodeJester` package in your Python scripts or interactive sessions. For example:
     ```python
     from stamped_and_sealed.reverse_text import reverse_text
     from stamped_and_sealed.dev_compliments import dev_compliment
     from stamped_and_sealed.fortune_py import fortune
     from stamped_and_sealed.leetspeak import leetspeak

     print(reverse_text("hello"))
     print(dev_compliment("coding"))
     print(fortune())
     print(leetspeak("hello"))
     ```
5. **Run the Example Script**:
   - An example script (`example.py`) is provided to demonstrate the package's functionality. Run it using:
     ```bash
     python example.py
     ```
6. **Run Tests**:
   - To verify that everything is working correctly, run the tests:
     ```bash
     pytest tests/
     ```

***
## Instructions for how to set up any environment variables and import any starter data into the database, as necessary, for the system to operate correctly when run
### Environment Variables
1. **Create a `.env` File**:
   - In the root directory of the project, create a `.env` file:
     ```bash
     touch .env
     ```
2. **Add Required Variables**:
   - Open the `.env` file and add the necessary variables. For example:
     ```plaintext
     API_KEY=your_api_key_here
     DATABASE_URL=your_database_url_here
     ```
3. **Load Environment Variables**:
   - Install the `python-dotenv` package to load the variables automatically:
     ```bash
     pip install python-dotenv
     ```
   - In your Python code, load the variables using:
     ```python
     from dotenv import load_dotenv
     import os

     load_dotenv()
     api_key = os.getenv("API_KEY")
     database_url = os.getenv("DATABASE_URL")
     ```
### Importing Starter Data
1. **Set Up the Database**:
   - Ensure your database is running and accessible. Update the `.env` file with the correct `DATABASE_URL`.
2. **Run the Data Import Script**:
   - If a script is provided to import starter data, run it using:
     ```bash
     python scripts/import_data.py
     ```
3. **Verify the Data**:
   - Check the database to ensure the starter data has been imported correctly.
