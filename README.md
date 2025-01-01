# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook. The bug is caused by a missing dependency in the `useEffect` call, leading to an infinite loop.

## Bug Description

The `MyComponent` component uses the `useState` hook to manage a count variable. The `useEffect` hook is designed to log the count to the console whenever the count changes. However, because `count` is not included in the dependency array for the `useEffect` hook, the effect is executed after every render, causing a continuous update cycle and ultimately, an infinite loop. This results in the application becoming unresponsive.

## Solution

The solution involves adding `count` to the dependency array of the `useEffect` hook.  This ensures that the effect only runs when the `count` variable changes.  This fixes the infinite loop issue.