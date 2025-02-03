# useEffect Hook with Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: missing dependencies. The `useEffect` hook, when used improperly, can lead to unexpected re-renders and performance issues.

## The Bug
The `bug.js` file contains a `MyComponent` which uses the `useEffect` hook to log the current count.  The problem is the `useEffect` hook lacks the `count` dependency in its dependency array. This causes the effect to run after every render even if the `count` value is the same causing unnecessary re-renders.

## The Solution
The `bugSolution.js` file shows the corrected code. By including `count` in the dependency array, the `useEffect` will only run when the `count` value changes.  This addresses performance concerns and ensures accurate behavior.

## How to Reproduce
1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`
4. Run `npm start`
5. Observe the console logs in `bug.js` and `bugSolution.js` to see the difference.