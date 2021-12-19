

# JS | Four In A Row



## 

After this learning unit, you will be able to:

- Build your own **Four in a row** game, using HTML, CSS and JavaScript
- Create the logic of the game using JavaScript classes
- Separate the logic of the game from the JavaScript DOM operations
- Structure JavaScript files according to the game classes

## Requirements

- [Fork this repo](https://guides.github.com/activities/forking/)
- Clone this repo into your `~/code/labs`

## Submission

Upon completion, run the following commands
```
$ git add .
$ git commit -m "done"
$ git push origin master
```
Navigate to your repo and create a Pull Request -from your master branch to the original repository master branch.
In the Pull request name, add your name and last names separated by a dash "-"

## Deliverables

Write your JavaScript in the provided files.

## Introduction

<iframe src="//giphy.com/embed/FGxy5NYhmH1ra" width="600" height="500" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

[Four in a row](https://en.wikipedia.org/wiki/Connect_Four) is a classic board game where two players have to insert tiles in a grid of 6x7 placed vertically. You have to insert the tiles from the top of the board and drop it.

The goal is to get together four tiles of the same color either horizontally, vertically or diagonally.

|![](https://i.imgur.com/fPDkwB2.png)|![](https://i.imgur.com/wgpZFHg.png)|![](https://i.imgur.com/C0HvRO9.png)|
|--|--|--|

## The board

In the `board.js` file we will need:

- A matrix to store a logical copy of the status of the board
- The color for each player
- An attribute to store who is the player to move next

We will have a function to insert a tile in the board depending on the selected column.

Also, we will create four function to check:

- If there is four tiles of the same color positioned horizontally
- If there is four tiles of the same color positioned vertically
- If there is four tiles of the same color positioned diagonally from top to the right
- If there is four tiles of the same color positioned diagonally from top to the left

We will create a function to check if there is a winner, and a function to change the turn once a tile is placed.

### HINT: The diangonal check

**If you don't want a hint about how to create this diagonal check, you can just skip this section.**

Either diagonals down-left and diagonals down-right, you don't have to check all of them. There are some of them with less than 4 cells in the same diagonal, so don't take those into the check.

- Down-right diagonals: You just need to check the three first rows and the first four columns
- Down-left diagonals: You just need to check the last three rows and the first four columns

### HINT: The Cross check

**If you don't want a hint about how to create this diagonal check, you can just skip this section.**

To check either the horizontal and vertical lines, take in count you don't have to go all the way checking every single tile. This is because you need at least 4 contiguous cells to check.

## User interactions

For the user interactions with the HTML, we will need:
- A function to add a tale once a column is selected by the user
- A function to render the tale in the HTML board
- A function that checks if there is a winner
- A function to render the final winner

## Summary

In this learning unit we created the Four in a Row game by separating first the logic from the rendering. We also learnt how to work with coordinates in a grid, taking in count the near cells to check their values.

## Extra Resources

- [CSS Only Four in a Row](https://codepen.io/william-index/full/waLLzY/)
