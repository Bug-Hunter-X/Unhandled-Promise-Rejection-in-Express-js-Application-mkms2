# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous operations.  The server starts, but crashes silently when the asynchronous operation fails without proper error handling.

## Bug

The `bug.js` file contains an Express.js application with an asynchronous operation (`someAsyncOperation`). This operation simulates a scenario where an error might occur.  The catch block exists but doesn't do anything meaningful to recover.  This leads to a crash without informative error messages.

## Solution

The `bugSolution.js` file provides a corrected version. It utilizes a `try...catch` block within the asynchronous operation's callback to catch any potential exceptions and send appropriate error responses to the client.  Furthermore, it includes a centralized error handler to catch unhandled errors in the Express application.