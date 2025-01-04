# React Router Nested Route Path Parameter Conflict

This repository demonstrates a common issue encountered when using nested routes with dynamic parameters in React Router v6.  Specifically, a route with a path parameter (e.g., `/:id`) can conflict with other routes if nested incorrectly.

## Bug Description
The bug occurs when a route with a path parameter is nested within another route that might also match the same path.  This leads to unexpected routing behavior, where the nested route might unintentionally capture parameters meant for the parent route, or vice versa. The specific example showcases a route with the path `/:id` that leads to issues when nested within other routes, even if it has a `path` prop for the nested route that only matches the route `/:id`.