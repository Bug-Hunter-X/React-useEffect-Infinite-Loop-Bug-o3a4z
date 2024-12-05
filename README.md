# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by incorrectly managing dependencies.

## Bug Description
The `MyComponent` attempts to increment a counter in the `useEffect` hook, but the dependency array `[count]` causes the effect to run continuously, leading to an infinite render cycle. This can freeze your browser or application.

## Bug Solution
The solution involves correctly managing the dependencies passed to `useEffect` to prevent unnecessary re-renders. In this specific case, the effect should only run once after the component mounts. The dependency array should be empty `[]` to achieve this effect.