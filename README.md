# Hangman_Game
This code implements a simple Hangman game using Java Swing.
The HangmanGame class extends JFrame and implements the ActionListener interface. It creates the GUI components required for the game, including labels, a text field for guessing, and a button to submit guesses.

The game logic revolves around the initializeGame(), updateHiddenWord(), and endGame() methods.

In the initializeGame() method, a random word is chosen from an array of words. A StringBuilder is used to represent the hidden word, with each character initially set to an underscore. The labels are updated to display the hidden word and the number of guesses left.

The updateHiddenWord() method is called when the player makes a guess. It checks if the guessed character is present in the word. If found, the corresponding underscore in the hidden word is replaced with the guessed character. If not found, the number of guesses left is decremented. If the number of guesses reaches zero, the game ends with a loss. If the hidden word is fully revealed, the game ends with a win.

The endGame() method is called when the game ends. It disables the input components, displays a message dialog with the game result, and then re-enables the input components for a new game.

The actionPerformed() method handles the event when the guess button is clicked or the Enter key is pressed in the guess text field. It retrieves the guess from the text field, updates the hidden word accordingly, and clears the text field.

The main() method creates an instance of HangmanGame using the SwingUtilities.invokeLater() method to ensure the GUI is created and run on the Event Dispatch Thread.

Overall, this code provides a basic implementation of a Hangman game using Java Swing, allowing the player to guess letters and track the progress of the hidden word.
