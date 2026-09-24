# ABC-Repository-
# import random

def guess_the_number():
    # Generate a random secret number between 1 and 100
    secret_number = random.randint(1, 100)
    attempts = 0
    
    print("✨ Welcome to the Number Guessing Game! ✨")
    print("I'm thinking of a number between 1 and 100.")
    
    # Loop continuously until the user guesses correctly
    while True:
        try:
            # Take input from the user and convert it to an integer
            guess = int(input("Take a guess: "))
            attempts += 1
            
            # Check the user's guess against the secret number
            if guess < secret_number:
                print("Too low! 📉 Try again.")
            elif guess > secret_number:
                print("Too high! 📈 Try again.")
            else:
                print(f"🎉 Congratulations! You found the number in {attempts} attempts!")
                break # Exit the loop when the guess is correct
                
        except ValueError:
            # Handle cases where the user inputs something that isn't a number
            print("❌ Invalid input. Please enter a valid number.")

# Run the game
if __name__ == "__main__":
    guess_the_number()

