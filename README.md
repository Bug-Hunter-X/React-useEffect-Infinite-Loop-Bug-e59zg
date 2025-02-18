# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array. 

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Bug

The `useEffect` hook in `bug.js` logs the current count to the console. However, because the dependency array `[]` is empty, the effect runs after every render, causing an infinite loop and crashing the application.

## Solution

The `bugSolution.js` file fixes the bug by including `count` in the dependency array. This ensures the effect only runs when the `count` value changes. 