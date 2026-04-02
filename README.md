# Rock-Paper-Scissor-game
import random
options = ("rock","paper","scissor")
is_running = True
while is_running:
    computer = random.choice(options)
    player = None

    while player not in options:
        player = input("chose on among rock, paper and scissor :").lower()
    
    print(f"Your choice-{player}")
    print(f"Computer's choice-{computer}")

        
    if player.isalpha():  
        if player == computer:
            print("both chose the same")  
        elif player=="rock" and computer=="paper":
            print("Hahaha! You lose")
        elif player=="rock" and computer=="scissor":
            print("Ohh! You win")
        elif player=="paper" and computer=="rock":
            print("Ohh! You win")
        elif player=="paper" and computer=="scissor":
            print("Hahaha! You lose")
        elif player=="scissor" and computer=="paper":
            print("Ohh! You win")
        elif player=="scissor" and computer=="rock":
            print("Hahaha! You lose")
            
            is_running=False

        else:
            print("please feed alphabets only")
            player = input("chose on among rock, paper and scissor :").lower()
