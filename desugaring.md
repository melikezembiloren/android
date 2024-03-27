# desugaring

Android devices are becoming more optimized with each passing day. Numerous features in Android are being optimized for both users and developers. When any Android operating system is developed, it comes with a multitude of Java classes that provide support for various functionalities such as time, date, and more in user devices. For instance, the time API was introduced in API level 26, causing apps using this API to crash on devices with lower API levels like Marshmallow and earlier versions. To prevent app crashes in such cases, Desugaring comes into play, enabling lower API levels to work with new JAVA libraries.
```
android {
    defaultConfig {
        multiDexEnabled = true
    }
```

```
   defaultConfig {
        multiDexEnabled = true
    }

```


```
 compileOptions {
        isCoreLibraryDesugaringEnabled = true
    }
```

```
dependencies {
    coreLibraryDesugaring("com.android.tools:desugar_jdk_libs:2.0.4")
}
```
