# React useEffect setInterval Memory Leak
This example demonstrates a common mistake when using setInterval within a React useEffect hook: failing to provide a cleanup function to prevent memory leaks.
The bug.js file shows the incorrect implementation. The bugSolution.js file provides the corrected code.

## Problem
The `setInterval` function, when used without a cleanup function inside a useEffect hook, continues running even after the component unmounts. This leads to memory leaks and potential performance issues.

## Solution
The solution is to return a function from the useEffect cleanup function.  This function will stop the `setInterval` when the component is unmounted.