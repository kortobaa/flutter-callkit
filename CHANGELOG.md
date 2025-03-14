## 2.1.0

- (Android) Add the possibility of setting a Notification icon;

## 2.0.9

- (iOS) Fix getting call state;

## 2.0.8

- (iOS) Fix second and next calls issue;

## 2.0.7

- (iOS) Fix audio after accepting from killed state;

## 2.0.6

- (iOS) Fix crashing on startup ([#44](https://github.com/ConnectyCube/connectycube-flutter-call-kit/issues/44))

## 2.0.5

- (Android) fix the compatibility with `Flutter` **3.x.x**;

## 2.0.4

- (Android) update `Gradle` version to the **6.5**;
- (Android) update `Kotlin` version to the **1.6.21**;
- (Android) megrate from the `jcenter()` to the `mavenCentral()` dependesies repository;

## 2.0.3

- (Android) fixed the working with apps targeted to the `targetSdkVersion 31` and above;

## 2.0.2

- (iOS, Android) fixed the `user_info` data transporting;
- (Android) fixed launching the app by `acceptCall` event;

## 2.0.1

* Minor updates

## 2.0.0
Completely reworked version. Reworked the way of interaction between the flutter app and native platforms.

Since this version you don't need any third-party plugins for working with push notifications anymore, cause all required functionality has already been integrated into the plugin.

**New**
- Added iOS support
- Added getting the subscription tokens (VoIP for the iOS and FCM for the Android)
- Added customisation for ringtone, app icon, color accent (for Android)

**Fixes and improvements**
- reworked callbacks `onCallRejectedWhenTerminated` and `onCallAcceptedWhenTerminated` now they will be fired even if the app is terminated or in the background
- migrated to `EventChannel` for sending events from native platforms to the Flutter app

## 0.1.0-dev.2

* Improved compatibility with projects which support Web platform.

## 0.1.0-dev.1

* New:
    - Implemented Dart [null-safety](https://dart.dev/null-safety) feature;
    - Added method `getCallData(String? sessionId)` for getting all provided data about the call;
    - Added method `clearCallData(String? sessionId)` which cleans all data related to the call;
    - Added method `getLastCallId()` which returns the id of the last displayed call. It is useful on starting app step for navigation to the call screen if the call was accepted;
    - Added static callback `onCallAcceptedWhenTerminated` which can be useful if need listen to events from the Call notification in the background or terminated state;

* Improvements:
    - Added new field `userInfo`, which can be used for exchanging with additional data between the Call notification and your app, you will get this data in callbacks `onCallAcceptedWhenTerminated`, `onCallAccepted`, `onCallRejectedWhenTerminated`, `onCallRejected` after setting it in method `showCallNotification`;

* Fixes:
    - Fixed the wrong calback naming `onCallAcceptedWhenTerminated` -> `onCallRejectedWhenTerminated`;

## 0.0.1-dev.1

* Initial release.
