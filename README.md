# React: Memory Leak from setInterval in useEffect

This repository demonstrates a common React bug: a memory leak caused by the improper use of `setInterval` within a `useEffect` hook without a cleanup function.  The `setInterval` function continues to run indefinitely, causing memory issues if the component unmounts before the interval is cleared.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a count every second. However, it lacks a cleanup function in the `useEffect` hook to stop the interval when the component unmounts. This leads to a memory leak.

## Solution

The `bugSolution.js` file shows the corrected code.  A cleanup function is added to the `useEffect` hook. This function uses `clearInterval` to stop the interval when the component is unmounted, preventing the memory leak.

## How to run

1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.