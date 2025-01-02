# Node.js Server Unresponsiveness Bug

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation within the request handler.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The `server.js` code simulates a 5-second CPU-bound operation inside the request handler. During this time, the Node.js event loop is blocked, preventing the server from responding to other requests. This leads to server hangs and poor performance.

## Solution

The `serverSolution.js` file demonstrates how to resolve this issue by using asynchronous operations.  This allows other requests to be handled concurrently without blocking the event loop.  This example uses `setTimeout` for simplicity but more complex asynchronous operations would follow the same principle.