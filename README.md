# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by a missing dependency in the `useEffect` hook's dependency array.

The `bug.js` file contains the buggy code, while `bugSolution.js` shows the corrected version.

## Bug Description

The `useEffect` hook is intended to perform side effects after a component renders.  However, if the dependency array is missing a crucial state variable (or other value), the effect will run repeatedly causing an infinite loop and potential performance problems.  In this case, the counter updates but is not included in the dependency array.