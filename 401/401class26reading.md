[<=== Back](../README.md)

# [Android Fundamentals](https://developer.android.com/guide/components/fundamentals#Resources)

*from developer.android.com*

Android apps can be written using Kotlin, Java, and C++ languages.

> Each Android app lives in its own security sandbox, protected by the following Android security features:

- Android OS is a multi-user Linux system in which each app is a different user
- The system assigns each app a unique Linux userID, and sets permissions for all the files in an app so that only the userID assigned to that app can access them.
- Each process has its own virtual machine - an app's code runs in isolation from other apps.
- Every app runs its own Linux process.

The Android system implements the *principle of least privilege*: 

Each app, by default, has access only to the components that it requires to do its work and no more.

## App Components

Each component is an entry point through which the system or a user can enter the app.

Four types of app components:

1. Activities
  - The entry point for interacting with the user. Represents a single screen with a user interface.
  - Implemented as a subclass of the `Activity` class.

2. Services
  - A general-purpose entry point for keeping an app running in the background for all kinds of reasons. Does not provide a user interface.
  - Started Services and Bound Services
    - ***Started Services***
      - Tell the system to keep them running until their work is completed.
    - ***Bound Services***
      - Run because some other app (or the system) has said that it wants to make use of the service.
      - Basically, the service providing an API to another process.
  - Implemented as a subclass of the `Service` class.

3. Broadcast receivers
  - A component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcase announcements. 
  - Many broadcasts originate from the system, but apps can also initiate broadcasts
  - Don't display a user interface, but may create a status bar notification
  - Implemented as a subclass of the `BroadcastReceiver` class, and delivered as an `Intent`

4. Content providers
  - Manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that the app can access.
  - To the system, a content provider is an entry point into an app for publishing named data items, identified by a URI scheme.
  - Useful for reading and writing data that is private to the app and not shared
  - Implemented as a subclass of the `ContentProvider` class, and must implement a standard set of API's that enable other apps to perform transactions.

  ## The Manifest File

  > Before the Android system can start an app component, the system must know that the component exists by reading the app's *manifest file*, `AndroidManifest.xml`. The app must declare all its components in this file, which must be at the root of the app project directory.

  The manifest:

  - Identifies any user permissions the app requires, such as Internet access or read-access to the user's contacts.
  - Declares the minimum API Level required by the app, based on which APIs the app uses.
  - Declares hardware and software features used or required by the app, such as a camera, bluetooth services, or a multitouch screen. 
  - Declares API libraries the app needs to be linked against, such as the Google Maps library.