# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake when using the `setInterval` function within a React `useEffect` hook, leading to a memory leak.  The solution showcases the proper way to handle cleanup to prevent this issue.

**Bug:** The original `MyComponent` uses `setInterval` within `useEffect` without a cleanup function. This means that even if the component unmounts, the interval continues to run, causing a memory leak.

**Solution:** The updated `MyComponent` includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, resolving the memory leak.

**How to run:**
1. Clone the repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`.