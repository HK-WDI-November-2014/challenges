# Code Challenge
Complete the following problems using JavaScript in the order of your choice. Work alone using any resources available to you (but don't look up code solutions!).

## For all challenges

Include all your functions under ```var quiz = {};```

## Challenge 1: Mastermind game

Create a mastermind game using JavaScript : create a function that first generates a random number from 0 to 1000 using ``` Math.floor(Math.random() * 1000) ```, and then answers to a tryThis(num) function that returns "below", "above" or "well done" by comparing num with the previously generated number.

## Challenge 2: function called nearHundred

If the number is between 90 and 99, the result is true; If it is 89 or below, it is false. If it isn't a number, print an error message .
##### Example: 
#### quiz.nearHundred(52) => false
#### quiz.nearHundred(93) => true
#### quiz.nearHundred('two') => Please enter a number!


## Challenge 3: function called missingChar

Remove the character that corresponds to the index from the string, and an error message if you don't enter a string
##### Example: 
#### quiz.missingChar("kittie", 1) => "kttie"
#### quiz.missingChar(347, 1) => Error: Please enter a string!

## Challenge 4: function called delHihi
Remove "hihi" from a string.
##### Example: 
#### quiz.delHihi("abhihicd") => "abcd"
#### quiz.delHihi("xyz") => "xyz"


## Challenge 5: method called backAround
Given a string, move the last character to the beginning.
##### Example: 
#### "cat".backAround() => "tca"
#### "hello".backAround() => "ohell"


