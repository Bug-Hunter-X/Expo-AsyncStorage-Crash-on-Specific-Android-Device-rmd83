# Expo AsyncStorage Crash on Android

This repository demonstrates a bug encountered with Expo's AsyncStorage on a specific Android device. The app crashes on startup with a vague error message. This issue only manifests on a particular Android device; other devices and emulators work correctly.

## Bug Description
The application utilizes AsyncStorage to persist user data. Upon starting the app on the affected device, it crashes immediately without detailed logging information.  Standard debugging techniques, including cache clearing and package reinstallation, were ineffective.

## Solution
The solution involves using a try...catch block around the AsyncStorage operations to gracefully handle potential errors. This allows the application to continue running, even if AsyncStorage is unavailable.