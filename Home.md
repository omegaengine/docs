![Logo](http://omegaengine.de/images/logo.png)

The OmegaEngine is a general-purpose 3D graphics engine written in C# using the .NET Framework 2.0 and DirectX 9 via [SlimDX](http://slimdx.org/).

The engine is designed to be
 * light-weight (compiled binaries with external libraries < 4MB),
 * modular (use only the parts you need for your project) and
 * gameplay-agnostic (also suitable for visualization projecs, etc.).

The engine is well-suited for strategy games, space simulations, etc.. It is not designed for use in FPSes, open-world sandboxes, etc..

 * **[Features](Features)**
 * **[Screenshots](Screenshots)**
 * **[Download](Download)**

# Code sample #
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

# License #
The main body of the code is covered by the [Mozilla Public License 2.0](http://www.mozilla.org/MPL/2.0/). Please have a look at the [licensing terms](License) covering the different parts of the engine for details.