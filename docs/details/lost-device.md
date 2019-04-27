The engine automatically restores a DirectX device if it is lost due to resolution changes, minimizing a fullscreen application, etc..

To reduce the amount of required manual reloading resources are stored in `Pool.Managed` whenever possible.

When this is not possible:

  * A delegate registered at the `engine.DeviceLost` event must release the resource using `.Dispose()`.
  * A delegate registered at the `engine.DeviceReset` event must reload the resource.
