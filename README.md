# rock_paper_scissors.py
This is a Rock Paper Scissors game made in Python where the user plays against the computer using random choices.

import random

print("Let's play Rock Paper Scissors!")

# list of choices
select = ["rock", "paper", "scissors"]

# computer's random choice
computer = random.choice(select)

# user input
user = input("Enter rock, paper, or scissors: ").lower()

print(f"Computer chose: {computer}")
print(f"You chose: {user}")


# checks if user entered a valid choice
if user not in select:
    print("Invalid choice! Please enter rock, paper, or scissors only.")
else:
    # winner logic
    if user == computer:
        print("Ohh... it's a tie >,<")
    elif (user == "rock" and computer == "scissors") or \
         (user == "paper" and computer == "rock") or \
         (user == "scissors" and computer == "paper"):
        print("You win! 🎉")
    else:
        print("Computer wins! (00)")
