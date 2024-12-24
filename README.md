# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, making the server unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem
The server in `bug.js` simulates a long-running task using a `while` loop. This blocks the event loop, preventing the server from handling other requests during this time.  This can lead to timeouts and an unresponsive application.

## Solution
The `bugSolution.js` file demonstrates how to use asynchronous operations to prevent blocking the event loop.  Asynchronous operations allow the server to continue handling other requests while the long-running task is performed in the background.