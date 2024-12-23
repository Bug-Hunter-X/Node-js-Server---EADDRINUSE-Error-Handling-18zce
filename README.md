# Node.js Server - EADDRINUSE Error Handling

This repository demonstrates a common Node.js error: `EADDRINUSE`, which occurs when trying to start a server on a port that's already occupied.  The solution shows how to gracefully handle this error.

## Bug
The `bug.js` file attempts to start a simple HTTP server on port 8080. If another process is using this port, the server will fail and throw the `EADDRINUSE` error.

## Solution
The `bugSolution.js` file demonstrates a robust way to handle this situation, using `server.on('error', ...)` to catch the error and handle it appropriately, such as retrying after a delay or exiting gracefully.