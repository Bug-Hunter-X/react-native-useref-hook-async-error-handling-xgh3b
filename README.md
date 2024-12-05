# React Native useRef Hook Async Error

This repository demonstrates a common error encountered when using the `useRef` hook in React Native with asynchronous operations. The error, 'Cannot read properties of undefined (reading 'current')', occurs because the asynchronous operation might execute after the component unmounts, resulting in an attempt to access a now-undefined ref.

## Problem

The `bug.js` file shows an example where a `setTimeout` function tries to access `myRef.current` after a delay. If the component unmounts before the timeout completes, `myRef.current` will be undefined, causing the error.

## Solution

The `bugSolution.js` file presents a solution that checks if `myRef.current` exists before accessing it. This prevents the error by handling the case where the component has unmounted.