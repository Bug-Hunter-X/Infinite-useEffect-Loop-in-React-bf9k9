# Infinite useEffect Loop in React

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook.  The example showcases how a missing dependency array leads to the effect running on every render, causing performance problems.

## Problem
The provided `MyComponent` utilizes the `useEffect` hook without specifying a dependency array.  This causes the effect to re-run after every render, creating an infinite loop that significantly impacts performance and may crash the application.

## Solution
The solution involves adding the `count` variable to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` value changes.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the counter button. You'll see the 'Effect running' message continuously logged, indicating the infinite loop.
