#  DEPENDENCY INJECTION WITH HILT 

Dependency Injection (DI) is a technique widely used n programming and well-suited to Android development.

Implementing dependency injection provides the reusability of code, ease ıf refactoring and ease of testing.

Doing manual dependency injection or service locators in a Android app requires to consturct every class and its dependencies by hand, and to use containers to reuse and manage dependencies.

Hilt is a dependency injection library, built on top of the popular DI library dagger, that reduce the boilerplate of doing manual dependency injection in project. 

In summary, in the hilt, the required dependencies are created as modules and used by injecting them where needed.

## ADDING DEPENDENCIES OF HILT 

* In build.gradle.kts (Project) file

```
plugins{
  ...
  id ("com.google.dagger.hilt.android") version "$hilt_version" apply false

```

* In build.gradle.kts (Module) file

```
plugins {
  ...
  kotlin("kapt")
  id("com.google.dagger.hilt.android")
}
```

```
dependencies{
  ...
  implementation("com.google.dagger:hilt-android:$hilt_version")
  kapt("com.google.dagger:hilt-compiler:$hilt_version")
}
```

```
kapt{
  correctErrorTypes = true
}
```

## HILT IN ACTION

### 1. @HiltAndroidApp
  First, replace your default application with a Dagger Hilt annotated one. The @HiltAndroidApp annotation is used to mark the application class in project. 

  This annotation is crucial for initalizing the Hilt component. When you apply @HiltAndroidApp to your Application class, Hilts sets up the necessary Dagger 2 components and modules for dependency injection.

 ```
  @HiltAndroidApp
  class MyApplication : Application()
  {
    ...
  }
```

### 2. @AndroidEntryPoint
  Secondly, you need to add EntryPoint to your activities and fragments, where dagger hilt injection will be used. The @AndroidEntryPoint annotation is used to mark Android components, such as Activity, Fragment, ViewModel, as injectable. Hilt will handle the injection of dependencies into these components when you use this  annotation.

  This eliminates the need for manually injecting dependencies and ensures thaat the components  are correctly configured for dependencjy injection.


```
  @AndroidEntryPoint
  class MainActivity : AppCompactActivity()  {

    @Inject
    lateinit var analytics : AnalyticsAdapter

  }
```
The MainActivity class is marked as an injectable Android component. When you annotate the analytics field with @Inject, Hilt will provide an instance of AnalyticsAdapter automatically when the MyActivity is created.

### 3. @Inject

  The @Inject annotation is used to inform Hilt that a particular field or constructor requires dependency injection. It can be applied to fiels, constructor parameters, or methods. Hilt will provide instances for these annotated elemens based on the definitions in the dagger modules.



  




