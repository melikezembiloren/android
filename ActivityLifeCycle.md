### Project

`app`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`manifests`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`AndroidManifest.xml` -------> Main configuration file.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`kotlin+java`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`app`   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`MainActivity.kt`-------> Main window.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`(android test)` -------> Android specific automation and integration tests.   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`(test)` -------> Unit testing  
`Gradle Scripts`  

### What is an Activity?
An Android activity is a component of the Android app that represents a single screen with a user interface. 
Activities are the building blocks of an Android application and are responsible for presenting the user interface and handling user interactions. 
Typically, an Android application consists of multiple activities, each serving a distinct purpose or presenting a different screen to the user.


The minimal requirements for an entity to be considered an activity include being a class derived directly or indirectly from the Activity class and 
being declared under the <activity> tag in the manifest file.

Every Activity has a special lifecycle.

## Activity Lifecycle
**Simplified Illustration of Activity Lifecycle:   **
It indicates under which circumstances which methods are called.


            
[![image](https://r.resimlink.com/zuhlo.png)](https://resimlink.com/zuhlo)




