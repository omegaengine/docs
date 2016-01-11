Prerequisites
-------------
* [DirectX June 2010 Runtime](http://omegaengine.de/support/directx-jun2010-minimal.exe)
* [Visual Studio Community 2013](http://www.visualstudio.com/downloads/download-visual-studio-vs#d-community) or better


NuGet packages
--------------
- **[OmegaEngine](http://www.nuget.org/packages/OmegaEngine/)** is the main package. If you are unsure where to start, this is a safe bet.
- **[OmegaEngine.Backend](http://www.nuget.org/packages/OmegaEngine.Backend/)** contains the actual library binaries for the OmegaEngine without the default assets (content and shader files). It is automatically included by the main package. Use this package directly if another project in your solution with the same build output directory already references the main package to avoid duplicating the assets.
- **[OmegaGUI](http://www.nuget.org/packages/OmegaGUI/)** is a skinable GUI toolkit for the OmegaEngine with an XML file format und Lua scripting. The AlphaEditor contains a WYSIWYG editor for the toolkit.

The AlphaFramework is a Model-View-Presenter framework for creating game worlds.
- **[AlphaFramework.World](http://www.nuget.org/packages/AlphaFramework.World/)** is used to build Models.
- The OmegaEngine acts as a View.
- **[AlphaFramework.Presentation](http://www.nuget.org/packages/AlphaFramework.Presentation/)** is used to build Presenters that bind Models to Views.
- **[AlphaEditor](http://www.nuget.org/packages/AlphaEditor/)** is an IDE-like editor for games based on the AlphaFramework. You can use it to create GUI screens, maps, particle systems, etc..


Visual Studio templates
-----------------------
The **[OmegaEngine Templates](https://visualstudiogallery.msdn.microsoft.com/65016a18-e699-47e8-ad91-114faf038d05)** Visual Studio extension can help you set up a suitable project structure.