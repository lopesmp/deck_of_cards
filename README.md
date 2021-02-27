# Deck of Cards 

## Description
Deck of Cards built with Ruby Language and test library rspec

## Installation 
Make sure to install Ruby in your machine
```
git clone https://github.com/lopesmp/decks_of_cards.git
cd decks_of_cards
rspec
```
# Tests 

## Card
  ### initialize
    when no arguments are present
      raises an error
    when the first argument is an integer from 1-13 and the second argument is a valid card suit
      returns an instance of the Card class
    when the first argument is greater than 13
      raises an error
    when the first argument is lower than 1
      raises an error
    when the first argument is not an integer
      raises an error
    when the second argument is not a valid card suit
      raises an error
  ### value
    returns an integer
    can only be read from, not written to
  ### suit
    returns a string
    can only be read from, not written to
  ### face
    when the value is a number from 2-10
      returns a string describing the face of the card
    when the value is a face card
      returns the name of the face card
    when the value is 1
      returns the string "Ace"

## Deck
  ### initialize
    creates a deck
  ### cards
    returns an array of 52 cards
    contains 13 cards of each suit
  ### shuffle
    rearranges the order of cards in a deck
    returns an array of shuffled cards
  ### draw
    returns a card from the deck
    removes the card from the deck