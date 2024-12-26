# Infinite Rendering Bug in React

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.

The `bug.js` file contains the buggy component.  The `bugSolution.js` file provides the corrected version.

## Bug Description

The `useEffect` hook in `MyComponent` lacks a dependency array. This causes the effect to run after every render, leading to an infinite loop and a browser crash. Each render triggers the effect, which triggers a re-render, and so on.

## Solution

The solution involves adding a dependency array to the `useEffect` hook.  This ensures that the effect only runs when the specified dependencies change. In this case, the effect only needs to run when the `count` state variable changes.