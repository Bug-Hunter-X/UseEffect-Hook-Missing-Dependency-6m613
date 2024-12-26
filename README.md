# useEffect Hook Missing Dependency in React
This repository demonstrates a common bug in React applications involving the `useEffect` hook: missing dependencies in the dependency array.

## The Problem
The provided `bug.js` file contains a component that uses the `useEffect` hook to log the current count. However, there's a crucial mistake: the dependency array is missing the `count` variable.

This omission leads to unexpected behavior.  The effect runs only once after the initial render, and then never again, even though the `count` state is being updated, because it isn't correctly included as a dependency in the second argument of `useEffect`.  The solution demonstrates how to include the dependency.