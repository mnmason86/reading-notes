[<=== Back](../README.md)

# Location

## [Getting the last known location](https://developer.android.com/training/location/retrieve-current)
*from developer.android.com*

> Using the Google Play services location APIs, your app can request the last known location of the user's device. In most cases, you are interested in the user's current location, which is usually equivalent to the last known location of the device.

> Specifically, use the fused location provider to retrieve the device's last known location. The fused location provider is one of the location APIs in Google Play services. It manages the underlying location technology and provides a simple API so that you can specify requirements at a high level, like high accuracy or low power. It also optimizes the device's use of battery power.

To access fused location provider, an app's development project must include Google Play services
- Download, install, and add the library

Apps whose features use location services must request location permissions, depending on the use cases of those features.

### Create location services client

In the `onCreate()` method:

```
private FusedLocationProviderClient fusedLocationClient;

// ..

@Override
protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}
```

### Get the location

To request the last known location, call the `getLastLocation()` method:

```
fusedLocationClient.getLastLocation()
        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });
```

This method returns a `Task` that you can use to get a `Location` object with latitude and longitude of a location.

To choose the best location estimate, depending on the app's use case:

`getLastLocation()` gets a location more quickly and minimizes battery usage, but might be out of date.

`getCurrentLocation()` gets a more accurate location, but can cause active location computation on the device, which may consume large amounts of power if the location isn't available or if the request isn't stopped correctly after obtaining a fresh location.