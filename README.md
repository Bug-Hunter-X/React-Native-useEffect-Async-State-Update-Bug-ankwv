# React Native useEffect Async State Update Bug

This repository demonstrates a common bug in React Native applications involving asynchronous state updates within the `useEffect` hook.  The bug leads to unexpected behavior and potentially unnecessary re-renders. The solution showcases how to correctly handle asynchronous operations to prevent this issue.

## Bug Description
When an asynchronous operation within `useEffect` modifies the component's state, the state update might not be reflected immediately. This can lead to data inconsistencies or unexpected UI behavior.  Additionally, improper handling can trigger additional re-renders that may degrade performance.

## How to reproduce
1. Clone this repo.
2. `cd` into the directory.
3. `npm install`
4. `npx react-native run-android` or `npx react-native run-ios`
5. Observe the unexpected behavior in the application. 

## Solution
The solution uses the `async/await` syntax with an immediate return of the `useEffect` function after calling `setState`, to improve readability, and prevent additional re-renders. 