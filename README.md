# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid or unexpected input.  Specifically, the example shows a route that fetches a user by ID but lacks proper handling for cases where the ID is not a number or a valid user does not exist.

## Bug

The `bug.js` file contains an Express.js route that fetches a user based on the ID passed in the request parameters.  However, it fails to handle scenarios where:

1.  The `userId` is not a valid number (e.g., a string or special characters).
2.  No user with the provided ID exists.

This can lead to runtime errors, unexpected behavior, or potential vulnerabilities.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler. It includes error handling to address the issues mentioned above.  The solution gracefully handles invalid inputs and returns appropriate HTTP status codes (400 for bad requests and 404 for not found).

## How to Run

1. Clone the repository.
2. Make sure you have Node.js and npm installed.
3. Navigate to the repository's root directory.
4. Install dependencies: `npm install express`
5. Run the application: `node bug.js` (or `node bugSolution.js` for the solution)

## Contributing

Feel free to contribute to this project by creating issues or pull requests.