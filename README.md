# React Native Launch Arguments

React Native module to get launch arguments. It makes passing parameters from testing tool such as Detox to react native super easy.

Mostly it's made for using
* [`launchArgs parameter of device.launchApp method`](https://github.com/wix/Detox/blob/master/docs/APIRef.DeviceObjectAPI.md#7-additional-launch-arguments) of [Detox](https://github.com/wix/Detox/)
* [`optionalIntentArguments (Android)` and `processArguments (iOS)`](http://appium.io/docs/en/writing-running-appium/caps/) parameters with [Appium](http://appium.io/)

**iOS**: it takes data from `[[NSProcessInfo processInfo] arguments]`

**Android**: it takes data from `currentActivity.getIntent().getBundleExtra("launchArgs")` for detox and `intent.getExtras()` for ADB params


## Getting started

```sh
npm i @qeepsake/react-native-launch-arguments
cd ios && pod install && cd ..
```

## Usage

In JS:

```js
import { LaunchArguments } from "@qeepsake/react-native-launch-arguments";
LaunchArguments.value();
```

In TS:

```ts
import { LaunchArguments } from "@qeepsake/react-native-launch-arguments";
interface MyExpectedArgs {
  authToken?: string;
  skipAuth?: boolean;
}
LaunchArguments.value<MyExpectedArgs>();
```
## License

MIT © [qeepsake](https://github.com/Qeepsake)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center">
      <a href="http://www.lukebrandonfarrell.com">
        <img src="https://avatars3.githubusercontent.com/u/18139277?v=4" width="100px;" alt=""/><br />
        <sub><b>Luke Brandon Farrell</b></sub>
      </a>
      <br />
      <a href="#projectManagement-lukebrandonfarrell" title="Project Management">📆</a> 
      <a href="https://github.com/aspect-apps/use-redux-effect/commits?author=lukebrandonfarrell" title="Code">💻</a>
    </td>
    <td align="center">
      <a href="https://github.com/iamolegga">
        <img src="https://avatars3.githubusercontent.com/u/5501657?v=4" width="100px;" alt=""/><br />
        <sub><b>iamolegga</b></sub>
      </a>
      <br />
      <a href="#projectManagement-iamolegga" title="Project Management">📆</a> 
      <a href="https://github.com/aspect-apps/use-redux-effect/commits?author=iamolegga" title="Code">💻</a> 
      <a href="https://github.com/aspect-apps/use-redux-effect/commits?author=iamolegga" title="Documentation">📖</a>
    </td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!