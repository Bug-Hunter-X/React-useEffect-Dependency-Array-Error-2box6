# React useEffect Dependency Array Error

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can lead to unexpected behavior, including infinite loops and incorrect updates.

## The Problem

The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count. However, the `count` variable is missing from the dependency array. This means the effect runs after every render, regardless of whether `count` has changed.

## The Solution

The `bugSolution.js` file shows the correct implementation.  By including `count` in the dependency array, the effect only runs when `count` changes, resolving the issue.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the component.