# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input. Specifically, the code attempts to parse a user ID as an integer without validating that it's a number, leading to potential errors.

## Bug
The `bug.js` file contains an Express.js route handler that fetches a user by ID.  If the ID is not a valid number, the `parseInt` function will return `NaN`, leading to an incorrect lookup or potentially a crash. 

## Solution
The `bugSolution.js` file demonstrates how to properly handle this by adding input validation to check if the ID is a valid number before parsing.  It utilizes a `try...catch` block to handle potential errors during the parsing process.