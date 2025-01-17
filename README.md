# React Router v6 Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 involving catch-all routes (`/*`).  When a catch-all route is not correctly positioned within the `Routes` component, it can conflict with other routes and prevent them from rendering correctly.  The example shows how to resolve this conflict by ensuring the catch-all route is placed last in the route hierarchy.

## Problem

The initial `App.js` demonstrates how placing the catch-all route (`/*`) before other routes prevents them from ever being matched.  This leads to only the `NotFound` component rendering regardless of the URL.

## Solution

The `AppSolution.js` illustrates the correct approach. By placing the catch-all route at the end of the `Routes`, after all other routes, it functions as intended. Only when no other route matches will it be rendered. 