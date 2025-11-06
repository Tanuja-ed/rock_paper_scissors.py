# rock_paper_scissors.py
This is a Rock Paper Scissors game made in Python where the user plays against the computer using random choices.

import random

print("Let's play Rock, Paper, Scissors!")

select = ["rock", "paper", "scissors"]
computer = random.choice(select)
user = input("Enter rock, paper, or scissors: ").lower()

print("\nYou chose:", user)
print("Computer chose:", computer)

# define what each move can beat
win_rules = {
    "rock": "scissors",
    "paper": "rock",
    "scissors": "paper"
}

if user not in select:
    print("Invalid choice! Please enter rock, paper, or scissors only >.<")
elif user == computer:
    print("It's a tie! 😐")
elif win_rules[user] == computer:
    print("You win! 🎉")
else:
    print("Computer wins! ")
