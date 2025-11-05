# Rock-Paper-Scissor-Game
This is a simple Rock-Paper-Scissors game built using Python. The player selects Rock, Paper, or Scissors, and the computer randomly chooses its move. The game then compares both choices and displays the result: Win, Lose, or Draw.

import random

game_images = ["Rock", "Paper", "Scissors"]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors:\n"))

# Check invalid input
if user_choice < 0 or user_choice > 2:
    print("You typed an invalid number. You lose!")
    exit()

print("You chose:", game_images[user_choice])

computer_choice = random.randint(0, 2)
print("Computer chose:", game_images[computer_choice])

# Game logic
if user_choice == computer_choice:
    print("Draw")
elif user_choice == 0 and computer_choice == 2:
    print("You win!")
elif user_choice == 2 and computer_choice == 0:
    print("You lose")
elif user_choice > computer_choice:
    print("You win!")
else:
    print("You lose")
