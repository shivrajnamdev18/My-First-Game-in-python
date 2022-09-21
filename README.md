# My-First-Game-in-python
i am build this game help of my big brother . and so excited for build the game

# snake, water, gun --- game

import random

def getwinner(p1, p2):
    if p1 == "snake" and p2 == "water":
        return p1
    elif p1 == "snake" and p2 == "gun":
        return p2
    elif p1 == "water" and p2 == "sanke":
        return p1
    elif p1 == "water" and p2 == "gun":
        return p1
    elif p1 == "gun" and p2 == "water":
        return p2
    elif p1 == "gun" and p2 == "sanke":
        return p1
    else:
        return""
def myGame():
    n = 10
    userwinner = 0
    count = 0
    mylist = ["snake","water","gun"]
    while(count < 10):
        player1 = random.choice(mylist)
        player2 = input("enter your choice [ snake, water, gun ] : ")
        print("computer has:", player1, "and you enterd:", player2)
        winner = getwinner(player1, player2)
        if winner == player1:
            print("you lose :(")
        elif winner == player2:
            print("you win! :)")
            userwinner += 1
        else:
            print("no winner!")
            continue
        count += 1
    print("you won", userwinner, "times")

if __name__=="__main__":
    myGame()
    print("Game Over")
