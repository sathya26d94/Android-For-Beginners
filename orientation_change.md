# Working with Orientation Change in Android App

When user changes orientation of phone from portrait to landscape, **Android destroys your current activity and creates a new activity by calling onCreate() method in your current Activity**

Lets say, if user is filling a form in a screen. If user knowingly/unknowlingly changes orientation of phone, all the data user enter will be wiped & the screen will be created freshly. User may not like this behaviour, as they have to enter all the details again from start

So its the responsibility of the developer to maintain the state of components even if user changes orientation

Here is the simple tutorial on how to save & retrieve state after orientation change

## Retaining components state on Orientation change

```java
EditText editText;

@Override
protected void onCreate(Bundle savedInstanceState) {
   super.onCreate(savedInstanceState);
   editText = (EditText) findViewById(R.id.edit);
   if (savedInstanceState != null) {
      CharSequence savedText = savedInstanceState.getCharSequence("mydata");
      editText.setText(savedText);
   }
}

@Override
protected void onSaveInstanceState (Bundle bundle) {
    super.onSaveInstanceState(bundle);
    bundle.putCharSequence("mydata", mTextView.getText());
}
```

> Whenever use changes orientation, Android will call onSaveInstance() method, where we save state of EditText into a bundle. When onCreate() called after orientation changes, **first check if the savedInstanceState is not null**. if its not null, you can assume the Activity is recreated after change in orientation

> When the app is opened for the first time, savedInstanceState param in onCreate() will be null


## How to stop switching to Landscape mode

In case younot wish to allow landscape mode for your app, please specify screenOrientation value as "portrait" in AndroidManifest.xml file

Lets see how to achieve it 

```xml
 <activity android:name=".MainActivity"
           android:screenOrientation="portrait">
</activity>
```

## Reference

[activity tag in AndroidManifest](https://developer.android.com/guide/topics/manifest/activity-element)
