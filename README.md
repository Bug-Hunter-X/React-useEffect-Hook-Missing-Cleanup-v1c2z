# React useEffect Hook Missing Cleanup
This repository demonstrates a common, yet easily missed, error in React applications: forgetting the cleanup function in the `useEffect` hook.  The `useEffect` hook, while powerful, requires careful consideration, especially when dealing with side effects that need to be cleaned up when the component unmounts.  Failing to provide a cleanup function can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a simple React component that increments a counter.  However, the `useEffect` hook lacks a return statement that would normally contain a cleanup function.  This omission leads to issues when the component unmounts.

## Solution
The `bugSolution.js` file demonstrates the corrected code.  A return function within `useEffect` ensures that cleanup operations are performed when the component is unmounted, preventing potential problems.

## How to reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs; you'll see the mounting message but no unmounting message in the original buggy code.