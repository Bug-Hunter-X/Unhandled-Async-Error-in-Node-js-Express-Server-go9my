# Unhandled Asynchronous Error in Node.js Express Server

This repository demonstrates a common error in Node.js applications involving unhandled exceptions within asynchronous callbacks. The server may crash unexpectedly if an error occurs during an asynchronous operation and there is not adequate error handling. 

## Bug
The `bug.js` file contains an Express.js server with a route that simulates an asynchronous operation.  Sometimes, this operation throws an error, causing the server to crash without proper error handling. 

## Solution
The `bugSolution.js` file provides a solution by using a `try...catch` block to handle the potential error, preventing unexpected server crashes.  This ensures the server remains operational even if errors occur during asynchronous operations.  Additionally, error handling is improved by using `process.on('uncaughtException')` to catch any errors that slip past the `try...catch` block.