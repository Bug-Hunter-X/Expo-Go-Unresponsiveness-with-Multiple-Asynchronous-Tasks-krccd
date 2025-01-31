# Expo Go Unresponsiveness with Multiple Asynchronous Tasks

This repository demonstrates a bug where the Expo Go app becomes unresponsive when a large number of asynchronous operations are performed concurrently. The issue is less prevalent in standalone builds.

## Bug Description

The Expo application exhibits unresponsiveness and potential crashes when executing numerous asynchronous operations simultaneously, such as numerous network requests or intensive background processes. This behavior is primarily observed within the Expo Go client, whereas standalone builds demonstrate improved stability.

## Reproduction Steps

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the app using Expo Go.
4. Trigger multiple asynchronous actions (as defined in the `bug.js` file).
5. Observe the app's performance and potential crashes.

## Solution

The recommended solution involves optimizing asynchronous operations to improve performance, particularly in the Expo Go environment.  See the `bugSolution.js` file for improved handling of asynchronous requests and task management.  This might include techniques like: batching operations, using debouncing or throttling, implementing task prioritization, and using more efficient data handling methods.

## Note

While standalone builds offer better performance, optimizing asynchronous tasks is critical for a robust user experience, even with a standalone app.