# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and missing dependencies, leading to an infinite loop.  The bug occurs because the effect is called on every render without properly specifying dependencies.

## Bug Description

The `useEffect` hook in the provided `MyComponent` continuously updates the state, causing an infinite loop of renders and console logs.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console for the continuous updates.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook.  The dependency array should include all variables from the component's scope that the effect uses. If the effect doesn't use any variables from the component's scope, the dependency array should be empty (`[]`).