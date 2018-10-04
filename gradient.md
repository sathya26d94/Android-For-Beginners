# Creating Gradient Background

> For code sample using gradient colors, refer [SplashScreen_UsingTimers](https://github.com/iamvickyav/SplashScreen_UsingTimer/blob/master/README.md)
## What is Gradient ?

> A term used in computer graphics to describe a fluid range of color filling an area

## How to create Color Gradient in Android ?

### Create your own gradient design under drawable folder

#### drawable/my_gradient.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape>
            <gradient
                android:startColor="@color/bg_start_color"
                android:endColor="@color/bg_end_color"
                android:angle="45"/>
        </shape>
    </item>
</selector>
```

> startColor & endColor forms the two gradient colors & angle helps the direction for color to flow

#### values/colors.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="colorPrimary">#0099ff</color>
    <color name="colorPrimaryDark">#303F9F</color>
    <color name="colorAccent">#FF4081</color>
    <color name="bg_start_color">#3399ff</color>
    <color name="bg_end_color">#ffffff</color>
</resources>
```

## How to preview my gradient color combination ?

> Use the [W3Schools Color gradients picker](https://www.w3schools.com/colors/colors_gradient.asp) 
