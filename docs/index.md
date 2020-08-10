![Logo](images/logo.png)

The OmegaEngine is a general-purpose 3D graphics engine written in C# using the .NET Framework 2.0 and DirectX 9 via SlimDX.

The engine is designed to be

 * light-weight (compiled binaries with external libraries < 4MB),
 * modular (use only the parts you need for your project) and
 * gameplay-agnostic (also suitable for visualization projects, etc.).

The engine is well-suited for strategy games, space simulations, etc.. It is not designed for use in FPSes, open-world sandboxes, etc..

 * **[Features](features.md)**
 * **[Screenshots](screenshots.md)**
 * **[Downloads](https://github.com/omegaengine/omegaengine/blob/master/README.md#downloads)**
 * **[API documentation](https://api.omegaengine.de/)**

## Code sample
Renders a textured sphere:
```csharp
var engine = new Engine(...);
var scene = new Scene
{
    Positionables = {Model.Sphere(engine, XTexture.Get(engine, "flag.png"))}
};
var view = new View(scene, new TrackCamera());
engine.Views.Add(view);
```
