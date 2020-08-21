# 10.1: Objects

Now we'll continue to build programs of increasing complexity.

We'll be implementing a game of cards, and we'll introduce a new kind of data that will make our programs easier to write and reason about.

Note that the javascript `object` is not the same object concept that is usually refered to in _Object Oriented Programming_. A javascript obejct is refered to as a _hash_ or _dictionary_ in some other languages.

### Compound Data

What is a deck of cards and how could we represent the deck in our program?

First of all, a deck of cards is a bunch of data that is **of the same type**. This implies an array.

We could create an array like so:

```javascript
var cards = ["nine of hearts","ten of hearts", "jack of hearts" ... ];
```

Is this a good representation of a game of cards?

Let's start to think abstractly about what kind of data a deck of cards contains?

#### order

A deck of cards is implicitly ordered. An array was a good choice to represent this.

#### card order

Each card has an rank. Our array of strings doesnt represent this rank, except by the sub-string "nine" etc. A card has a suit. We are representing this by the string "heart". A card has a rank of face cards, which we are not representing. \(`jack < queen`\)

For a given card we need a way to represent the different values in that individual card.

#### objects as compound data

We can use an object to represent a single piece of data that contains heterogenous data- data of all different types.

```javascript
var singleCard = {
  rank : 11,
  suit: "heart",
  name: "jack"
};
```

We've encoded in this variable the three important pieces of data about the card.

We can make this into an array of objects.

#### object data access

```javascript
singleCard.rank
```

```javascript
singleCard.suit
```

```javascript
singleCard.name
```

## card shuffling

```javascript
var getRandomIndex = function(size){
  return Math.floor(Math.random() * size)
};

var shuffleCards = function( cards ){

  var index = 0;
  var cards = [1,2,3];

  while( index < cards.length ){

    var randomIndex = getRandomIndex(cards.length);

    var currrentItem = cards[index];

    var randomItem = cards[randomIndex];

    cards[index] = randomItem;
    cards[randomIndex] = currentItem;

    index = index + 1;
  }

  return cards;
}
```

## High Card

```javascript
var originalCards = [ ... ];

var cards = shuffleCards(originalCards);

var main = function(input){

  var computerCard = cards.pop();
  var playerCard = cards.pop();

  var myOutputValue = "They had: "+computerCard.name + " of "+computerCard.suit+ yu had: "+  "+playerCard.name + " of "+playerCard.suit;

  if( computerCard.rank > playerCard.rank ){
    myOutputValue = myOutputValue + "computer wins.";

  }else if( computerCard.rank < playerCard.rank ){
    myOutputValue = myOutputValue + "you win!!";

  }else{
    myOutputValue = myOutputValue + " its a tie.";
  }

  return myOutputValue;
};
```
