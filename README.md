# Practical 2R: Programming Resources in Android

Develop an Android application demonstrating the use of Programming Resources (`colors.xml`, `themes.xml`, `strings.xml`, `dimens.xml`, drawable resources) and apply them in UI components.

---

## Project Overview

* **Project Name:** Practical 2R
* **Template:** Empty Views Activity
* **Language:** Java
* **Package Name:** `com.example.practical2r`
* **Architecture:** 1 `AndroidManifest.xml`, 6 Java Files, 1 Drawable Image, 6 Layout XML files, and 4 Values XML files (Total 18 files).

---

## 1. Manifest

### `AndroidManifest.xml`
**Path:** `app > manifests > AndroidManifest.xml`

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)"
    package="com.example.practical2r">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.Practical2R">

        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

        <activity android:name=".ColorActivity" />
        <activity android:name=".DimensionActivity" />
        <activity android:name=".DrawableActivity" />
        <activity android:name=".StringActivity" />
        <activity android:name=".ThemeActivity" />

    </application>

</manifest>
```

---

## 2. Java Source Files
**Path:** `app > java > com.example.practical2r >`

### 1. `MainActivity.java`
```java
package com.example.practical2r;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    public void openColorActivity(View view) {
        startActivity(new Intent(this, ColorActivity.class));
    }

    public void openThemeActivity(View view) {
        startActivity(new Intent(this, ThemeActivity.class));
    }

    public void openStringActivity(View view) {
        startActivity(new Intent(this, StringActivity.class));
    }

    public void openDrawableActivity(View view) {
        startActivity(new Intent(this, DrawableActivity.class));
    }

    public void openDimensionActivity(View view) {
        startActivity(new Intent(this, DimensionActivity.class));
    }
}
```

### 2. `ColorActivity.java`
```java
package com.example.practical2r;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class ColorActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_color);
    }
}
```

### 3. `DimensionActivity.java`
```java
package com.example.practical2r;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class DimensionActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_dimension);
    }
}
```

### 4. `DrawableActivity.java`
```java
package com.example.practical2r;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class DrawableActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_drawable);
    }
}
```

### 5. `StringActivity.java`
```java
package com.example.practical2r;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class StringActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_string);
    }
}
```

### 6. `ThemeActivity.java`
```java
package com.example.practical2r;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class ThemeActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_theme);
    }
}
```

---

## 3. Drawable Resources

* **File Name:** `pebbles.jpg`
* **Path:** `app > res > drawable > pebbles.jpg`
* **Instruction:** Copy your image file from your local folder and paste directly into the `drawable` folder (do not drag and drop). Keep the image file size small (within KB size).

---

## 4. Values XML Files
**Path:** `app > res > values >`

### 1. `colors.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="purple_200">#FFBB86FC</color>
    <color name="purple_500">#FF6200EE</color>
    <color name="purple_700">#FF3700B3</color>
    <color name="teal_200">#03DAC5</color>
    <color name="teal_700">#FF018786</color>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="custom_green">#9ADA03</color>
    <color name="custom_brown">#FFC49662</color>
    <color name="custom_pink">#E91E63</color>
    <color name="custom_blue">#0000FF</color>
</resources>
```

### 2. `dimens.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <dimen name="activity_padding">24dp</dimen>
    <dimen name="view_margin">16dp</dimen>
    <dimen name="text_size_medium">18sp</dimen>
</resources>
```

### 3. `strings.xml`
```xml
<resources>
    <string name="app_name">Practical 2R</string>
    <string name="btn_click">Click on me</string>
    <string name="welcome_heading">Welcome to Practical 2R</string>
    <string name="string_demo_desc">This is a string resource demo.</string>
    <string name="studio_welcome">Welcome to Android Studio.</string>
    <string name="practical_resources">This is your Practical 2 Resources.</string>
</resources>
```

### 4. `themes.xml`
```xml
<resources xmlns:tools="[http://schemas.android.com/tools](http://schemas.android.com/tools)">
    <!-- Base application theme. -->
    <style name="Theme.Practical2R" parent="Theme.MaterialComponents.DayNight.DarkActionBar">
        <!-- Primary brand color. -->
        <item name="colorPrimary">@color/purple_500</item>
        <item name="colorPrimaryVariant">@color/purple_700</item>
        <item name="colorOnPrimary">@color/white</item>
        <!-- Secondary brand color. -->
        <item name="colorSecondary">@color/teal_200</item>
        <item name="colorSecondaryVariant">@color/teal_700</item>
        <item name="colorOnSecondary">@color/black</item>
        <!-- Status bar color. -->
        <item name="android:statusBarColor">?attr/colorPrimaryVariant</item>
    </style>
</resources>
```

---

## 5. Layout XML Files
**Path:** `app > res > layout >`

### 1. `activity_main.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:gravity="center" android:layout_height="match_parent" android:layout_width="match_parent" android:orientation="vertical" android:padding="@dimen/activity_padding" xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)">

    <TextView android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="wrap_content" android:text="@string/welcome_heading" android:textSize="@dimen/text_size_medium"/>

    <Button android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="match_parent" android:onClick="openColorActivity" android:text="Color Demo"/>

    <Button android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="match_parent" android:onClick="openThemeActivity" android:text="Theme Demo"/>

    <Button android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="match_parent" android:onClick="openStringActivity" android:text="String Demo"/>

    <Button android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="match_parent" android:onClick="openDrawableActivity" android:text="Drawable Demo"/>

    <Button android:layout_height="wrap_content" android:layout_width="match_parent" android:onClick="openDimensionActivity" android:text="Dimension Demo"/>

</LinearLayout>
```

### 2. `activity_color.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:background="@color/custom_green" android:gravity="center" android:layout_height="match_parent" android:layout_width="match_parent" android:orientation="vertical" android:padding="@dimen/activity_padding" xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)">

    <TextView android:background="@color/custom_pink" android:layout_height="wrap_content" android:layout_width="wrap_content" android:padding="12dp" android:text="Color Resource Demonstration" android:textColor="@color/white" android:textSize="@dimen/text_size_medium"/>

</LinearLayout>
```

### 3. `activity_theme.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:gravity="center" android:layout_height="match_parent" android:layout_width="match_parent" android:orientation="vertical" android:padding="@dimen/activity_padding" xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)">

    <TextView android:layout_height="wrap_content" android:layout_width="wrap_content" android:text="Theme Applied from themes.xml" android:textSize="@dimen/text_size_medium"/>

</LinearLayout>
```

### 4. `activity_string.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:gravity="center" android:layout_height="match_parent" android:layout_width="match_parent" android:orientation="vertical" android:padding="@dimen/activity_padding" xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)">

    <TextView android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="wrap_content" android:text="@string/string_demo_desc" android:textSize="@dimen/text_size_medium"/>

    <TextView android:layout_height="wrap_content" android:layout_marginBottom="@dimen/view_margin" android:layout_width="wrap_content" android:text="@string/studio_welcome" android:textSize="@dimen/text_size_medium"/>

    <TextView android:layout_height="wrap_content" android:layout_width="wrap_content" android:text="@string/practical_resources" android:textSize="@dimen/text_size_medium"/>

</LinearLayout>
```

### 5. `activity_drawable.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:gravity="center" android:layout_height="match_parent" android:layout_width="match_parent" android:orientation="vertical" android:padding="@dimen/activity_padding" xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)">

    <ImageView android:contentDescription="Pebbles Drawable Resource" android:layout_height="250dp" android:layout_width="250dp" android:scaleType="centerCrop" android:src="@drawable/pebbles"/>

</LinearLayout>
```

### 6. `activity_dimension.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:gravity="center" android:layout_height="match_parent" android:layout_width="match_parent" android:orientation="vertical" android:padding="@dimen/activity_padding" xmlns:android="[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)">

    <TextView android:layout_height="wrap_content" android:layout_margin="@dimen/view_margin" android:layout_width="wrap_content" android:text="Dimension Demonstration" android:textSize="@dimen/text_size_medium"/>

</LinearLayout>
```

---

## Execution Instructions

1. Connect or start the **Pixel 4 API 25 (Android 7.1.1 Nougat)** AVD Emulator.
2. Click the green **Play (Run)** button at the top of the Android Studio interface.
3. Test each screen by clicking the buttons on the main screen and using the device Back button to return to `MainActivity`.
