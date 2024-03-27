# desugaring



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
