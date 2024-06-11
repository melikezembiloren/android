##  DEPENDENCY INJECTION WITH HILT 

Dependency Injection (DI) is a technique widely used n programming and well-suited to Android development.

Implementing dependency injecction provides the reusability of code, ease ıf refactoring and ease of testing.

Doing ömanual dependency injection or service locators in a Android app requires to consturct every class and its dependencies by hand, and to use containers to reuse and manage dependencies.

Hilt is a dependency injection library, built on top of the popular DI library dagger, that reduce the boilerplate of doing manual dependenc injection in project. 

In summary, in the hilt, the required dependencies are created as modules and used by injecting them where needed.
