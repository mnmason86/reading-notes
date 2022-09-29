[<=== Back](../README.md)

# [Publishing Your App](https://developer.android.com/studio/publish)
*from developer.android.com*

Publishing an app means making it available to users. There are two main tasks:
- Prepare the app for realease / build a release version which users can download and install
- Release the app to users / publicize, sell, and distribute the release version

## Preparing for Release

Complete the following tasks:

- Remove `log` calls and the `android:debuggable` attribute from the manifest file.
  - Set app's version information, and configure any required settings to meet Google Play requirements

- Use the gradle build files: use *release* build type to set build settings
  - See [building and running from android studio](https://developer.android.com/studio/run)

- Thoroughly test the release version on at least one target 'handset' device, and one target tablet device

- Ensure that all app resources are updated and included

- Prepare remote servers and services that the app depends on

## Releasing through an Google Play

Three basic steps:

- Prepare promotional materials
  - Screenshots, videos, graphics, and promotional text

- Configure options and upload assets
  - Choose countries, list languages, pricing, app type, category, content rating

- Publish the release version of the app
  - Click "Publish" in the Play Console

**Questions**

**How are releases and versioning related?**

Versioning allows an app to specify the minimum system API with which it is compatible. It is important because users need to know if it will work on their devices, and other apps and services may need to query the system for the app's version.

**What are the 5 main tasks you need to complete to prepare your application for release to the Google Play Store?**
1. Configure app for release
2. Build and sign a release version of your app
3. Test the release version
4. Update app resources
5. Prepare remote servers and services



