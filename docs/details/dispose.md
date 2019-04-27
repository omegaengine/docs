All classes in the `OmegaEngine` namespace implementing the  `IDisposable` interface must be `.Dispose()`ed manually.

Unlike other .NET objects you can not rely on the garbage collection to cleanup left-over resources here. This is because of circular references caused by [event hooks](lost-device.md) as well as the [asset](../assets/index.md) management system's caching feature.

If you forget a `.Dispose()` this may trigger an exception (in Debug mode) or a log entry (in Release mode) at a non-deterministic point in time.

![](../images/class_diagrams/scene_management.png)
