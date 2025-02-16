# Expo Camera: takePictureAsync() error before initialization

This repository demonstrates a common error encountered when using Expo's Camera API: attempting to use `takePictureAsync()` before the camera has fully initialized. The error occurs because the camera's state might still be 'pending' or 'unavailable' instead of 'ready'.

The `bug.js` file shows the incorrect implementation that causes the error, while `bugSolution.js` provides a corrected implementation that ensures the camera is ready before taking a picture.  The solution involves using the camera's `status` property to monitor the initialization state and only calling `takePictureAsync()` when the camera is ready.

This simple example highlights the importance of checking the camera's status before interacting with it.  Always ensure proper asynchronous handling to prevent unexpected errors and maintain application stability.