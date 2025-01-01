# Accessing environment variables in client-side components in Next.js
This repository demonstrates a common error in Next.js applications when trying to access environment variables within client-side components.  Environment variables are typically intended for server-side processes and are not directly accessible in the browser environment.

## Problem
The `about.js` file attempts to access `process.env.MY_VARIABLE`. This will result in a runtime error because the `process` object is not available in the browser context.

## Solution
The solution is to either:
1. Move the environment variable usage to a server-side function (API route or getServerSideProps) and pass the required data as props to the client-side component.
2. Use a different method for managing configuration data in the client (e.g., setting a variable during build time).