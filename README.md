<h1 align="center">Hangman Game</h1>

                                                     ____
                                                    |    |
                                                    |    O
                                                    |   /|\
                                                    |   / \
                                                   _|_
                                                  |   |______
                                                  |          |
                                                  |__________|
                           

<p align="center">
  Welcome to the Hangman Game! This repository contains the code for a classic word-guessing game. Challenge yourself to guess the hidden word before you run out of lives. Have fun playing!
</p>

## Game Overview
The Hangman Game is a simple word-guessing game where players try to guess a word one letter at a time. The game provides a set of underscores representing the letters of the word to be guessed. Players need to guess letters, and if the guessed letter is present in the word, it is revealed in the correct position(s). If the guessed letter is not present, a part of the hangman is drawn. Players continue guessing until they either successfully guess the word or run out of lives.

## How to Play
To play the Hangman Game, follow these steps:
1. Clone this repository: `git clone https://https://github.com/034adarsh/Hangman-Final`
2. Install the necessary dependencies.
3. Run the `hangman.py` script.
4. Guess a letter each round by entering it in the command line.
5. Keep guessing until you either guess the word correctly or lose all your lives.

## Prerequisites
- Python 3
- Libraries: random

## Usage
1. Import the required modules:
    ```python
    import random
    from hangman_words import word_list
    from hangman_art import logo, stages
    ```
2. Generate a random word from the `word_list`:
    ```python
    chosen_word = random.choice(word_list)
    word_length = len(chosen_word)
    ```
3. Set up the game by initializing variables:
    ```python
    end_of_game = False
    lives = 6
    ```
4. Print the game logo:
    ```python
    print(logo)
    ```
5. Run the game loop:
    ```python
    while not end_of_game:
        guess = input("Guess a letter: ").lower()
        ...
    ```
6. Check the guessed letter, update the game display, and track lives:
    ```python
    if guess in display:
        print(f"You've already guessed {guess}")
        ...
    ```
7. Print the current game display:
    ```python
    print(f"{' '.join(display)}")
    ```
8. Check if the player wins or loses:
    ```python
    if "_" not in display:
        end_of_game = True
        print("You win.")
        ...
    if lives == 0:
        end_of_game = True
        print("You lose.")
    ```
9. Print the hangman ASCII art:
    ```python
    print(stages[lives])
    ```

## Customization
You can customize the Hangman Game by modifying the `word_list` in `hangman_words.py` to include your own set of words. Additionally, you can modify the ASCII art in `hangman_art.py` to create your own hangman visualizations.

## Contributing
Contributions to enhance the Hangman Game are always welcome. If you have any suggestions, bug fixes, or new features to add, please submit a pull request. Let's make the game even better together!

## License
This project is licensed under the [MIT License](LICENSE).

## Contact
For any questions or inquiries, feel free to reach out to us:
- **Email:** adarsh36jnp@gmail.com
