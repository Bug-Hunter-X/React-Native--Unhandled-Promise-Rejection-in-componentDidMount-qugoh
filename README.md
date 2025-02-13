# React Native: Unhandled Promise Rejection in componentDidMount

This repository demonstrates a common error in React Native applications: attempting to access component state or props before the component has fully mounted. This often leads to unexpected behavior, crashes, or unhandled promise rejections, especially when dealing with asynchronous operations.

## The Problem

The `bug.js` file shows an example where an asynchronous data fetch is initiated within the `constructor` before the component's state is fully initialized.  Accessing `this.state` within the `fetchData` method prematurely can lead to issues. Similarly, trying to render using `this.state` before the data is fetched results in rendering null, or an error.

## The Solution

The `bugSolution.js` file demonstrates how to correctly handle asynchronous operations within lifecycle methods to avoid this problem. By performing the data fetch in `componentDidMount`, you ensure that the component's state is properly initialized before accessing it, resulting in more robust and predictable behavior.

## How to Run

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `react-native run-android` or `react-native run-ios` to run the app on your device or simulator.