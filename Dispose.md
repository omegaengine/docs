All classes in the `OmegaEngine` namespace implementing the  `IDisposable` interface must be `.Dispose()`ed manually.

Unlike other .NET objects you can not rely on the garbage collection to cleanup left-over resources here. This is because of circular references caused by [event hooks](DeviceLost) as well as the [asset](Asset) management system's caching feature.

If you forget a `.Dispose()` this may trigger an exception (in Debug mode) or a log entry (in Release mode) at a non-deterministic point in time.

![](http://omegaengine.de/images/class_diagrams/scene_management.png)