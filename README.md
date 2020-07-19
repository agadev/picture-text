# Flutter Vision

This is a Flutter app for extracting text from images using **text recognition** functionality ,built using [Firebase ML Kit](https://firebase.google.com/docs/ml-kit). 

This is fully functional app where user can take picture from either using camera or select image from device gallery and then perform text extraction on it. Once text is extracted it can be shared/copied to clipboard using sharing functionality of device.
This away is inspired by [tutorial](https://blog.codemagic.io/text-recognition-using-firebase-ml-kit-flutter) written by Souvik Biswas.




## App Screenshot

<p align="center">
  <img src="https://github.com/sbis04/flutter_vision/raw/master/Screenshots/mlkit.png" alt="Flutter Vision" />
</p>

## Required configurations

Make sure you complete the following configurations before running the app on your device.

### Android

Go to **project directory** -> **android** -> **app** -> **build.gradle** and set the **minSdkVersion** to **21**:

```gradle
minSdkVersion 21
```

### iOS

* Add the following in `ios/Runner/Info.plist`:
  ```
  <key>NSCameraUsageDescription</key>
  <string>Can I use the camera please?</string>
  <key>NSMicrophoneUsageDescription</key>
  <string>Can I use the mic please?</string>
  ```

* Go to `ios/Podfile`.
  * Uncomment this line:
    ```bash
    platform :ios, '9.0'
    ```

  * Add the following at the end:
    ```bash
    pod 'Firebase/MLVisionBarcodeModel'
    pod 'Firebase/MLVisionFaceModel'
    pod 'Firebase/MLVisionLabelModel'
    pod 'Firebase/MLVisionTextModel'
    ```

Now, you are ready to run the app on your device.

