# Overview

Demo/tutorial for learning to use TFJS with React Native with a pose detection model.

## Run it locally
If running on a mobile device, as I am, DO NOT upgrade the Expo app to v51. Certain TensorFlow features are not compatible with it at this time. 

Install packages:

```shell
yarn install
```

Run the application:

```shell
yarn start
```

If you want to run a clean install, run these first:

```shell
rm -rf node_modules
rm yarn.lock
```

Depending on the Expo Go version on your mobile device, you may need to do a clean install with updated expo dependencies to resolve compatibility issues. 

## Other configs
In the app.json, I had to include these configurations:

```
    "sdkVersion": "50.0.0",
    "jsEngine": "jsc",
    "plugins": [
      [
        "expo-camera",
        {
          "cameraPermission": "Allow $(PRODUCT_NAME) to access your camera."
        }
      ]
    ]
```

* Expo defaults to use the "Hermes" jsEngine, but "jsc" provides full compatibility with third-party libraries. 
* "sdkVersion" should match your mobile device's Expo app supported SDKs. 
* "expo-camera" plugin for device camera permission is required.
