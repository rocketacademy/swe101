# Code Review Guidelines

## Overall \(All Projects\)

### Formatting

1. Did students use Prettier to format their code?
2. Did their PR pass the automated ESLint test in GitHub?

### Naming

1. Do variable names accurately describe the data they store?
2. Are variable names in camelCase?

### Commenting

1. Are comments sufficient to explain code that may be confusing?
2. Are there redundant comments that don't help the reader understand the code?

### Decomposition

1. Are there repeated sections of code that could be decomposed into helper functions?
2. Would the code be easier to read if more logical segments were decomposed into helper functions, even if code isn't repeated?

### Gameplay

1. Does the game correctly transition between modes?
2. Does the game end after a player wins or does it allow the players to play again without refreshing?

## Project 1: Scissors Paper Stone

1. Did students use `||` to consolidate win, loss, and draw conditions without repeating code?

## Project 2: Beat That!

1. Did students create a helper function to concatenate 2 or more numbers to form a combined number?

## Project 3: Blackjack

1. Is there a function to calculate the sum of the cards in a player's hand?
2. Does that function calculate the hand score correctly, including for aces?

