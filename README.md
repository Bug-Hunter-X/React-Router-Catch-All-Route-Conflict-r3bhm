# React Router Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) interferes with other, more specific routes.  The problem arises when the catch-all route is defined before the more specific routes, causing it to always be matched regardless of the URL.

The `App.js` file contains the buggy code.  The solution is presented in `AppSolution.js`, which correctly orders the routes to resolve the conflict.

## Solution

The key is to place the catch-all route (`/*`) last in the `<Routes>` component. This ensures it only matches URLs that haven't already been matched by more specific routes.