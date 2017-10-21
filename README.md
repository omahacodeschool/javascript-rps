JavaScript Rock-Paper-Scissors
==============================

(The setup/installation instructions for this assignment are identical to the [JavaScript Starter](https://github.com/omahacodeschool/javascript-starter#readme) that you might already be familiar with.)

You can launch C9 with this assignment's starter code by clicking this button:

<a href="https://c9.io/auth/github?r=https%3A%2F%2Fc9.io%2Fopen%2F%3Fclone_url%3Dgit%2540github.com%253Aomahacodeschool%252Fjavascript-rps.git"><img src="https://cl.ly/mld9/create-workspace.png" alt=""></a>

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

---

### Enhancing the Program

Have you finished all of the bonuses? If you're ready to move ahead for a new challenge, here are new ways to improve your Rock-Paper-Scissors game.

#### Weapon Validation

Store the valid "weapon" choices (`rock`, `paper`, and `scissors`) in an Array. Then update the weapon validation feature (which verifies the user typed in a valid weapon) so that it simply checks if what the user typed in is in that Array or not.

#### Series

Change the program so that, instead of merely playing 1 game, the program plays _3 games_. Have the computer display the score after each game (including ties).

It's okay if there's not a winner at the end of the 3-game series.

Remember to organize your code using functions, so that you're not repeating too much of your code for each game.

#### Series Scoreboard

Instead of just outputting the score after each game, display a "scoreboard" in the terminal that shows each game's result. Something like this:

```
Game 1: Player 2 won
Game 2: Player 2 won
Game 3: Tie
```

Implement this by storing each game's result in an `Array`. Then fetch each game's result from the `Array` to display the scoreboard.

---

#### Optional

If you're _still_ finding that you want another challenge, here are two paths you can go down:

1. Look up [Rock-Paper-Scissors-Lizard-Spock](https://www.google.com/search?q=rock+paper+scissors+lizard+spock&oq=rock+paper+scirr&aqs=chrome.3.69i57j0l5.2864j0j7&sourceid=chrome&ie=UTF-8) and implement that game.
2. Implement Tic-Tac-Toe (as a new project). (You'll have to copy the files from the [javascript-starter](https://github.com/omahacodeschool/javascript-starter) to begin the new project.)

---

# Loops

Loops!

Are you ready for loops? Below you'll find some of the same enhancements that you were asked to make in previous classes. The difference is that, this time, you should alter the implementation to use loops (where appropriate).

So the tasks below will be familiar, but your challenge is to use loops whereas before you would not have done that.

---

---

## Weapon Validation

Your program should already verify that the player has chosen a valid weapon. But currently you simply exit the program if the player enters an invalid weapon.

Your task is to change the implementation so that the program instead keeps on asking the player for a weapon until they give you a valid response.

Use a `while` loop for this!

```javascript
// Returns True if the weapon is invalid.
function isInvalid(w){
    if ((w !== "Rock") && (w !== "Paper") && (w != "Scissors")){
        return true
    }
}

var weapon = ask.question("Enter your weapon");

// Keep on asking if the weapon is invalid!
while (isInvalid(weapon)){
    weapon = ask.question("Enter your weapon");
}
```

## Series

You've used functions to create a 3-game serious. Now, use a loop so that you don't have to repeat the function call three times. Instead, achieve this with JavaScript using a `while` loop.

```javascript
var gameCounter = 1;

while (gameCounter < 4){
    // Keep playing...
}
```

---

## Series Scoreboard

You should be storing each game's result in an Array so you can display a scoreboard, like this:

```
Player 2 won
Player 2 won
Tie
```

Use a `for` loop to loop through the games' results.

```javascript
for (let result of scoreboard) {
  console.log(result);
}
```

### Extra

If you also want to get the Game Number, you might want to check out the [most advanced loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for). That'll let you do something like this:

```
Game 1: Player 2 won
Game 2: Player 2 won
Game 3: Tie
```