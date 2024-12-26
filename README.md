# React Native Asynchronous Data Access Error

This repository demonstrates a common but subtle error in React Native applications related to accessing data from asynchronous operations before the data has been fully loaded.

The `bug.js` file contains the erroneous code, which attempts to access a property of an object before the object has been populated.  This results in a 'Cannot read properties of undefined' error. 

The `bugSolution.js` file provides the corrected code, which employs proper error handling and conditional rendering to avoid this error.

## Steps to reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the application using `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the error in the `bug.js` version of the component.
5. Then switch to the `bugSolution.js` version to see the corrected behaviour.

## Solution

The solution involves checking if `data` is not null before attempting to access its properties.  This is commonly done using optional chaining (`?.`) or conditional rendering.