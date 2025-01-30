# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by a long-running operation blocking the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The `server.js` example uses a `while` loop to simulate a lengthy operation within the request handler. This blocks the event loop, preventing the server from responding to subsequent requests until the loop completes.  This results in the server appearing unresponsive.

## Solution

The `serverSolution.js` file demonstrates how to resolve this issue by using asynchronous programming techniques (e.g., `setTimeout`).  This allows other operations to be processed while the lengthy task is running, maintaining the server's responsiveness.