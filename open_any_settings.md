# How to Open any Settings in Android ? (Including Wifi, Location, Bluetooth etc.)

**Note**: Settings is an in-built app in Android designed by Google. Usually we use **Intents** to Open one app from another. Consider Settings like any other app.

```java
Intent intent = new Intent(Settings.ACTION_LOCATION_SOURCE_SETTINGS);
startActivity(intent);
```

| Settings                                      | Usage                                       |
| --------------------------------------------- |:-------------------------------------------:|
| Settings.ACTION_LOCATION_SOURCE_SETTINGS      | Opens Location Settings                     |
| Settings.ACTION_SETTINGS                      | Opens Settings Page                         |
| Settings.ACTION_DISPLAY_SETTINGS              | Open Settings to modify display preferences |
| Settings.ACTION_FINGERPRINT_ENROLL            | Open Fingerprint settings page              |
| Settings.ACTION_WIFI_SETTINGS                 | To enable Wifi                              |

To see entire list, please refer [List of Settings](https://developer.android.com/reference/android/provider/Settings)
