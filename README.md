# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows how forgetting to include dependencies in the dependency array can lead to an infinite render loop.

The `bug.js` file contains the buggy code. The `bugSolution.js` demonstrates the fix.

## Bug
The issue arises because the `useEffect` hook is called on every render, creating an infinite loop. This occurs when a value used inside the `useEffect` function is not included in its dependency array.

## Solution
The solution is to add the correct dependencies to the dependency array. In this example, the `count` variable must be included, ensuring that the effect only runs when `count` changes.