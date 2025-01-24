# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by improperly using the `useEffect` hook.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.  The issue arises from modifying the state variable within the `useEffect` callback, causing it to re-render and repeatedly trigger the same `useEffect`.

## Bug Description

The original code attempts to increment a counter within the `useEffect` hook's dependency array.  This creates an infinite loop as the state update causes a re-render, which triggers the `useEffect` again, leading to uncontrolled state updates and a crash.