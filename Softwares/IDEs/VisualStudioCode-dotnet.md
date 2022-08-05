# Tips to develop with Visual Studio Code for .NET



## Index
- [.. SDKs](/Softwares/IDEs/VisualStudioCode.md)
- [Extension](#extension)
- [Set to debug mode](#debug-mode)
- [Hide build and debug files](#hide-build-debug-files)



## Extension <a name="extension"></a>

* [C#](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)
* [.NET Core Test Explorer](https://marketplace.visualstudio.com/items?itemName=formulahendry.dotnet-test-explorer)
* [Auto-Using for C#](https://marketplace.visualstudio.com/items?itemName=Fudge.auto-using)
* [C# Namespace Autocompletion](https://marketplace.visualstudio.com/items?itemName=adrianwilczynski.namespace)
* [C# XML Documentation Comments](https://marketplace.visualstudio.com/items?itemName=k--kato.docomment)
* [NuGet Reverse Package Search](https://marketplace.visualstudio.com/items?itemName=jesschadwick.nuget-reverse-package-search)


## Set to debug mode <a name="debug-mode"></a>

### When strart up Visual Studio Code
![Enable debug](/media/001-vscode-dotnet-builder-debug.png "Enable debug")

### Extension icon
![Enable debug](/media/002-vscode-dotnet-builder-debug.png "Enable debug")
> Click in `Generate C# Assets for Build and Debug`

### Menu
![Enable debug](/media/003-vscode-dotnet-builder-debug.png "Enable debug")
> `Ctrl` + `Shift` + `P` : And start writing `Generate Assets...`


## Hide build and debug files <a name="hide-build-debug-files"></a>

1. Go Settings
2. Search the configuration: `hide files`
3. Add these pattern
   * `**/bin`
   * `**/obj`
   * `**/.vs`
   * `**/.vscode`

![Hide build and debug files](/media/vscode-dotnet-hide-build-debug-files.png "Hide build and debug files")



## References
[Amichai Mantinband](https://www.youtube.com/watch?v=m9HvsB1-hAo)