import random

def main():
    number_to_guess = random.randint(1, 100)  # Generate a random number between 1 and 100
    attempts = 0
    guessed_correctly = False

    print("I have generated a random number between 1 and 100. Try to guess it!")

    while not guessed_correctly:
        try:
        guess = int(input("Enter your guess: "))
        attempts += 1

        if guess < number_to_guess:
            print("Too low! Try again.")
        elif guess > number_to_guess:
            print("Too high! Try again.")
        else:
            guessed_correctly = True
            print(f"Congratulations! You guessed the number {number_to_guess} correctly in {attempts} attempts.")
        except ValueError:
            print("Invalid input. Please enter an integer.")

if __name__ == "__main__":
    main()
