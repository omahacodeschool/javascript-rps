JavaScript Rock-Paper-Scissors
==============================

(The setup/installation instructions for this assignment are identical to the [JavaScript Starter](https://github.com/omahacodeschool/javascript-starter#readme) that you might already be familiar with.)

---

Your assignment is to build a playable game of Rock-Paper-Scissors. The game will be played in a terminal by two people. There aren't any graphics. Instead, each player will just type in their "weapon" of choice when it's their turn. It's a very short game :)

## Specifications

When you run `npm start`, the program should greet the players and welcome them to a game of Rock-Paper-Scissors. (Use `console.log` for such messaging.)

It should also ask Player 1 to type in their weapon.

Player 1 should be able to type in their weapon. When they hit the `RETURN/ENTER` key, their turn is over.

Next, Player 2 should be able to type in their weapon. As soon as they hit the `RETURN/ENTER` key, their turn is over and the game is complete! The result should be displayed (e.g. `"Player 1 wins!"`), and the program is finished with its execution.

Note: It's true that Player 2 can cheat by seeing what Player 1 typed in before them. Don't worry about that for now. As you continue with this assignment later, you'll address that problem.

## Core Concepts

Creating this game will require you to understand...

- Conditionals
- Variables

It might also help to know about functions/methods, but their use is not required to get through the assignment.

## Example

Here's an example of what this might look like when you're finished:

![](https://cl.ly/mwVb/Screen%20Recording%202017-10-06%20at%2006.20%20PM.gif)

---

### Bonus

Done early? For a challenge, try some of these tasks:

- If you haven't already, can you find any opportunities for writing a function in this program?
- What happens if a player types in something besides either "Rock", "Paper", or "Scissors"? See if you can make the game exit immediately if a player fails to choose a valid weapon.
- Can you find in this [documentation reference](https://github.com/anseki/readline-sync) what code is needed to **hide** Player 1's weapon from the cheating eyes of Player 2?