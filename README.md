# React Native Dimensions API Inaccuracy Bug

This repository demonstrates a bug where using the React Native `Dimensions` API before component mount leads to inaccurate screen dimension retrieval. The `DimensionsBug.js` file showcases the problematic code, while `DimensionsBugSolution.js` provides a solution.

## Bug Description:
The `Dimensions` API doesn't provide accurate window dimensions until after the component has fully mounted. Accessing the dimensions before this results in either undefined or incorrect values. 

## Solution:
The solution involves using the `useEffect` hook to access the dimensions after the component has rendered.  This ensures the values obtained are accurate.

## How to Reproduce:
1. Clone the repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the initial dimensions, and then compare to dimensions after a slight delay. 