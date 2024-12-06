# React 19 useEffect Dependency Array Bug

This repository demonstrates a common error in React 19's `useEffect` hook: improper use of the dependency array.  The bug showcases how a missing or incorrect dependency can result in unexpected re-renders and potential performance issues.

## Bug Description

The `bug.js` file contains a component that uses `useEffect` to log the current count to the console. However, the dependency array is missing, causing the effect to run after every render, leading to excessive logging and potential performance problems. 

## Solution

The solution is shown in `bugSolution.js`. By adding `[count]` as the dependency array, the effect now runs *only* when the `count` state changes, fixing the infinite loop issue. This is a crucial aspect of React's performance optimization strategy.

## How to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs and compare the behavior of the two files (bug.js and bugSolution.js)