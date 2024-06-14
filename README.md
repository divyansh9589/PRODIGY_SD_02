# PRODIGY_SD_02
# Create a Guessing Game

import random

def main():
    # Generate a random number between 1 and 100
    random_number = random.randint(1, 100)
    attempts = 0
    guessed = False

    print("Welcome to the Number Guessing Game!")
    print("I have selected a random number between 1 and 100.")
    print("Try to guess it!")

    # Loop until the user guesses the correct number
    while not guessed:
        try:
            # Prompt the user to enter their guess
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            # Compare the guess to the generated number
            if guess < random_number:
                print("Too low! Try again.")
            elif guess > random_number:
                print("Too high! Try again.")
            else:
                guessed = True
                print(f"Congratulations! You've guessed the number {random_number} in {attempts} attempts.")
        except ValueError:
            # Handle the case where the user does not enter an integer
            print("Invalid input. Please enter an integer.")

main()
