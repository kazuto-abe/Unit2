In this task, you will train your computational thinking skills. If you need to remember what these are, see here.

Situation: 

In a game of guessing a number between 1-100 for two players, player A and player B. 
1. The player A knows the number. 
2. The player B is trying to guess with the least number of attempts.
3. Player A can only reply to a guess from the other player B with “low”, “high”, or “That is the number”.

```.py
import random
number = random.randint(0,100)
print (number)
for n in range(100):
  player_input = int(input("Please guess the number from 0 to 100 \n"))
  if number == player_input:
    print("That is the number! You got this!")
    break
  elif player_input > number:
    print("The number is lower")
  elif player_input < number:
    print("The number is higher")
  else:
    print("Please put an POSITIVE integer")
```
