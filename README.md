# Deck of Cards - Read all of this document before jumping into code

## Objective

You will be building a deck of cards in Ruby.   To accomplish this, you must implement a `Card` class in `card.rb` and a `Deck` class in `deck.rb`.

## Specifications

### Card

* A `Card` should be initialized with two positional arguments, a `value` and a `suit`. The value should be a number from 1-13, and the suit should be a string of either `"hearts"`, `"diamonds"`, `"clubs"` or `"spades"`.  It should be possible to write code like this: `Card.new(4, "spades")`.
* A `Card` should have public instance methods, `value`, and `suit`, that return the value of these arguments. (Hint: you will want to use instance variables and `attr_reader`.)
* A `Card` should also have a public instance method called `face`.   Face should return a string represenation of the card's value.  For instance, `Card.new(1, "hearts").face` should return the string "Ace". If the value is 2, the face should be "2", if the value is 13, the face should be "King", etc...

### Deck

* A `Deck` is made up of 52 `Cards`, so you will need to require the card file at the top of `deck.rb`.
* A `Deck` should be initialized with no arguments, but you will need to set its `@cards` instance variable inside of the `initialize` method.  Calling `Deck.new.cards` should return an array of 52 card with unique value / suit combinations.  **Hint:** you will want to make a loop of every suit, inside a loop of every value, to push each combination of value and suit into an array.
* A `Deck` should have a public method called `shuffle`, which permanently rearranges the order of the cards in its `@cards` instance variable.  Calling `Deck.new.shuffle` should return an array of shuffled cards.
* A `Deck` should have a public method called `draw`.  Calling `Deck.new.draw` should remove one of the deck's cards and return it.  There should be one less card in the deck every time its `draw` method is called.

## Definition of Done

Your goal is to make as many of the specs pass as you can.   You can run all of the specs by running `rspec -fd` from the root of this directory.  Alternatively you can run the "Deck Specks" by running `rspec spec/deck_spec.rb`, or the "Card Specs" by running `rspec spec/card_spec`.

There are some **BONUS** specs in `spec/card_spec`.  They are set to pending with an `x` in front of the word `context`.  If you finish all the regular specs, remove the `x` to turn on the bonus specs.
