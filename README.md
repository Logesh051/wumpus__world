# Experiment No. 9: Solve Wumpus World Problem using Python Demonstrating Inferences from Propositional Logic

## Name: LOGESH.N.A

## Register Number: 212223240078

## AIM

To solve the Wumpus World Problem using Python demonstrating inferences from Propositional Logic.

---

## THEORY

Wumpus World is a knowledge-based environment used to demonstrate Artificial Intelligence and Propositional Logic.

The environment consists of:

* Wumpus
* Pit
* Gold
* Agent

The agent starts from a safe location and attempts to reach the goal while avoiding dangers.

The agent can perceive:

* Breeze → Indicates a nearby Pit.
* Stench (Smell) → Indicates a nearby Wumpus.

The agent uses logical inference to determine safe paths and reach the goal successfully.

---

## ALGORITHM

1. Create the Wumpus World environment.
2. Place the agent in the starting position.
3. Accept movement from the user.
4. Check for Breeze and Smell.
5. If Wumpus is detected, allow the agent to throw an arrow.
6. If Gold is found, declare victory.
7. If the agent falls into a Pit or meets the Wumpus, terminate the game.
8. Display the final score.

---

## PROCEDURE

1. Define the Wumpus World grid.
2. Initialize player position.
3. Accept movement commands.
4. Move the player in the specified direction.
5. Detect Breeze and Smell conditions.
6. Allow arrow throwing when required.
7. Check for Gold, Pit, or Wumpus.
8. Display the result.

---

## PROGRAM

```python
wumpus = [["Safe","Breeze","PIT","Breeze"],
          ["Smell","Safe","Breeze","Safe"],
          ["WUMPUS","GOLD","PIT","Breeze"],
          ["Smell","Safe","Breeze","PIT"]]

row = 0
column = 0

while True:

    move = input("u/d/l/r : ")

    if move == 'u' and row > 0:
        row -= 1

    elif move == 'd' and row < 3:
        row += 1

    elif move == 'l' and column > 0:
        column -= 1

    elif move == 'r' and column < 3:
        column += 1

    print("Current Location:",
          wumpus[row][column])

    if wumpus[row][column] == "GOLD":
        print("GOLD FOUND! You Won")
        break

    elif wumpus[row][column] == "PIT":
        print("Fell into PIT")
        break

    elif wumpus[row][column] == "WUMPUS":
        print("WUMPUS Found! Game Over")
        break
```

---

## SAMPLE INPUT

```text
r
d
d
r
```

---

## SAMPLE OUTPUT

```text
Current Location: Breeze
Current Location: Safe
Current Location: GOLD

GOLD FOUND! You Won
```

---

## RESULT

Thus the Wumpus World Problem was solved successfully using Python.
