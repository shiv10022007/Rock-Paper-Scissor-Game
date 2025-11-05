# Rock-Paper-Scissor-Game
#This is a simple Rock-Paper-Scissors game built using Python. The player selects Rock, Paper, or Scissors, and the computer randomly chooses its move. The game then #compares both choices and displays the result: Win, Lose, or Draw.

import random

# List of choices
game_images = ["Rock", "Paper", "Scissors"]

# Take user input
user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper, or 2 for Scissors:\n"))

# Check for valid input
if user_choice < 0 or user_choice > 2:
    print("You typed an invalid number. You lose!")
else:
    print(f"You chose: {game_images[user_choice]}")

    # Computer choice
    computer_choice = random.randint(0, 2)
    print(f"Computer chose: {game_images[computer_choice]}")

    # Game logic
    if user_choice == computer_choice:
        print("It's a draw!")
    elif (user_choice == 0 and computer_choice == 2) or \
         (user_choice == 1 and computer_choice == 0) or \
         (user_choice == 2 and computer_choice == 1):
        print("You win!")
    else:
        print("You lose!")

    print("You win!")

