# Rock-Paper-Scissor-Game
#This is a simple Rock-Paper-Scissors game built using Python. The player selects Rock, Paper, or Scissors, and the computer randomly chooses its move. The game then #compares both choices and displays the result: Win, Lose, or Draw.

import random

# Choices list
game_images = ["Rock", "Paper", "Scissors"]

# Asking user for their choice
user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors:\n"))

# Check if user entered a valid number
if user_choice >= 0 and user_choice <= 2:
    print("You chose:", game_images[user_choice])

    # Computer makes a random choice
    computer_choice = random.randint(0, 2)
    print("Computer chose:", game_images[computer_choice])

    # Game rules
    if user_choice == computer_choice:
        print("It's a draw!")
    elif user_choice == 0 and computer_choice == 2:
        print("You win!")
    elif user_choice == 2 and computer_choice == 0:
        print("You lose!")
    elif user_choice > computer_choice:
        print("You win!")
    else:
        print("You lose!")
else:
    print("You typed an invalid number. You lose!")

