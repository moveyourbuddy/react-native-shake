# React Native Shake Event Detector

(forked from https://github.com/Doko-Demo-Doa/react-native-shake)

With this library, you can add shake event detector on your React Native app. Because `react-native-shake-event` is not in active development anymore, I decided to created this.

Please note that it only works on _real devices_

## Installation

```sh
npm install @moveyourbuddy/react-native-shake
```

or

```sh
yarn add @moveyourbuddy/react-native-shake
```

## Linking the native modules

### Automatic:

```shell
react-native link @moveyourbuddy/react-native-shake
```

### Manual (iOS):

1. Add the `ios/RNShakeEvent.xcodeproj` file to your Xcode project [Demo](https://facebook.github.io/react-native/img/AddToLibraries.png);
2. Add the `Products/libRNShakeEvent.a` file to **Build Phases** [Demo](https://facebook.github.io/react-native/img/AddToBuildPhases.png).

This step is described here: [Linking Libraries](https://facebook.github.io/react-native/docs/linking-libraries-ios.html#content).

### Manual (Android):

```
react-native link @moveyourbuddy/react-native-shake
```

## Usage

```js
import RNShake from "@moveyourbuddy/react-native-shake";

class MyComponent extends React.Component {
  componentWillMount() {
    RNShake.addEventListener("ShakeEvent", () => {
      // Your code...
    });
  }

  componentWillUnmount() {
    RNShake.removeEventListener("ShakeEvent");
  }
}
```
