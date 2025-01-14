# React setInterval Memory Leak

This repository demonstrates a common error in React applications: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to memory leaks as the interval continues to run even after the component unmounts.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it lacks a cleanup function within the `useEffect` hook to clear the interval when the component is unmounted. This causes the interval to persist, leading to a memory leak.

## Solution

The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect`.  A cleanup function is provided to clear the interval using `clearInterval` when the component unmounts. This prevents memory leaks and ensures that resources are released appropriately.