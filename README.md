import random

def number_guessing_game():
    print("Welcome to 'Guess the Number'!")
    number_to_guess = random.randint(1, 100)  # Random number between 1 and 100
    attempts = 10  # Maximum attempts

    print("You have 10 attempts to guess the number!")
    
    while attempts > 0:
        guess = int(input("Enter your guess (1-100): "))
        
        if guess < number_to_guess:
            print("Too low!")
        elif guess > number_to_guess:
            print("Too high!")
        else:
            print(f"Congratulations! You've guessed the number {number_to_guess}!")
            return
        
        attempts -= 1
        print(f"You have {attempts} attempts left.")

    print(f"Sorry, you've run out of attempts! The number was {number_to_guess}.")

if __name__ == "__main__":
    number_guessing_game()# Number-Guessing-Game
