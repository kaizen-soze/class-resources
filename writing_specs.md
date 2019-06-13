# How (and why) to write a product spec
Picture this: you have a great idea for an app, spin up a repo, pull up your coding editor, and get to work. Everything's cool, right?

Probably not. Writing good software is a big undertaking, and unless you know where you're going it's really easy to get bogged down in the minutiae. Getting stuck reduces your sense of momentum and makes finishing a project much more difficult.

## What is a tech spec?
A spec is a technical document that describes the core functionality of what your app will do.

Specs do not talk about how to do something except in the broadest of terms. Don’t talk about specific variables or code structure. Just describe what should happen.

The exception is if you’re doing something novel or unorthodox. Do describe, briefly, how the feature will work.

A tech spec is a blueprint. It describes what the final product looks like but does not describe how it works.

## How to write a tech spec
1. Understand in full what the app needs to do.
2. Begin describing every single feature of the app.
Focus on what the feature accomplishes, not how it’s done.
    > Correct: “The calculator display updates every time a key is pressed.”
    
    > Incorrect: “Once a button is clicked, the event listener grabs the display element and updates the value attribute.”
3. Repeat for every feature until the entire app is described.

## Describing algorithms in a tech spec
Understand in full what the algorithm needs to do.

Describe each step of the algorithm in plain English.

> Correct: “The plus method accepts two arguments, x and y, and adds them together. The method returns the sum”

> Correct: “The plus method accepts any number of arguments and adds them together. Each argument is checked to verify it is a number. The method returns the sum.”

> Incorrect: “The plus method adds numbers”
