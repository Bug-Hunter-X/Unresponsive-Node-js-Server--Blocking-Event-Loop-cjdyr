# Unresponsive Node.js Server: Blocking Event Loop

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The solution showcases how to use asynchronous operations to prevent this problem.

## Bug

The `server.js` file contains a Node.js HTTP server with a request handler that performs a long-running synchronous operation. This blocks the event loop, making the server unresponsive to new requests.

## Solution

The `server-solution.js` file demonstrates the solution by using asynchronous operations (setTimeout) to prevent blocking the event loop.  This allows the server to continue handling requests while the long-running operation completes in the background.

## How to run

1. Clone this repository.
2. Run `node server.js` to see the bug in action.
3. Run `node server-solution.js` to see the solution.