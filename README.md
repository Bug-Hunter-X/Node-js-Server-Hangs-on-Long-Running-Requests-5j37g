# Node.js Server Hanging Issue

This repository demonstrates a common issue in Node.js where long-running requests can cause the server to hang, making it unresponsive.  The original `server.js` file shows the problematic code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The `server.js` file contains a simple HTTP server that simulates a long-running task (a 5-second delay) within the request handler.  This blocks the event loop, preventing the server from handling subsequent requests.  This results in a unresponsive server and poor performance.

## Solution

The `serverSolution.js` demonstrates the correct approach.  Asynchronous operations prevent the main thread from being blocked. This ensures responsiveness even under heavy load.

## How to Run

1. Clone this repository.
2. Navigate to the directory.
3. Run `node server.js` to see the problematic behavior.
4. Run `node serverSolution.js` to see the corrected solution.

## Note

This example highlights the importance of using asynchronous programming techniques in Node.js to avoid blocking the event loop and maintaining server responsiveness.