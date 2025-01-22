# Incorrect Conditional Logic in React useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook where the conditional logic within the effect is not correctly handled, leading to unexpected behavior.

## Description

The `bug.js` file contains a React component that uses the `useState` and `useEffect` hooks. The intent is to log a message to the console only when the `count` state variable is greater than 0. However, the conditional logic within the `useEffect` hook is flawed. Because the effect runs after the first render, `count` is initially 0, making the `if` condition false initially. Subsequent updates to the `count` cause the effect to run again with the correct value.