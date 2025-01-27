# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js applications: unhandled promise rejections.  The `bug.js` file contains a simple HTTP server with an asynchronous operation that may fail.  Crucially, it lacks proper error handling, leading to a silent failure.

The `bugSolution.js` file provides a corrected version with robust error handling to prevent unhandled promise rejections.

## How to reproduce the bug

1. Clone this repository.
2. Run `node bug.js`.
3. The server will start, but if the simulated asynchronous operation fails (roughly 20% chance), there will be no visible error message.

## Solution

Always handle promise rejections using `.catch()` to prevent unexpected errors and facilitate better debugging and error logging.