[<=== Back](../README.md)

# Intent Filters

## [Allowing Other Apps to Start Your Activity](https://developer.android.com/training/basics/intents/filters)
*from developer.android.com*

To allow other apps to start your activity, add an `<intent-filter>` element in the manifest file for the corresponding `<activity>` element.

Intent filters should be as specific as possible in terms of the type of action and data the activity accepts.

**Action**

> A string naming the action to perform. Usually one of the platform-defined values such as `ACTION_SEND` or `ACTION_VIEW`.
Specify this in your intent filter with the `<action>` element. The value you specify in this element must be the full string name for the action, instead of the API constant.


**Data**

> A description of the data associated with the intent.
Specify this in your intent filter with the `<data>` element. Using one or more attributes in this element, you can specify just the MIME type, just a URI prefix, just a URI scheme, or a combination of these and others that indicate the data type accepted.


**Category**

> Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started. There are several different categories supported by the system, but most are rarely used. However, all implicit intents are defined with `CATEGORY_DEFAULT` by default.
Specify this in your intent filter with the `<category>` element.

*example*

```
<activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>
```

# [Implicit vs. Explicit Intents](https://developer.android.com/guide/components/intents-filters#Types)
*from developer.android.com*

## Intent Types

There are two types of intents: Explicit Intents and Implicit Intents

**Explicit Intents**: 

> Explicit Intents specify which application will satisfy the intent, by supplying either the target app's package name or a fully-qualified component class name. You'll typically use an explicit intent to start a component in your own app, because you know the class name of the activity or service you want to start. For example, you might start a new activity within your app in response to a user action, or start a service to download a file in the background.

**Implicit Intents**:

> Implicit Intents do not name a specific component, but instead declare a general action to perform, which allows a component from another app to handle it. For example, if you want to show the user a location on a map, you can use an implicit intent to request that another capable app show a specified location on a map.

<img src="img/intent-filters_2x.png" alt="intent filters" width="300"/>


If an intent filter is declared for an activity, it becomes possible for other apps to start that activity with a certain kind of intent. If an intent filter is *not* declared, it can only be started with an explicit intent (from your own app).

