# React Router Dom path="/*" Issue

This repository demonstrates a common issue encountered when using the `path="/*" ` route in React Router Dom v6.  The `path="/*" ` route, intended to act as a catch-all for unmatched routes, is not working as expected. Even when a valid path is present, the catch-all route takes over.

## Problem

The provided code includes a catch all route `path="/*"` which should only be triggered if none of the other routes are matched.  However, in this implementation it is always triggered, regardless of the URL.

## Solution

The solution is to place the catch-all route at the end of all the other routes defined in the `Routes` component.  This ensures that it is only evaluated after other, more specific routes have been checked.