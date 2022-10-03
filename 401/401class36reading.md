[<=== Back](../README.md)

# [Amplify and Cognito](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)
*from Amplify docs*

## Getting Started

> The Amplify Auth category provides an interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool. The Amplify CLI helps you to create and configure the auth category with an authentication provider.

### Configure Auth Category

- In the project directory, enter `amplify add auth`
  - Default configuration
  - "username" for sign in
  - No configuration of advanced settings
- Push changes with `amplify push`

### Install Amplify Libraries

In build.gradle:

```
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.37.3'
}
```

### Initialize Amplify Auth

```
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```

### Check the current auth session

```
Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);
```

## Sign In

> The Auth category can be used to register a user, confirm attributes like email/phone, and sign in with optional multi-factor authentication. It is set up to use Amazon Cognito User Pools which manages the users and their properties.

### Register a User

Invoke the following API to initiate a sign up flow:

```
AuthSignUpOptions options = AuthSignUpOptions.builder()
    .userAttribute(AuthUserAttributeKey.email(), "my@email.com")
    .build();
Amplify.Auth.signUp("username", "Password123", options,
    result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
    error -> Log.e("AuthQuickStart", "Sign up failed", error)
);
```

The user will need to confirm their sign up with a code that is sent to the user's email:

```
Amplify.Auth.confirmSignUp(
    "username",
    "the code you received via email",
    result -> Log.i("AuthQuickstart", result.isSignUpComplete() ? "Confirm signUp succeeded" : "Confirm sign up not complete"),
    error -> Log.e("AuthQuickstart", error.toString())
);
```


### Sign in a User

The following method will start the sign in flow:

```
Amplify.Auth.signIn(
    "username",
    "password",
    result -> Log.i("AuthQuickstart", result.isSignInComplete() ? "Sign in succeeded" : "Sign in not complete"),
    error -> Log.e("AuthQuickstart", error.toString())
);
```

*Multi-factor Authentication may also be set up, but some steps can only be chosen during the initial setup of Auth.*