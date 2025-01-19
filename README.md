# React useEffect setInterval Memory Leak
This example demonstrates a common error in React components that use `setInterval` within the `useEffect` hook without proper cleanup.

The `setInterval` function is used to repeatedly update the component's state, but without the cleanup function, the interval continues to run even after the component is unmounted. This can lead to memory leaks and unexpected behavior. 

The `bug.js` file contains the buggy component. The `bugSolution.js` file demonstrates how to fix this by adding a cleanup function to the `useEffect` hook that clears the interval when the component unmounts.