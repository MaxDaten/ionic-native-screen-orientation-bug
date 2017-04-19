# Screen Orientation Error

see: https://github.com/driftyco/ionic-native/issues/1001

Note:

1. Installed via
  ```sh
  > npm install ionic-native@2.9.0
  > ionic plugin add cordova-plugin-screen-orientation@2.0.0 --save
  ```
2. manually moved `node_modules/ionic-native/dist` content to `lib/ionic-native`
  ```sh
  > cp -r node_modules/ionic-native/dist/* www/lib/ionic-native/
  ```
3. Added ionic-native to `index.html` after `cordova.js`
4. Added `$cordovaScreenOrientation.lockOrientation('portrait');` to `app.js`

Error:

```js
TypeError: undefined is not an object (evaluating 'util_1.get(window, pluginObj.pluginRef)[methodName].apply')
```

Tested on:

- iOS 8.3
- iOS 10.3
