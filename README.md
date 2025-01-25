# Unnecessary Re-renders in React's useEffect Hook

This repository demonstrates a common React performance issue where the `useEffect` hook runs after every render, even when it doesn't need to.  This can lead to unnecessary calculations, API calls, or other side effects, degrading application performance.

The `bug.js` file shows the problematic code, while `bugSolution.js` demonstrates a corrected version using the optional dependency array to control when the effect runs.

## Problem

The `useEffect` hook in `bug.js` is designed to log the current count to the console. However, it runs on *every* render, which is inefficient.  The log message appears multiple times, reflecting the frequent updates. This unnecessary execution can be computationally expensive, especially in complex components or with frequent updates.