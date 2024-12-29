# React Memory Leak: Uncontrolled setInterval in useEffect

This repository demonstrates a common mistake in React applications involving the `setInterval` function within the `useEffect` hook, leading to a memory leak. The example shows how to fix this issue by clearing the interval in the cleanup function of the useEffect hook.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it doesn't store or clear the interval ID, which causes the interval to continue running indefinitely even after the component is unmounted, leading to a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect` by storing the interval ID and clearing it in the cleanup function. This ensures that the interval is stopped when the component is unmounted, preventing memory leaks.

## How to run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.