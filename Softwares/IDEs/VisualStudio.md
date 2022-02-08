# Visual Studio Code
Maybe the best and more complete IDE.



## Index
- [.. Softwares](/Softwares/README.md)
- [Download](#download)
- [Extensions](#extensions)
  - [Productivity Power Tools 2017/2019](#extensions-productivity-power-tools)
- [Tips](#tips)
  - [Display line numbers](#tips-display-line-numbers)
  - [Unused namespaces](#tips-unused-namespaces)
- [Tools](#tools)
  - [Task list](#tools-tasklist)
  - [Code cleanup](#tools-Code-cleanup)
- [HotKeys (Shortcuts)](#hotkeys)
  - [Edit](#hotkeys-edit)
  - [List](#hotkeys-list)


## Download <a name="download"></a>
- [For Windows](https://visualstudio.microsoft.com/vs/)
- [For mac](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio-mac/?sku=communitymac&rel=16)



### Extensions <a name="extensions"></a>


#### Productivity Power Tools 2017/2019 <a name="extensions-productivity-power-tools"></a>
This is an extension bundle installer that will install each of the individual components of Productivity Power Tools for Visual Studio 2017 and 2019

[Download](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.ProductivityPowerPack2017)



### Tips <a name="tips"></a>


#### Display line numbers <a name="tips-display-line-numbers"></a>
1. `Menu` > `Tools` > `Options` > `Text Editor` > `All Languages`
2. Mark the option `Line numbers`
[Official documentation](https://docs.microsoft.com/en-us/visualstudio/ide/reference/how-to-display-line-numbers-in-the-editor?view=vs-2019)


#### Unused namespaces <a name="tips-unused-namespaces"></a>
**Remove unused namespaces**
1. Install extension the [Productivity Power Tools 2017/2019](#extensions-productivity-power-tools)
2. `Menu` > `Tools` > `Options` > `Productivity Power Tools` > `PowerCommands` > `General`
3. Mark the option `Remove and Sort Usings on save`



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


#### Code cleanup <a name="tools-Code-cleanup"></a>

##### Run
1. `Menu` > `Anazlyze` > `Code cleanup`
2. Run a profile

_Or can use the [shortcut](#tools-Code-cleanup-shortcut)_

##### My configuration suggestion
- Apply 'this' qualification preferences
- Sort usings
- Remove unnecessary usings
- Remove unused variables
- Remove unnecessary casts
- Add accessibility modifiers
- Make private fields readonly when possible
- Add/remove braces for single-line control statements

##### Shortcut <a name="tools-Code-cleanup-shortcut"></a>
![Task List options](/media/visualstudio-tools-code-cleanup.png "Task List options")



### Hotkeys (Shortcuts)<a name="hotkeys"></a>

#### Edit <a name="hotkeys-edit"></a>
`Menu` > `Tools` > `Options` > `Environment` > `Keyboard`


#### List <a name="hotkeys-list"></a>

**Comments**
- `Ctrl` + `K` `Ctrl` + `C` : Add line comment (Edit.CommentSelection)
- `Ctrl` + `K` `Ctrl` + `U` : Remove line comment (Edit.UncommentSelection)

**Capitalization**
- `Ctrl` + `Shift` + `U` : Transform to uppercase (Edit.MakeUppercase)
- `Ctrl` + `U` : Transform to lowercase (Edit.MakeLowercase)

**Files**
- `Ctrl` + `Shift` + `S` : Save All (File.SaveAll)