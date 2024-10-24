#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Seed the random number generator
    std::srand(static_cast<unsigned int>(std::time(0)));

    // Generate a random number between 1 and 100
    int targetNumber = std::rand() % 100 + 1;
    int playerGuess = 0;
    int attempts = 0;

    std::cout << "Welcome to the Number Guessing Game!" << std::endl;
    std::cout << "I have selected a number between 1 and 100." << std::endl;
    std::cout << "Can you guess what it is?" << std::endl;

    // Loop until the player guesses the correct number
    while (playerGuess != targetNumber) {
        std::cout << "Enter your guess: ";
        std::cin >> playerGuess;
        attempts++;

        // Check the player's guess
        if (playerGuess < targetNumber) {
            std::cout << "Too low! Try again." << std::endl;
        } else if (playerGuess > targetNumber) {
            std::cout << "Too high! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You've guessed the number " << targetNumber 
                      << " in " << attempts << " attempts!" << std::endl;
        }
    }
// end of pragram
    return 0;
}
