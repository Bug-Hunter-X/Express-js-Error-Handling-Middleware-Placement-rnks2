# Express.js Error Handling Middleware Placement

This repository demonstrates a common error in Express.js applications: incorrect placement of error handling middleware.  Placing error handling middleware before other routes can prevent them from being executed, leading to unexpected behavior.  The solution shows the correct placement of this middleware.

## Bug

The `bug.js` file shows the error: the error handling middleware is placed before the route handler.  This means that any errors that occur in the route handler will not be caught by the middleware.

## Solution

The `bugSolution.js` file shows the correct placement of the error handling middleware.  It should always be placed after all other route handlers to ensure that all errors are caught.