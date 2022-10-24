# Visual Studio Code
Maybe the best and more complete IDE.



## Index
- [.. Softwares](/Softwares/README.md)
- [Download](#download)
- [Extensions](#extensions)
  - [Productivity Power Tools](#extensions-productivity-power-tools)
- [Tips](#tips)
  - [Show line numbers](#tips-show-line-numbers)
  - [Show whitespaces](#tips-show-whitespaces)
  - [Map mode on scrollbar](#tips-map-mode-scrollbar)
  - [NuGet Package Manager](#tips-nuget-package-manager)
  - [Unused namespaces (Visual Studio 2017 and 2019)](#tips-unused-namespaces)
  - [Does not close the browser when stop debug](#tips-does-not-close-the-browser-when-stop-debug)
  - [Enabling Source Link](#tips-enabling-source-link)
- [Tools](#tools)
  - [Task list](#tools-tasklist)
  - [Code cleanup](#tools-Code-cleanup)
- [Exclude VisualStudio from windows defender](#windows-defender)
- [HotKeys (Shortcuts)](#hotkeys)
  - [Edit](#hotkeys-edit)
  - [List](#hotkeys-list)


## Download <a name="download"></a>
- [For Windows](https://visualstudio.microsoft.com/vs/)
- [For mac](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio-mac/?sku=communitymac&rel=16)



### Extensions <a name="extensions"></a>


#### Productivity Power Tools 2017/2019 <a name="extensions-productivity-power-tools"></a>
This is an extension bundle installer that will install each of the individual components of Productivity Power Tools for Visual Studio 2017, 2019 and 2022

[To 2017/2019](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.ProductivityPowerPack2017)



### Tips <a name="tips"></a>


#### Show line numbers <a name="tips-show-line-numbers"></a>
1. `Menu` > `Tools` > `Options` > `Text Editor` > `All Languages`
2. Mark the option `Line numbers`

[Official documentation](https://docs.microsoft.com/en-us/visualstudio/ide/reference/how-to-display-line-numbers-in-the-editor?view=vs-2019)


#### Show whitespaces <a name="tips-show-whitespaces"></a>
Mark the option `Menu` > `Edit` > `Advanced` > `View White Space`
> [Equivalence in Visual Studio Code](./VisualStudioCode/README.md#tips-show-whitespaces)


#### Map mode on scrollbar <a name="tips-map-mode-scrollbar"></a>
Show the map on the vertical scrollbar.
![Map mode on scrollbar](/media/visualstudio-tips-map-scrollbar.png "Map mode on scrollbar")

[Official documentation](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-track-your-code-by-customizing-the-scrollbar?view=vs-2022)



#### Default package management format <a name="tips-Default-package-management-format"></a>
1. `Menu` > `Tools` > `Options` > `NuGet Package Manager` > `Default package management format`
2. Change to `PackageReference`


#### Unused namespaces <a name="tips-unused-namespaces"></a>
**Remove unused namespaces**

_Only for Visual Studio 2017 and 2019_
1. Install extension the [Productivity Power Tools 2017/2019](#extensions-productivity-power-tools)
2. `Menu` > `Tools` > `Options` > `Productivity Power Tools` > `PowerCommands` > `General`
3. Mark the option `Remove and Sort Usings on save`


#### Does not close the browser when stop debug <a name="tips-does-not-close-the-browser-when-stop-debug"></a>
1. `Menu` > `Tools` > `Options` > `Project and Solutions` > `Web Projects`
2. Uncheck the option `Stop debugger when browser windows is closed, close browser when debugging`


#### Enabling Source Link <a name="tips-enabling-source-link"></a>
1. `Menu` > `Tools` > `Options` > `Debugging` > `Symbols` and ensure that the 'NuGet.org Symbol Server' option is checked. Specifying a directory for the symbol cache is a good idea to avoid downloading the same symbols again.
![Enabling Source Link](https://devblogs.microsoft.com/dotnet/wp-content/uploads/sites/10/2020/11/visual-studio-step-1.png "Enabling Source Link")
> If you’d like to step into the .NET framework code, you’ll also need check the 'Microsoft Symbol Servers' option.

2. Disable Just My Code in `Menu` > `Tools` > `Options` > `Debugging` > `General` since we want the debugger to attempt to locate symbols for code outside your solution.
![Enabling Source Link](https://devblogs.microsoft.com/dotnet/wp-content/uploads/sites/10/2020/11/visual-studio-step-2.png "Enabling Source Link")
> Verify that Enable Source Link support is checked (it is by default). If you’d like to step into .NET Framework code, you’ll also need to check Enable .NET Framework source stepping. This is not required for .NET Core.

> [Equivalence in Visual Studio Code](./VisualStudioCode/README.md#tips-enabling-source-link)

>> Original source of the tutorial [.NET Blog](https://devblogs.microsoft.com/dotnet/improving-debug-time-productivity-with-source-link/)



### Tools <a name="tools"></a>


#### Task list <a name="tools-tasklist"></a>
A tool to show all your tags TODOs, FIXMEs, etc.
![Task List](/media/visualstudio-tools-tasklist.png "Task List")

**Open window**

`Menu` > `View` > `Task List`

**Add support to tag FIXME**
1. `Menu` > `Tools` > `Options` > `Envirnment` > `Task List`
2. Choose the tag name and priority
2. Button `Add`

![Task List options](/media/visualstudio-tools-tasklist-options.png "Task List options")
> [Equivalence in Visual Studio Code](./VisualStudioCode/README.md#extensions-tasklist)


#### Code cleanup <a name="tools-Code-cleanup"></a>

##### Run
1. `Menu` > `Anazlyze` > `Code cleanup`
2. Run a profile

_Or can use the [shortcut](#tools-Code-cleanup-shortcut)_

##### My configuration suggestion
- Remove unnecessary casts
- Make private fields ReadOnly when possible
- Apply object/collection initialization preferences
- Sort usings
- Sort imports
- Apply Me qualification preferences
- Format document
- Remove unnecessary imports
- Remove unused variables
- Add accessibility modifiers
- Apply file header preferences
- Apply expression/block body preferences
- Apply inline 'out' variables preferences
- Apply implicit/explicit type preferences
- Add/remove braces for single-line control statements
- Apply language/framwork type preferences
- Remove unnecessary usings
- Apply 'this' qualification preferences
- Make private fields readonly when possible
- Sort usings

##### Shortcut <a name="tools-Code-cleanup-shortcut"></a>
![Task List options](/media/visualstudio-tools-code-cleanup.png "Task List options")



### Exclude VisualStudio from windows defender <a name="windows-defender"></a>
1. Go to `Start` > `Settings` > `Privacy & Security` > `Windows Security` > `Virus & threat protection` > Under `Virus & threat protection settings` (Manage settings) > `Exclusions` > `Add or remove exclusions` > `Add an exclusion` > `Folder` > `Select the folder` > `Exclusions`
2. Add VisualStudio exe `C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\devenv.exe` *(The path can be different depending on the version and edition of Visual Studio)*
3. Add your project folder `C:\projects` (That is my example, you can use another folder)

![Exclude VisualStudio from windows defender](/media/vs-windows-defender.png "Exclude VisualStudio from windows defender")



### Hotkeys (Shortcuts)<a name="hotkeys"></a>

#### Edit <a name="hotkeys-edit"></a>
`Menu` > `Tools` > `Options` > `Environment` > `Keyboard`

or

`Ctrl` + `K` + `S`


#### List <a name="hotkeys-list"></a>

**Comments**
- `Ctrl` + `K` `Ctrl` + `C` : Add line comment (Edit.CommentSelection)
- `Ctrl` + `K` `Ctrl` + `U` : Remove line comment (Edit.UncommentSelection)

**Capitalization**
- `Ctrl` + `Shift` + `U` : Transform to uppercase (Edit.MakeUppercase)
- `Ctrl` + `U` : Transform to lowercase (Edit.MakeLowercase)

**Files**
- `Ctrl` + `Shift` + `S` : Save All (File.SaveAll)

**Selection**
- `Shift` + `Alt` + `Up Arrow` : Cursor column select up (Edit.LineUpExtendColumn) (Text Editor)
- `Shift` + `Alt` + `Down Arrow` : Cursor column select down (Edit.LineDownExtendColumn) (Text Editor)
- `Shift` + `Alt` + `Right Arrow` : Cursor column select right (Edit.CharRightExtendColumn) (Text Editor)
- `Shift` + `Alt` + `Left Arrow` : Cursor column select left (Edit.CharLeftExtendColumn) (Text Editor)