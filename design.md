# Android-For-Beginners

> This repo is to help beginners of Android development.
> To go to index, [click here](https://github.com/iamvickyav/Android-For-Beginners/blob/master/index.md)

## Design

To make design changes in Android, you may have to work with styles.xml & colors.xml usually residing at **res/values**

By default, styles.xml comes with values like colorPrimary, colorPrimaryDark & colorAccent for the default theme applied to your app

### styles.xml
```xml
<style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
    <!-- Customize your theme here. -->
    <item name="colorPrimary">@color/colorPrimary</item>
    <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
    <item name="colorAccent">@color/colorAccent</item>
</style>
```

@color refers to the properties in color.xml file (available in res/values/colors.xml)

### colors.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <!--   color for the app bar and other primary UI elements -->
    <color name="colorPrimary">#3F51B5</color>

    <!--   used for the status bar -->
    <color name="colorPrimaryDark">#303F9F</color>

    <!--   a secondary color for controls like checkboxes and text fields -->
    <color name="colorAccent">#FF4081</color>
</resources>
```

## Change Background Color of App

If you want to change background color of your app, simply add the following item in styles.xml 

```xml
<item name="android:windowBackground">@color/activityBackground</item>
```

and below in colors.xml

```xml
<color name="activityBackground">#3F51B5</color>
```

## Reference:

[Styles and Themes](https://developer.android.com/guide/topics/ui/look-and-feel/themes)
