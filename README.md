# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop.  The problem stems from the way JavaScript handles closures and the asynchronous nature of `setTimeout`.

## Problem

The expected behavior of the code in `bug.js` is to print numbers 0 through 9 with a one-second delay between each number. However, due to the asynchronous nature of `setTimeout`, by the time the closures execute, the loop has already finished, and 'i' will hold its final value (10). Thus, the console will print '10' ten times.

## Solution

The solution in `bugSolution.js` uses an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop.  This captures the value of `i` at each iteration correctly, resulting in the expected output.

## How to Run

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment (browser's console, Node.js, etc.).
3. Run each file separately to observe the different outputs.