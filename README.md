# Expo Linking.getInitialURL() Android Inconsistency

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API on Android. The function intermittently returns `null` even when a deep link is successfully opened, making it unreliable for handling deep links in Android apps.  The issue is specific to Android; iOS functionality is unaffected.

## Steps to Reproduce

1. Clone this repository.
2. Run the app on both Android and iOS emulators/devices.
3. Open a deep link on both platforms.
4. Observe the inconsistent behavior on Android where `getInitialURL` might return `null`, even with a successful deep link.

## Expected Behavior

`Linking.getInitialURL()` should consistently return the deep link URL when the app is opened from a deep link, regardless of the platform (Android or iOS).

## Actual Behavior

On Android, `Linking.getInitialURL()` sometimes returns `null` despite successfully opening the app via a deep link. iOS behavior is consistent and correct.  Debugging this is difficult due to the lack of error messaging.