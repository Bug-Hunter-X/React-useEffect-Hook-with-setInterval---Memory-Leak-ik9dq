# React useEffect Hook with setInterval - Memory Leak
This repository demonstrates a common mistake when using the useEffect hook in React with setInterval, leading to memory leaks.  The bug involves a missing cleanup function to clear the interval when the component unmounts. This example shows the incorrect implementation and provides a corrected version.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter. However, it lacks the necessary cleanup function to clear the interval when the component is unmounted. This results in the interval continuing to run even after the component is no longer displayed, leading to memory leaks and unexpected behavior. 

## Solution
The `bugSolution.js` file presents the corrected version of the component.  A cleanup function is included within the useEffect hook's return statement. This function calls `clearInterval` to stop the interval when the component unmounts, thereby resolving the memory leak issue.
