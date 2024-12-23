# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid user IDs.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file shows the corrected version with proper error handling.

## Bug Description

The `GET /users/:id` route attempts to find a user based on the provided ID. However, it lacks error handling. If no user with the given ID is found, the application may crash, resulting in a 500 Internal Server Error.

## Solution

The solution involves checking for the existence of the user before sending a response. If the user is not found, a 404 Not Found response is returned instead of crashing the application.

## How to Run

1. Clone the repository
2. Navigate to the project directory
3. Run `npm install express`
4. Run `node bug.js` (to see the error) and `node bugSolution.js` (to see the corrected version).