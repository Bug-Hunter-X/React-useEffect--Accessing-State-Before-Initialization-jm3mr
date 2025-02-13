# React useEffect: Accessing State Before Initialization

This repository demonstrates a common error in React applications where a state variable is accessed within the `useEffect` hook before it has been properly initialized.  This leads to undefined values and potential errors.

## The Bug
The `bug.js` file shows the incorrect implementation.  The `useEffect` hook attempts to log the `count` variable immediately upon component mount, before `useState` has assigned it a value.  This results in `console.log` outputting `undefined`.

## The Solution
The `bugSolution.js` file provides a corrected version.  By adding a conditional check within the `useEffect` hook, we only access the `count` variable after it's been assigned a value.  This prevents the undefined behavior and ensures correct logging.

## How to Reproduce
1. Clone this repository.
2. Navigate to the directory.
3. Open `bug.js` to see the incorrect code.
4. Open `bugSolution.js` to see the corrected code.