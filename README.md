# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  Specifically, the example shows a route that fetches a user by ID.  If the ID is not a valid integer, the code will throw an error.  The solution demonstrates how to properly handle such errors.

## Bug

The `bug.js` file contains the buggy code.  It attempts to parse the user ID as an integer without handling potential errors.  If a non-numeric ID is provided, the `parseInt` function will return `NaN`, leading to a failure in the `find` method.

## Solution

The `bugSolution.js` file provides a corrected version.  It includes error handling that checks if the parsed ID is actually a number. If not, it sends an appropriate error response.  This prevents unexpected crashes and provides a more robust user experience.