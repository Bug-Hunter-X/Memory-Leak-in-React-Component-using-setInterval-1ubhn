# React setInterval Memory Leak
This repository demonstrates a common React bug involving memory leaks due to the improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides the corrected version.

## Problem
The initial implementation of `MyComponent` uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts, leading to a memory leak.  The interval continues running even after the component is removed from the DOM.

## Solution
The solution involves adding a cleanup function to the `useEffect` hook.  This cleanup function uses `clearInterval` to stop the interval when the component is unmounted.  This prevents the memory leak.

## How to Run
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.