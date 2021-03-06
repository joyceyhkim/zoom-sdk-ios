# Zoom iOS Software Development Kit (SDK)
<div align="center">
<img src="https://s3.amazonaws.com/user-content.stoplight.io/8987/1541013063688" width="400px" max-height="400px" style="margin:auto;"/>
</div>

> **The version in this repo is a device-only version. If you would like to use the version that supports both device and simulator, you can download the version (**ios-mobilertc-all-*.zip**) from the release page: [https://github.com/zoom/zoom-sdk-ios/releases](https://github.com/zoom/zoom-sdk-ios/releases)**

## Latest SDK Notifications
1. New way to retrieve and to send SDK logs. Now you may use the "**Send Logs By Email**" feature to send email with logs for troubleshooting. Our demo app includes this feature, you may refer to the implementation in the demo app for your SDK app.
2. **Variable Name Changes**: Since [v4.3.1.47201.0322](https://github.com/zoom/zoom-sdk-ios/releases/tag/v4.3.1.47201.0322), we have renamed the term "APP" to "SDK" in our demo to avoid confusion between the term "API" and "APP".
3. Please be aware that some of our interfaces are deprecated in the latest release, please check out our [CHANGELOG](https://github.com/zoom/zoom-sdk-ios/blob/master/CHANGELOG.md) for more detail
4. Encounter with issues? The answer might be waiting for you at [Frequently Asked Questions](https://marketplace.zoom.us/docs/sdk/native-sdks/iOS/get-help/faq#frequently-asked-questions) sections.
5. Our brand new [Zoom Developer Community Forum](https://devforum.zoom.us/) is now online!!! Check it out! We are here to help! :D

## Full Documentation && Community Support
You can find the full Zoom iOS SDK documentation and the community support forum here:
<div align="center">
   <a target="_blank" href="https://marketplace.zoom.us/docs/sdk/native-sdks/iOS" style="text-decoration:none">
   <img src="https://s3-us-west-1.amazonaws.com/sdk.zoom.us/Doc-button.png" width="350px" max-height="350px" style="margin:1vh 1vw;"/>
   </a>
   <a target="_blank" href="https://devforum.zoom.us/c/mobile-sdk" style="text-decoration:none">
   <img src="https://s3-us-west-1.amazonaws.com/sdk.zoom.us/Forum-button.png" width="350px" max-height="350px" style="margin:1vh 1vw;"/>
   </a>
</div>

## What is Zoom iOS SDK?

Zoom SDK makes it easy to integrate Zoom with your iOS applications, and boosts up your applications with the power of Zoom.

* **Easy to use**: Our SDK is built to be easy to use. Just import the libraries, call a few functions, and we will take care all video conferencing related stuffs for you.
* **Localizable**: Our SDK naturally supports 7 major languages, and you can add more to grow your applications internationally.
* **Custom Meeting UI**: If you want to add your own decorations to your Zoom meeting rooms, try our Custom UI feature to make your meeting room special.

## Disclaimer

**Please be aware that all hard-coded variables and constants shown in the documentation and in the demo, such as Zoom Token, Zoom Access, Token, etc., are ONLY FOR DEMO AND TESTING PURPOSES. We STRONGLY DISCOURAGE the way of HARDCODING any Zoom Credentials (username, password, API Keys & secrets, SDK keys & secrets, etc.) or any Personal Identifiable Information (PII) inside your application. WE DON’T MAKE ANY COMMITMENTS ABOUT ANY LOSS CAUSED BY HARD-CODING CREDENTIALS OR SENSITIVE INFORMATION INSIDE YOUR APP WHEN DEVELOPING WITH OUR SDK**.

## Getting Started

The following instructions will get you a copy of the project up and running on your local machine for development and testing purposes.
* For detailed instructions, please refer to our documentation website: [[https://marketplace.zoom.us/docs/sdk/native-sdks/iOS](https://marketplace.zoom.us/docs/sdk/native-sdks/iOS)];
* If you need support or assistance, please visit our [Zoom Developer Community Forum](https://devforum.zoom.us/);

### Prerequisites

Before you try out our SDK, you would need the following to get started:

* **A Zoom Account**: If you do not have one, you can sign up at [https://zoom.us/signup](https://zoom.us/signup).
  * Once you have your Zoom Account, sign up for a 60-days free trial at [https://marketplace.zoom.us/](https://marketplace.zoom.us/)
* **An iOS device**
  * **[Note]**:**The examples downloaded from here only works on real device. If you want to try it on iOS simulator, or on all architectures (x86_64, i386, etc.), please use the version (ios-mobilertc-all-*.zip) from release page: [https://github.com/zoom/zoom-sdk-ios/releases](https://github.com/zoom/zoom-sdk-ios/releases);**

### Installing

Clone or download a copy of our SDK files from GitHub. After you unzipped the file, you should have the following folders:

```
├── CHANGELOG.md
├── LICENSE.md
├── [MobileRTCSample] <- Libraries and examples are inside
├── README.md
├── lib
└── version.txt
```
Launch your **Xcode**, navigate to the "MobileRTCSample" folder, and open the MobileRTCSample.xcodeproj file.


```
├── MobileRTCSample
├── MobileRTCSample.xcodeproj
└── MobileRTCSampleScreenShare
```

We provide 2 examples for you:
 * **MobileRTCSample**: An iOS app that has all basic features for login users.
 * **MobileRTCSampleScreenShare**: An iOS extension that enables screen sharing feature.


## Running the tests

Connect your iOS device to your computer and simply press "Run" on selected example, the example will run on your device.


## Documentation

Please visit [[https://marketplace.zoom.us/docs/sdk/native-sdks/iOS](https://marketplace.zoom.us/docs/sdk/native-sdks/iOS)] for details of each features and functions.

## SDK Reference

You may find the SDK interface reference at [https://marketplace.zoom.us/docs/sdk/native-sdks/iOS/sdk-reference](https://marketplace.zoom.us/docs/sdk/native-sdks/iOS/sdk-reference).
If you would like to get a local copy of the SDK reference, you may [download it here](https://github.com/zoom/zoom-sdk-ios/archive/gh-pages.zip).

## Versioning

For the versions available, see the [tags on this repository](https://github.com/zoom/zoom-sdk-ios/tags).

## Change log

Please refer to our [CHANGELOG](CHANGELOG.md) for all changes.

## Frequently Asked Questions (FAQ)

* :one: `dyld: Library not loaded: /usr/lib/libstdc++.6.dylib`:
  * libstdc++ is deprecated for 5+ years, Apple removes it in XCode 10. This issue has been resolved since release version [v4.1.34076.1024](https://github.com/zoom/zoom-sdk-ios/releases/tag/v4.1.34076.1024).
* :two: `dyld: Library not loaded: MobileRTC.framework/MobileRTC`:
  * Our **iOS SDK** is a **dynamic library**, please import the **MobileRTC.framework** into:
    * **Link Binary With Libraries**
    * **Embedded Binaries**
* :three: `d:undefined symbols for architecture x86_64`:
  * The examples downloaded from here only works on real device. If you want to try it on **iOS simulator**, or on all architectures (**x86_64, i386, etc.**) , please use the version (**ios-mobilertc-all-*.zip**) from release page: [https://github.com/zoom/zoom-sdk-ios/releases](https://github.com/zoom/zoom-sdk-ios/releases);
* :four: `Unsupported Architecture. Your executable contains unsupported architecture '[x86_64, i386]`
  * As the answer on StackOverflow([https://stackoverflow.com/questions/42641806/check-and-remove-unsupported-architecture-x86-64-i386-in-ipa-archive](https://stackoverflow.com/questions/42641806/check-and-remove-unsupported-architecture-x86-64-i386-in-ipa-archive)) says:
> Apple has started complaining if app contains simulator architectures during distribution.

  So if you are going to publish your application through App Store, please use the **device-only** version(which is the version in the master branch of our Github repo or the one you downloaded from our SDK documentation).
* :five: App Crashed and log shows the crash point at `TermSBPTUIModule(Cmm::ICmmMessageQueueClient*)`
   * This error appears becuase the instance of the `MobileRTCMeetingServiceDelegate` was not set to `nil` after you finish using our Zoom services. We defined the delegate as `assign` property, which needs to be set to `nil` manually.
```
@property (nullable, assign, nonatomic) id<MobileRTCMeetingServiceDelegate> delegate;
```
   Setting the delegate to nil should fix this crash.
* Not finding what you want? We are here to help! Please visit our [Zoom Developer Community Forum](https://devforum.zoom.us/) for further assistance.


## Support

For any issues regarding our SDK, please visit our new Community Support Forum at https://devforum.zoom.us/.

## License

Please refer to [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* :star: If you like our SDK, please give us a "Star". Your support is what keeps us moving forward and delivering happiness to you! Thanks a million! :smiley:
* If you need any support or assistance, we are here to help you: [Zoom Developer Community Forum](https://devforum.zoom.us/);

---
Copyright ©2019 Zoom Video Communications, Inc. All rights reserved.
