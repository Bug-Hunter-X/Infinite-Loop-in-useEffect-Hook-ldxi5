# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from omitting dependencies in the `useEffect` hook's dependency array, leading to an infinite re-render loop.

## Bug Description

The `MyComponent` function uses `useState` to track a counter. The `useEffect` hook attempts to log the count to the console after every render.  However, because `count` is not included in the dependency array, the effect runs continuously causing an infinite loop and crashing the browser tab.

## Solution

The solution involves adding `count` to the dependency array for the `useEffect` hook.