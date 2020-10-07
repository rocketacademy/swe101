# Project 2: Dice - Beat That!

Begin the app by **forking** this repo: [https://github.com/rocketacademy/swe101-dice-project](https://github.com/rocketacademy/swe101-dice-project)

Create a dice game based on these rules: [https://www.activityvillage.co.uk/beat-that](https://www.activityvillage.co.uk/beat-that)

## Base Version

There will be 2 players. Have a mode for each player. 

Players will take turns. When the player clicks the submit button, it rolls 2 dice.

The game goes into a new mode and shows the 2 dice the player rolled.

The player picks the order of the dice they want.

Example:

{% hint style="success" %}
Player One rolls. 

They roll **Dice 1** as 3 and **Dice 2** as 6.

```text
Welcome Player 1.
You rolled Dice 1:3 and Dice 2:6.
Choose the order of the dice.
```



They can pick **Dice 1** or **Dice 2** as the first numeral of the number.

```text
Player 1, you chose Dice 2 first.
Your number is 63.
It is now player 2's turn.
```

Player One picks **Dice 2** as the first numeral, \(and **Dice 1** as the second\) so gets the number **63**.

Player Two rolls two dice and must create a number that is greater.
{% endhint %}

## More Comfortable

### Variable Number of Dice

Create a new version of the game that deals with two or more dice.

At the beginning of the game is a mode that asks the user how many dice they want to play with.

Each player's set of dice should be stored in an array.

When the player rolls, use a loop to place _**n**_ new dice roll values in the array.

Ask the user to input the _array element position_ of the digits:

```text
You rolled:
----dice: 2 3 1 7
position: 0 1 2 3

Enter the order of the positions of the numbers you want.
```

The user might enter:

```text
3102
```

Which means they want the number 7321.

{% hint style="warning" %}
**Use arrays and loops to construct this number:**

Use  `input` and turn it into a series of positions.

```javascript
var positions = input.split(''); // makes an array: [3,1,0,2];
```

Loop over `positions` to construct the new number.
{% endhint %}



### Score

Keep score for each player. The score is the running sum total of all numbers that player has constructed.

### Auto-Choose

Add functionality where the game auto-selects the highest number from the dice that are rolled. E.g. for dice rolls 2 3 1 6, the game auto-selects 6321.

### Variable Number of Players

At the beginning of the game ask how many players would like to play.

## Submit

[Push](../7-github/7-1-github-fork-and-pull-request.md#git-push) the commits in your local repo to GitHub. [Create a pull request](../7-github/7-1-github-fork-and-pull-request.md#github-pull-request) to submit your assignment. Please fill in the questionnaire in the pull request comments when you submit.

## Reference Solution

Please only refer to the reference solution after you have attempted the project. Thank you!

Note that there are many ways to implement the project and the reference solution is only 1 way.

This reference solution does not include exercises in the More Comfortable section.

[https://github.com/rocketacademy/swe101-dice-project/pull/10/files](https://github.com/rocketacademy/swe101-dice-project/pull/10/files)
